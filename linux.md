# Linux

> Miscellaneous notes about developing against Linux/POSIX.

## Bash

### Arrays
#### Creating arrays
```bash
some_array=()
some_other_array=('foo' 'bar')
```

#### Appending elements
```bash
some_array+=('baz')
some_array+=('2 '3')
```

#### Accessing elements
```bash
echo "All elements ${some_other_array[@]}"
echo "The first element ${some_other_array[0]}"
```

**Note**: `echo $your_array` will _only print the first element_.

#### Array length
```bash
echo "Length of some_array: ${#some_array[@]}"
```

## Printing file size

The `du` command (a POSIX standard) can print the size of a file.
`du` counts the number of file system blocks used by the file.
`du` rounds up to the nearest block, so it will be inaccurate if
a block size is used that is larger than the file size.

The minimum block size is 512 bytes, so `du` isn't appropriate
for very small files.

The flags provide different block size counting options.

```bash
# Print the size of file.txt in kilobytes (-k => kilobytes)
du -k file.txt
```
