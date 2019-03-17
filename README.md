# test_mypy_ns_pkg
Testing PEP 420 in mypy

Run with

```python
python3 main.py
```

It will print `1` as expected.

Now run 

```
$ mypy --namespace-packages main.py
main.py:3: error: Module 'foo.bar' has no attribute 'Baz'
```

Adding `__init__.py` to the `foo` directory would fix this.
Need some sanity checking, but maybe this should be added to https://github.com/python/mypy/issues/1645
