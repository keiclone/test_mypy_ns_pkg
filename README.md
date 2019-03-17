# test_mypy_ns_pkg
Testing PEP 420 in mypy

Run with

```python
python3 main.py
```

It will print `1` as expected.

Now run 

```
$ mypy main.py
main.py:3: error: Cannot find module named 'foo.bar'
main.py:3: note: See https://mypy.readthedocs.io/en/latest/running_mypy.html#missing-imports
```

Need some sanity checking, but maybe this should be added to https://github.com/python/mypy/issues/1645
