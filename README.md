[![Build Status](https://travis-ci.com/twlz0ne/nix-gccemacs-sierra.svg?branch=master)](https://travis-ci.com/twlz0ne/nix-gccemacs-sierra)

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

## Create symlink

``` sh
ln -snf $(nix path-info $(which emacs))/{lib/emacs/28.0.50/native-lisp,bin/native-lisp}
```

---

For macOS 10.15 or newer see [nix-gccemacs-darwin](https://github.com/twlz0ne/nix-gccemacs-darwin).
