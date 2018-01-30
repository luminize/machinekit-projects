# Machinekit Projects

The aim of this repository is to bring order in the
Machinekit project by gatherering issues and (ongoing)
(sub) projects.

This repo *will* contain different files written in Asciidoc
so that generating documents and visualising diagrams can
be done in an easy way.

Tools:
- Asciidoctor
- Asciidoctor-diagram
- Asciidoctor-pdf
- IDE with proper Asciidoctor preview capabilities.

This repo _will not_ contain code, nor will it be a substitute
for the Machinekit documentation.

## Installation

### Debian installation with ruby 2.3.3

```bash
sudo apt-get install graphviz
gem install asciidoctor
gem install asciidoctor-diagram
gem install asciidoctor-pdf --pre

```

### Windows installation

- install ruby 2.3.3
- install graphviz

then open console or powershell
```
gem install asciidoctor
gem install asciidoctor-diagram
gem install asciidoctor-pdf --pre
```

- make sure the binary locations of ruby and graphviz are added to your PATH

## IDE's (to be extended)

### Microsoft Visual Code

One of such is Microsoft Visual Code, where the Asciidoctor
plugin can generate correct output in a live preview window.
This IDE is not mandatory, but has proven to work quite well
with writing these documents.

- Install [https://code.visualstudio.com](Microsoft Visual Code)
- Install the [https://marketplace.visualstudio.com/items?itemName=joaompinto.asciidoctor-vscode ](Asciidoc plugin)
- Reload
- Preferences -> Settings
- search for "asciidoc"
- copy the `"AsciiDoc.html_generator": "asciidoctor -o-",` setting to your User Settings (right pane)
- change that to `"AsciiDoc.html_generator": "asciidoctor -r asciidoctor-diagram -o-"`

Now write some asciidoc with a diagram (For example plantUML)
then `CTRL + K` and after that `R` will show the Asciidoctor output in the right pane.

## Generating a PDF:

Generating pdf files is done by:
`asciidoctor-pdf -r asciidoctor-diagram yourfile.adoc`