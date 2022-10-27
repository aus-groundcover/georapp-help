# Introduction
This repository contains the Geoglam Rapp Help source files. The documentation website is statically generated from this repository using [mkdocs.org](https://www.mkdocs.org).

Manually copy generated HTML files to {lw-lpdaac}/work/fc-wron/data/public/RaPP_Help, which is mounted publically at https://eo-data.csiro.au/remotesensing/RaPP_Help.

# Getting Started
Prerequisites:
* Python

Install the following using `pip install -r requirements.txt`:
* pygments (>=2.9.0)
* pymdown-extensions
* mkdocs
* mkdocs-material

For full documentation visit:
  * [mkdocs.org](https://www.mkdocs.org)
  * [mkdocs-material](https://squidfunk.github.io/mkdocs-material/)

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.
