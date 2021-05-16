# About Packaging

## What really is _packaging_?

  
"packaging" is the act of creating a package for jspkg to install for users.

jspkg uses a binary package format not that different from `.deb`s, but it still has its differences.

## What is in a `.jsp` package?

{% hint style="warning" %}
**Do not** write `.jsp` packages yourself. There are a variety of reasons why you may want to, but there are _many_ better ways.

It's a lot safer and easier to write packages using jspkg's build tools.

**Manually written package archives will not be allowed into the archive.**
{% endhint %}

`.jsp` binary packages are really just fancy `.tar.gz`s, but they contain _nested archives_.

Here's a usual directory tree:

```text
hello-world.jsp
├─ contents.tar.gz
│  ├─ usr/
│     ├─ bin/
│        ├─ hello-world
├─ metadata
```

* `contents.tar.gz`: data to write to the filesystem
* `metadata`: a jspkg [metadata format](metadata-format.md) document with package data

