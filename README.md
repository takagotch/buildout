### buildout
---
https://github.com/buildout/buildout

http://www.buildout.org/en/latest/

```py
import os, shutil, sys, subprocess

for d in 'eggs', 'develop-eggs', 'bin', 'parts':
  if not os.path.exists(d):
    os.mkdir(d)

if os.path.isdir('build'):
  shutil.rmtree('build')

try:
  import pkg_resources, setuptools
except ImportError:
  pass
else:
  raise SystemError(
    "Buildout development with a pre-installed setuptools or "
    "distribute is not supported.")
```

```sh
pip install zc.buildout
buildout
```

```
```


