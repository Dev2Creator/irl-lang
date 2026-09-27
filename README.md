# IRL™ Language 🌱

**The .irl language — Python's words with C's braces.**

```
var age = int(input("Your age: "))

if (age > 18) {
    print(f"adult")
} elif (age > 12) {
    print("teen")
} else {
    print("kid")
}

for (i in range(3)) { print(i) }

memo function fib(n) {
    if (n < 2) { return n }
    return fib(n - 1) + fib(n - 2)
}
print(fib(90))   // instant
```

- **Frozen 2.1 spec:** [LANG.md](LANG.md)
- **Architecture law (Python = bootstrap, Zig = native path):** [DESIGN.md](DESIGN.md)
- **Compiler:** [COMPILER.md](COMPILER.md) — constant folding, DCE, builtin caching, `.pyc` back end, incremental cache
- **For AI assistants:** [AI_GUIDE.md](AI_GUIDE.md)
- Logo assets: [assets/brand/](assets/brand/)

## Run / build / check

```zsh
irl hello.irl                     # run directly
irl lang build hello.irl -O2 -v   # compile to bytecode
irl lang check hello.irl --json   # validate (CI/AI-friendly)
irl lang spec                     # the frozen grammar
irl lang repl                     # persistent-kernel REPL
```

## Status

Bootstrap engine: complete, 100+ parity/feature tests green. Native C
accelerator (machine-code lexer) with pure-Python fallback. The Zig
native backend plugs into the SEESEMBLY IR contract — see DESIGN.md.

AGPL-3.0-or-later · Anika Mukherjee · part of the [IRL™ ecosystem](https://github.com/Dev2Creator/IRL-)
