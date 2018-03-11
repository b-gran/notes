# Python

## Checking membership in a List

There is an operator (`in`) specifically for doing this:
```python
'foo' in ['foo', 'bar'] # true
'baz' in ['foo', 'bar'] # true
```

The `in` operator on Lists has terrible performance compared to other methods of checking membership.
[This SO question](https://stackoverflow.com/questions/7571635/fastest-way-to-check-if-a-value-exist-in-a-list/40963434#40963434) goes into detail.

If performance matters, use a `Set` instead (but still use the `in` operator).
```python
elems = ['foo', 'bar']
equivalent_set = set(elems)
'foo' in equivalent_set # True
'baz' in equivalent_set # true
```

## Opening a REPL for a Django app

The first step is to open the REPL as normal
```bash
python
```

At first, the REPL won't allow you to import models or other Django constructs, so you need to initialise the Django app:
```bash
>>> import django
>>> django.setup()
```

Finally, you're ready to work with Django models directly:

```bash
>>> from rewiresecurities.core.models import ClassInformation, Offering
```
