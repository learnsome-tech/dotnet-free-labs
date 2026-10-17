# m01l02-08 · The question mark, the warning, and the escape hatch

**Lesson:** [The C# Language: Types, Variables, and Flow Control](https://learnsome.tech/learn/dotnet-course/m01l02) (lesson 1.2, module 1: C Sharp And .NET Fundamentals) · Free  
**Check:** Graded

## Goal

Read and write everyday C# declarations, numeric choices, nullability and control flow without guessing what the compiler will do.

## Files

- [`starter/Nulls.cs`](starter/Nulls.cs): the listing from the lesson
- [`starter/snippet.csproj`](starter/snippet.csproj)
- [`expected.txt`](expected.txt): the output the check compares with
- [`check.json`](check.json): how `./check` runs and checks this lab

## Steps

1. Go to the starter: `cd labs/m01l02/m01l02-08/starter`
2. Read `Nulls.cs` the way the lesson builds it:
   - Lines 1–5: wears one too
   - Lines 6–10: compiles quietly
   - Lines 11–12: does not check
3. Notes from the lesson:
   - Line 1: string? says the value may be absent, and the compiler now tracks it
   - Line 12: code!.Length compiles silently: the null forgiving operator
4. Run it: `dotnet run`.
5. Check it from the repository root: `./check m01l02-08`.

## Expected output

```text
Nulls.cs(12,36): warning CS8602: Dereference of a possibly null reference.
sku is WID-7
no sku
5
```

## How to check

`./check m01l02-08` copies `starter/` into a scratch directory and runs `dotnet run` there, the way the site's lab sandbox does: that directory is the working directory and `HOME`, `LANG=C.UTF-8`, `TZ=UTC`, a limit of 10 seconds and 256 KiB of output per stream.

It passes when the output matches `expected.txt` by the site's rules, within the limits. Standard output and standard error are compared after the .NET SDK's noise is set aside: restore and build banners, test-platform headers, hosting start-up lines, stack-trace frames and blank lines are dropped, and times, paths, GUIDs and timestamps are masked. `./check` builds the project first (the site compiles within its time limit with a warm compiler), then times the run. A pass here is a pass on the site.

---

[Open the lesson on LearnSome.tech](https://learnsome.tech/learn/dotnet-course/m01l02) · [All labs of this lesson](../README.md) · [Course README](../../../README.md)
