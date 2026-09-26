# LaTex-Template
Just a place to store the template I use for LaTex lecture notes

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