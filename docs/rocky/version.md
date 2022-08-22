---
title: Rocky Linux Release Version Guide
---

This page goes over the Rocky Linux Release Versions, their support, timelines, and how it affects our users.

## Current Supported Releases

Below is a table of Rocky Linux versions, with accompanying general release and (planned or are) end of life dates.

| Major Version  | Release Date  | End of Life          |
|----------------|---------------|----------------------|
| Rocky Linux 8  | June 21, 2021 | May 31, 2029         |
| Rocky Linux 9  | July 14, 2022 | May 31, 2032         |

This however does not tell the full story. See timeline and version policy below.

## Timeline

For a major release of Red Hat Enterprise Linux and thus Rocky Linux, the following should be true:

* Major version is released with support of ten (10) years (exception is Rocky Linux 8, which started at 8.4)
* Five (5) years of minor release updates

  * There are generally ten (10) minor release updates
  * Minor releases come every six (6) months
  * Minor releases generally come with new features and sometimes software rebases

* After five (5) years of minor releases, Enterprise Linux and derivatives go into maintenance only mode for the remainder of its life

The question often becomes, how often are releases? Based on the cadence set out by Red Hat, the months of May and November are generally when minor releases should be released. If May is a guide, that is also when major versions should be released.

Below is a general guideline (which will likely have mistakes) for the "full support" cycle for an Enterprise Linux distribution.

| Info          | .0   | .1       | .2   | .3       | .4  | .5       | .6  | .7       | .8  | .9       | .10 |
|---------------|------|----------|------|----------|-----|----------|-----|----------|-----|----------|-----|
| Release Month | May  | November | May  | November | May | November | May | November | May | November | May |

After `X.10` is released, the following may be true:

* Maintenance Mode starts for the next five (5) years
* No more minor releases; `X.10` is considered the final release version and only this receives updates until End of Life
* CentOS Stream X will cease development (likely before release)

## Version Policy

Rocky Linux follows the same pattern as Red Hat Enterprise Linux. As such, releases aim to be as on time as possible as they are released upstream.

For Rocky Linux 8, previous versions of packages will coexist in the repositories to allow a user to downgrade in case of a regression or other use cases (such as security only updates). However, when a new minor release arrives, all previous updates/versions are *not* carried over.

Rocky Linux 9 does not currently support this policy and can be expected in a future Rocky Linux 9 version. Please see [Peridot Issue #18](https://github.com/rocky-linux/peridot/issues/18).

## End of Life and Unsupported Release Policy

A version of Rocky Linux is considered unsupported if:

* The Rocky Linux version has been superseded by another minor release *or*
* The Rocky Linux release is End of Life

See the examples below.

### Example: An Unsupported Release

When a new Rocky Linux minor release arrives (for example, `8.6`) the following is true:

* The previous version is no longer supported by Release Engineering and the community
* This version is no longer updated and is moved to the [vault](http://dl.rockylinux.org/vault/rocky/)
* You are recommended to update your system with `dnf update`

### Example: An End of Life Release

When an Rocky Linux version has reached its End of Life date (for example, May of 2029), the following is true:

* The release is no longer supported in full by Release Engineering or the community
* The final version is moved to the [vault](http://dl.rockylinux.org/vault/rocky/).
* This release receives no more updates and is no longer supported.
* You are recommended to install a supported Rocky Linux version and migrate your data.