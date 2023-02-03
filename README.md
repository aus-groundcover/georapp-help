# Introduction
This repository contains the Geoglam Rapp Help source files.

- The documentation website is statically generated from this repository using [MkDocs](https://www.mkdocs.org).
- Manually copy generated HTML files to the server at [https://eo-data.csiro.au/remotesensing/rapp-help](https://eo-data.csiro.au/remotesensing/rapp-help).

## Getting Started

1. Clone this repository
1. `mkdocs serve` will start a local server. Save your changes to the files and view them at the local link given.
1. Make a branch and PR to this repository
1. Once the PR is merged an admin will build and upload the updates to the hosting server.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

## Commands

* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

Full documentation:
- [mkdocs.org](https://www.mkdocs.org)
- [mkdocs-material](https://squidfunk.github.io/mkdocs-material/)

## Prerequisites
* Python3

Install the following using `pip install -r requirements.txt`:
* pygments (>=2.9.0)
* pymdown-extensions
* mkdocs
* mkdocs-material
