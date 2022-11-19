
# Use `scikit-learn`

Really the point is: figure out how to get Poetry to specify a depdendency *with a dash* in its name. 

Thus far generates:

```
$ poetry --version
Poetry version 1.1.12
$ poetry install

  TypeError

  expected string or bytes-like object

  at .../site-packages/poetry/core/utils/helpers.py:27 in canonicalize_name
       23│ _canonicalize_regex = re.compile(r"[-_]+")
       24│ 
       25│ 
       26│ def canonicalize_name(name):  # type: (str) -> str
    →  27│     return _canonicalize_regex.sub("-", name).lower()
       28│ 
       29│ 
       30│ def module_name(name):  # type: (str) -> str
       31│     return canonicalize_name(name).replace(".", "_").replace("-", "_")
```

