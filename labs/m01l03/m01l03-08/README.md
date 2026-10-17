# m01l03-08 · Equality: references first, members only if you say so

**Lesson:** [Classes, Interfaces, and Object-Oriented C#](https://learnsome.tech/learn/dotnet-course/m01l03) (lesson 1.3, module 1: C Sharp And .NET Fundamentals) · Free  
**Check:** Graded

## Goal

You can model a domain with properties, interfaces and constructor injection, and tell when inheritance is the wrong tool.

## Files

- [`starter/Equality.cs`](starter/Equality.cs): the listing from the lesson
- [`starter/snippet.csproj`](starter/snippet.csproj)
- [`expected.txt`](expected.txt): the output the check compares with
- [`check.json`](check.json): how `./check` runs and checks this lab

## Steps

1. Go to the starter: `cd labs/m01l03/m01l03-08/starter`
2. Read `Equality.cs` the way the lesson builds it:
   - Lines 1–6: reference equality by default
   - Lines 7–14: overrides Equals to compare the code instead
3. Notes from the lesson:
   - Line 4: No operator was defined, so this is still a reference check
   - Line 12: Compare the members you consider to be identity
   - Line 13: Always a pair, always from the same members
4. Run it: `dotnet run`.
5. Check it from the repository root: `./check m01l03-08`.

## Expected output

```text
False
False
True
True
```

## How to check

`./check m01l03-08` copies `starter/` into a scratch directory and runs `dotnet run` there, the way the site's lab sandbox does: that directory is the working directory and `HOME`, `LANG=C.UTF-8`, `TZ=UTC`, a limit of 10 seconds and 256 KiB of output per stream.

It passes when the output matches `expected.txt` by the site's rules, within the limits. Standard output and standard error are compared after the .NET SDK's noise is set aside: restore and build banners, test-platform headers, hosting start-up lines, stack-trace frames and blank lines are dropped, and times, paths, GUIDs and timestamps are masked. `./check` builds the project first (the site compiles within its time limit with a warm compiler), then times the run. A pass here is a pass on the site.

---

[Open the lesson on LearnSome.tech](https://learnsome.tech/learn/dotnet-course/m01l03) · [All labs of this lesson](../README.md) · [Course README](../../../README.md)
