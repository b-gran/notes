# Python

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
