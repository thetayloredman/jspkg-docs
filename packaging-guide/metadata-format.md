---
description: Information on the metadata format used in jspkg packaging.
---

# Metadata Format

jspkg metadata is a simple `Key: Value` storage system.

Just kidding!

\(Not really\)

\(Just a little\)

There are some complicated bits: \(`#` is not a real comment, remove it in your head\)

```text
Key: Value # simple kv pair
Multiline-Key: line 1 of value
 line 2 of value # space matters
. # end of multiline
MKey-With-Paragraphs: paragraph 1 line 1
 paragraph 1 line 2
 . # paragraph splitter
 paragraph 2
.
```

