# AWX EE

This is a fork of [ansible/awx-ee](https://github.com/ansible/awx-ee).

There are a few branches here:

* `stream9` is a copy of the upstream awx-ee but using CentOS Stream 9 as a
  base image.
* `stream9-fallible` uses the above work and instead uses `fallible` and
  `fallible-compat` instead of `ansible-core` to run workloads.
* `stream9-relrod` is based on `stream9` but includes a set of collections and
  packages specific to workloads that I, relrod, need, and eliminates some that
  I don't intend to use in my own projects.

These are pushed to the following:

* `stream9` -> `quay.io/relrod/awx-ee-stream9:latest`
* `stream9-fallible` -> `quay.io/relrod/awx-ee-fallible:latest`
* `stream9-relrod` -> `quay.io/relrod/awx-ee-stream9-relrod:latest`


## Regenerating the build context with podman:

```bash
$ tox -epodman
```

## Regenerating the build context with docker:

```bash
$ tox -edocker
```
