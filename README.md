# 💩 Brainfuck Uglifier

A Brainfuck optimizer which removes useless spaces, comments and useless characters from your Brainfuck program.

I know this is pretty useless, but I am trying some new programming languages and this is a really simple task to replicate across all the programming languages that I am currently testing.

**Other Languages:** <br />
- [GoLang](https://github.com/micheleriva/brainfuck-uglifier-go)
- [Ruby](https://github.com/micheleriva/brainfuck-uglifier-ruby)
- [Crystal](https://github.com/micheleriva/brainfuck-uglifier-crystal)

**Work in progress:**
- [Common Lisp](https://github.com/micheleriva/brainfuck-uglifier-common-lisp)

# Usage

Given the following brainfuck program:

```brainfuck
-[--->+<]>--.   # S
[--->+<]>--.    # O
[--->+<]>-----. # Space
+++++[->+++<]>. # O
+.              # P
++++.           # T
-----------.    # I
++++.           # M
----.           # I
-[--->+<]>++.   # Z
---[->+++<]>.   # E
-.              # D
[->+++<]>++.    # Point
```

Parse it in Crystal like this:

```crystal
program = Uglifier.new "./test/test.bf"

puts program.uglify
# -[--->+<]>--.[--->+<]>--.[--->+<]>-----.+++++[->+++<]>.+.++++.-----------.++++.----.-[--->+<]>++.---[->+++<]>.-.[->+++<]>++.
```

# License
[MIT](/LICENSE.md)