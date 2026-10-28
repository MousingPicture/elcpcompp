# Comp++

**The compiler for Effective Language C Plus.**

`comp++` is a compiler project developed in C++ to compile programs written in Effective Language C Plus (EL C+).

This repository distributes the compiler executable and official language importers. It is intended for users who want to download and use the compiler without building it from source.

---

# Part 1: Comp++ Compiler

## What is Comp++?

`comp++` is the compiler responsible for processing EL C+ source files and producing executable programs.

Its purpose is to provide a dedicated compilation tool for the EL C+ programming language, including support for language importers that define the keywords used in source code.

## How Does It Work?

The compilation process is designed around these stages:

1. **Read the source file** — loads the EL C+ program.
2. **Read the declaration** — checks the language declaration.
3. **Load the importer** — loads the selected language keyword definitions.
4. **Analyze the program** — checks syntax and reports errors.
5. **Generate the output** — produces a compiled executable for a supported target.

The actual supported features and compilation targets depend on the compiler release.

## Download

Download the appropriate release from the [Releases](../../releases) page.

The distribution includes:

- `comp++` — the compiler executable.
- `iodefault.elhp` — the default English keyword importer.
- `ioid.elhp` — the Indonesian keyword importer.

## Installation

1. Download the appropriate archive from the Releases page.
2. Extract the archive.
3. Keep the compiler and importer files in the locations expected by the compiler.
4. Add the compiler directory to your system's `PATH` if you want to run `comp++` from any terminal directory.

Installation instructions for each supported operating system will be documented as platform releases become available.

## Usage

Compile a source file using the compiler:

```powershell
comp++ main.elcp -o main.exe
```

Here:

- `comp++` runs the compiler.
- `main.elcp` is the source file.
- `-o main.exe` specifies the output filename.

The exact options and supported targets may vary by release.

## Language Importers

Comp++ uses importer files with the `.elhp` extension to define language keywords.

| Importer | Language |
|---|---|
| `iodefault.elhp` | English |
| `ioid.elhp` | Indonesian |

An importer allows the language to use different keyword sets without requiring a separate compiler executable for each language.

## Error Reporting

When compilation fails, the compiler should report the problem so that the programmer can identify and correct the source code.

The available diagnostics depend on the compiler version.

---

# Part 2: Effective Language C Plus

## What Is EL C+?

**Effective Language C Plus (EL C+)** is a programming language designed to work with the `comp++` compiler.

Its source files use the `.elcp` extension. The language supports importer-based keywords, allowing programs to use English or Indonesian keyword definitions.

## A First Program

Using the English importer:

```cpp
#decla <ELCP>
#importer <iodefault.elhp>

main() {
    print("Hello World!");
    return 0;
}
```

This example declares an EL C+ program, selects the English importer, prints a message, and returns an exit code.

## Language Importers

### English: `iodefault.elhp`

The default English importer defines keywords such as:

| Purpose | Keyword |
|---|---|
| Function declaration | `function` |
| Variable declaration | `let` |
| Constant declaration | `constant` |
| Return value | `return` |
| Main entry point | `main` |
| Conditional | `if`, `else` |
| Loop | `while`, `for` |
| Output | `print` |
| Input | `input` |

### Indonesian: `ioid.elhp`

The Indonesian importer provides localized equivalents:

| Purpose | Keyword |
|---|---|
| Function declaration | `fungsi` |
| Variable declaration | `biarkan` |
| Constant declaration | `konstan` |
| Return value | `kembali` |
| Main entry point | `utama` |
| Conditional | `jika`, `lainnya` |
| Loop | `selama`, `untuk` |
| Output | `cetak` |
| Input | `isi` |

The keywords listed above describe the intended importer mapping. Actual language support depends on the compiler release.

## Project Goals

EL C+ aims to provide:

- A dedicated compiler written in C++.
- Language-specific keyword importers.
- A straightforward compilation workflow.
- Support for English and Indonesian programming syntax.
- Native executable generation for supported platforms.

These goals will evolve as the language and compiler develop.

## License and Usage Restrictions

The compiler and official importers are distributed under the license included in this repository.

Please read `LICENSE` before using or redistributing the files.

## Project Status

EL C+ and `comp++` are under development. Supported syntax, compilation targets, and installation methods may change between releases.

