# shroud

Wrap the spawn of the executed executable

[![Madlib Project Badge](https://img.shields.io/badge/madlib-purple?logo=github&logoSize=auto)](//github.com/madlib-lang/madlib) <!-- $MADLIB.projectBadge -->
[![shroud v0.0.2](https://img.shields.io/badge/v0.0.2-purple?label=version)](//github.com/brekk/shroud) <!-- $MADLIB.json.version -->

---

A convenient wrapper around `Process.exec` with some additional opt-in safety.

Safest version:
```madlib
import Shroud from "shroud"
import File from "File"

jq = Shroud.killSoftly("jq")
json = File.read("./madlib.json")
pipe(
  chain(jq(["name"]))
)(json)

```
