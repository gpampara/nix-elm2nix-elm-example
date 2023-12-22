# Nix + Elm + elm2Nix + npm project example

This is a sample project to show how nix, Elm and npm can be used
together for both local development and to build a derivation of the
project itself.

# Prerequistites

Importantly, the elm and the npm data needs to be updated when either
the `elm.json` or `package.json` (and therefore the
`package-lock.json` after running `npm install`) files change. A `npm`
script has been added to automate the update process for Elm
dependency changes. For the time being, the `npm` dependency changes
require running `prefetch-npm-deps package-lock.json` and then
updating the hash in `npmDeps.nix`.

The `prefetch-npm-deps` will be automated in a subsequent update to
this example project.
