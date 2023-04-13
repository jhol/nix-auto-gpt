# nix-auto-gpt


To manually load development environment for Auto-GPT, run:

> nix develop github:superherointj/nix-auto-gpt


Automatically loading dependencies is possible using [direnv](https://github.com/nix-community/nix-direnv). There is a [PR#1091](https://github.com/Torantulino/Auto-GPT/pull/1091) for it.

While that doesn't happen, you have to manually configure automatically loading dependencies:

  At Auto-GPT git repository:

  * Add `.envrc` file

    > echo '[[ -z $IN_NIX_SHELL ]] && use flake github:superherointj/nix-auto-gpt' > .envrc

  * Git ignore `.envrc` file

    > echo ".envrc" >> .git/info/exclude



This repository is licensed: MIT