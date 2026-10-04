# LaTex-Template
Just a place to store the template I use for LaTex lecture notes

## Folder Directory

```c++
.
├── homework // Template for creating homework (Q1, Q1a, Q1b, etc)
└── notes // Template for creating notes (has sections / chapters)
```

Within either `/homework` or `/notes`, you'll find three set of templates

```c++
. // /homework or /notes
├── full // Full example of notes
├── minimal // Barebones example with only Main.tex and preamble (plus custom defs)
└── semi-minimal // Minimal but with Sections and Image folders added
```

Here's the contents of these folders

```c++
./full
├── images // Parent folder path for all images. Called with `includegraphics`
├── include // Preamble, custom commands, definitions, etc
├── Main.pdf // Compiled output of `Main.tex`
├── Main.tex // The main tex file to compile, includes all files in `/Sections`
├── Sections // Child .tex files for different sections / chapters of notes
└── template // Copy-paste contents for Main.tex and Section children and parents
    ├── Main.tex // Example of a main tex file
    ├── Question Parent.tex // (Only in /homework) ex: Question 1 
    ├── Question Child.tex // (Only in /homework) ex: Question 1a 
    ├── Section Child.tex // ex: Section 1.2 
    └── Section Parent.tex // ex: Section 1
```

## Usage

I use this in `VSCode` with the `LaTex-Workshop` plugin.

If you'd like to use the `minted` package (for coding blocks), please add this to your `User Settings` in `VSCode`

```json
"latex-workshop.latex.tools": [
    
        // Assuming this is your default build tool
        {
            "name": "latexmk",
            "command": "latexmk",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-pdf",
                "-outdir=%OUTDIR%",
                "-auxdir=%AUXDIR%",
                "-shell-escape", // <--- Add this line
                "%DOC%"
            ],
            "env": {}
        },
        ...
```
