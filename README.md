# travis-job-docker
Test job for travis-ci


|Python|trusty|xenial|bionic|focal|
|:----:|:----:|:----:|:----:|:---:|
|2.7|yes|yes|yes|yes|
|3.0|no|no|no|no|
|3.1|no|no|no|no|
|3.2|no|no|no|no|
|3.3|no|no|no|no|
|3.4|no|yes|no|no|
|3.5|yes|yes|yes|yes|
|3.6|yes|yes|yes|yes|
|3.7|yes|yes|yes|no|
|3.8|yes|yes|yes|yes|
|3.9|yes|yes|yes|yes|
|nightly|yes|yes|yes|yes|
|pypy2|no|no|no|no|
|pypy3|no|no|no|no|


```
arch:
  - amd64
  - ppc64le

dist: trusty

language: python

python:
  - 3.7
  - 3.6
  - 3.3
  - 3.2
  - pypy2

# Disable version 3.3, 3.2 & pypy
jobs: 
  exclude:
    - arch: ppc64le
      python: 3.3
    - arch: ppc64le
      python: 3.2
    - arch: ppc64le
      python: pypy2
 
script:
  - python --version
```

