# julia-physicists-cheatsheet
A handy reference for the lecture Advanced Statistical Physics (and others)



<br>

<br>

<br>

<br>


# Introduction

This is a (not so) small and elective collection of important code-snippets for the Advanced Statistical Physics lecture. For convenience of julia-beginners there is a small basic tutorial, which is directed to people who have experience in programming but are new to julia. Another good start is [julia express](http://bogumilkaminski.pl/files/julia_express.pdf). Other cheat cheets are from [juliadocs](https://juliadocs.github.io/Julia-Cheat-Sheet/) the comparison-cheatsheet from [QuantEcon]{https://cheatsheets.quantecon.org/}, which is also great and lists many useful snippets. More comprehensive examples can be found on [rip-tutorials](https://riptutorial.com/julia-lang).

## Specifics of julia

julia is a high-performance, dynamic programming language and very convenient for numerical calculations. Especially in comparison to Python the speed is sometimes magnitudes better and close to C.

### Differences to other programming languages

- julia is quite strict with the definition of so-called *scopes*. This is the region in which variables are defined. E.g. you cannot call variable from outside within a for-loop. More on this later in the [section *pitfalls*](#sec:pitfalls).
- no semicolons needed at the end of line (but they can be used in the interactive REPL-promt to supress output)
- `if`, `for`, `while`, ... have to be terminated by `end`
- strings have to be placed of double quotation marks: `"foo"`
- indexing of arrays etc. is 1-based not 0-based, end is given by `end`, e.g. `f[1],` `f[2],` `...,` `f[end-1],` `f[end]`. Be aware of this when looping (out-of-bonds-error)!
- a range is given by `start:step:stop`
- Julia saves arrays "column major", whereas languages like C and Python use "row major", so use loops along columns for best speed. Details: [link](https://docs.julialang.org/en/v1/manual/performance-tips/#man-performance-column-major)
- Since julia is very fast, in most cases you do not have to write "vectorized" code. Instead just use loops.


### Recommended IDEs

Although you can use any plaintext-editor for writing code, I can recommend Jupyter if you are used to it or like the use of the so-called notebooks ([IJulia](https://github.com/JuliaLang/IJulia.jl)). If not or you like more plaintext based IDEs, try [Atom](http://docs.junolab.org/stable/man/installation/) or [Visual Studio Code](https://www.julia-vscode.org/), which have nice features like displaying plots, a built-in profiler (shows which lines of code take much computation time), workspace (view of all variables and their values) and progressbars. Read the respective section for more details.

# ... continued in julia-cheatsheet.pdf
