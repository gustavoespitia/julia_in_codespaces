# Running Julia in Github Codespaces

This is a simple setup to run Julia on Github Codespaces just as a reminder for myself, maybe it will be useful for someone else. Notice this procedure follows the Julia (Community) template.

First go to repository you want to run in Codespaces, for example https://github.com/gisel-uninorte/SimpleDistributionPowerFlow.jl

On the green box (<> Code), select Codespaces and clic in plus (+) sign to add a new codespaces

When the Codespace is running for the first time, add a file folder with the name .devcontainer at top of folder structure and copy the devcontainer.json file that you find in this repository.

devcontainer.json is a plain file with this instruction:
      {
      	"name": "Julia (Community)",
      	"image": "ghcr.io/julia-vscode/julia-devcontainer",
      	"extensions": ["julialang.language-julia"],
      	"postCreateCommand": "/julia-devcontainer-scripts/postcreate.jl",
      	"remoteUser": "vscode"
      }

Restart Codespaces (clic on alert notice or simple reload the page)

When restart precedures finished, press Cntrl-Shift-P and execute Julia Start REPL (or simply press Alt-J Alt-O)

To use the selected package issue the Julia using command, per example:
julia> using SimpleDistributionPowerFlow

To know the version of Julia, issue the bash command: julia -version
