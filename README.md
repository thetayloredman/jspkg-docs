# Welcome!

Welcome to the official jspkg documentation.

## What is jspkg?

jspkg stands for **J**ava**S**cript **P**ac**k**a**g**e Manager.

> Note: jspkg **is not a npm alternative, and never will be.** The intent of this project is similar to that of other GNU/Linux package managers such as pacman, dpkg, apt, zypper, rpm, etc.
>
> The twist in jspkg is that _everything is local_. All packages are installed as your user, so there is no root access required.

## Examples

{% hint style="warning" %}
jspkg is still being developed. These examples are subject to change.
{% endhint %}

### Installing packages

```bash
$ jspkg install hello-world
```

```text
Requesting metadata from repository... 100%
Calculating changes... 100%

The following changes will be made. Read carefully!

The following packages will be installed:
  hello-world, bash

The following packages will be upgraded:
  glibc

Do you want to apply the changes? [Y/n/...?] ?
[y] = yes, continue
[n] = no, abort
[d] = show more details
[D] = show more details through 'less'
[l] = show less details
[L] = show details through 'less'

Do you want to apply the changes? [Y/n/...] d

The following packages will be installed:
  hello-world (repo main, version 1.0.0-1, author badboyhalocat)
  bash (repo main, version 5.2-10, author unknown)

The following packages will be upgraded:
  glibc (from repo main, version unknown, author unknown, to version unknown)

Do you want to apply the changes? [Y/n/...] y

(Reading database... 52 packages currently installed by 24 authors)
Calculating dependency order... 100% (no dependency conflicts found)

Running prerm scripts for upgraded packages...
run prerm for glibc, done

Preconfiguring packages... (preinstall)
run preinstall for glibc (UPGRADE AS_DEP unknown => unknown), done
run preinstall for bash (INSTALL AS_DEP), done
run preinstall for hello-world (INSTALL MANUAL), done

Upgrading glibc from unknown to unknown...
Extracting glibc_unknown-1 over glibc_unknown-0... 100%

Installing bash...
Extracting bash... 100%

Installing hello-world...
Extracting hello-world... 100%

Running postinstall scripts....
run postinstall for glibc, done
run postinstall for bash, done
run postinstall for hello-world, done

Running hooks...
Calculating... 2 hooks apply
[glibc_upgrade]... done
[binst]... done

Operation completed.
```

