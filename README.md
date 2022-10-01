# Lectures conspects.


## What is this repo?
Here will be lectures for study terms >=3.

Conspects for term 1 and 2 can be found [here](https://github.com/khbminus/HSE-summaries).

Want to contribute and/or found a mistake? Follow the instructions below.

## Setup locally
- Clone the project: `git clone https://github.com/dmitrii-artuhov/HSE-summaries.git`
- [Install MiKTeX](https://miktex.org/download) (latex compiling toolchain).
- On Windows you need to install perl, you can install [strawberry perl](https://strawberryperl.com/).
- Install [VS Code](https://code.visualstudio.com/download) (I prefer it due to vast number of plugins) and plugin [Latex Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop).
- Follow the [link](https://youtu.be/4lyHIQl4VM8) to set up MiKTeX with the installed plugin.
- To compile the project you need to use `lualatex` compiler. To set it as a default compiler (so it is used automatically when you save the project) edit `setting.json` for the extension:
    ```json
    {
        "latex-workshop.latex.recipes": [
            {
                "name": "latexmk (lualatex)",
                "tools": [
                    "lualatexmk"
                ]
            },
            ...
        ]
    }
    ```
- Before compiling you also need to install some fonts in your system (donwload zip from [here](/fonts/Fonts.zip)). PS. If some fonts are missing inform me about it!
- Also you need to have [python](https://www.python.org/downloads/) installed.

## How to contribute
- Edit some latex code, keep the same folder structure, everything related to editing latex is self explanatory (see `/src` folder).
- Create PR with the amendmends, set its target to `master` branch.
- Before pushing, don't forget to run `python3 ./build.py` so the pdf files are generated and saved to `/pdf` folder.