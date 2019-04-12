# Factorio Planner

Factorio Planner helps you plan your factories by computing how many
resources and machines you need to produce a given throughput of
resources. Try it here: http://doomeer.com/factorio

## Architecture

Factorio Planner is written in OCaml, but is then compiled to Javascript
using js_of_ocaml.

* `index.html` is the HTML page which loads the Javascript.
* `factorio.js` is the Javascript compiled from the OCaml code.
  It is included in the repository in case you don't want to compile it.
* `factoriojs.ml` is the main file, which implements the Web interface.
* `factorio.ml` contains type definitions and the code to compute
  ressource summaries.
* `recipes.ml` contains maker and ressource definitions.
  This is the file you want to modify to change ingredients or add
  new ressources.
* `html.mli` is the interface to `html.ml`, which provides helpers
  for Web interfaces.

## Install OCaml

To compile Factorio Planner you need to install the OCaml compiler
as well as js_of_ocaml.

### Debian or Ubuntu:

    sudo apt-get install ocaml ocaml-findlib camlp4 js-of-ocaml

Alternatively, you can use OPAM (OCaml Package Manager, https://opam.ocaml.org):

    sudo apt-get install opam
    opam init
    opam switch 4.03.0
    opam install js_of_ocaml

### Windows:

Download OCaml for Windows here: https://fdopen.github.io/opam-repository-mingw/installation
Open the OCaml terminal that the installation produces and run the following:

    opam init
    opam switch 4.03.0
    opam install js_of_ocaml

## Compile Factorio Planner

Just run:

    make

This will compile the project and regenerate `factorio.js`.

## License

Factorio Planner is released under the MIT license.
See the `LICENSE` file.

The images included are extracted from the official Factorio Wiki (see: https://wiki.factorio.com)
released and also distributed here under the Creative Commons BY-NC-SA 3.0 License, see https://creativecommons.org/licenses/by-nc-sa/3.0/.
