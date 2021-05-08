[![CI](https://github.com/twlz0ne/nix-gccemacs-sierra/workflows/CI/badge.svg)](https://github.com/twlz0ne/nix-gccemacs-sierra/actions?query=workflow%3ACI)

# nix-gccemacs-sierra

Build gccemacs for macOS 10.12 Sierra using Nix.

## Installation

- Build on local machine

    ``` sh
    git clone https://github.com/twlz0ne/nix-gccemacs-sierra
    cd nix-gccemacs-sierra && nix-env -iA emacsGccSierra
    ```

- Pull pre-built binaries from Cachix (recommend)

    ``` sh
    nix-env -iA cachix -f https://cachix.org/api/v1/install
    cachix use gccemacs-sierra
    nix-env -iA emacsGccSierra -f https://github.com/twlz0ne/nix-gccemacs-sierra/archive/master.zip
    ```

For macOS 10.15 or newer see [nix-gccemacs-darwin](https://github.com/twlz0ne/nix-gccemacs-darwin).
