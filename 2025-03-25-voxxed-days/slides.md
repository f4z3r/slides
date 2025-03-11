---
title: I use NixOS btw...
sub_title: Learnings from 2 years daily driving NixOS
options:
  implicit_slide_ends: true
theme:
  path: ../assets/presenterm/theme.yaml
---

Nix Trinity
===

![Nix Trinity](./assets/nix-trinity.png)

<!--
speaker_note: |
  2 MINUTES

  Extend to 4 minutes with intro story?

  Nix Lang:
  - ...
  Nix Pkgs:
  - ...
  NixOS:
  - ...
-->

Nix Language
===

# Expressions

```nix +line_numbers
let
  x = 1;
in
  {
    a = {
      b = true;
    };
    d.e.f = "hello";
    y = x;
    config = builtins.readFile ./config.ini;
  }
```

<!--
speaker_note: |
  1 MINUTES (3)
-->

Nix Language
===

# Derivations

```nix {1-17|1|2-3|5-10|9|12-14} +line_numbers
rustPlatform.buildRustPackage rec {
  pname = "presenterm";
  version = "0.10.1";

  src = fetchFromGitHub {
    owner = "mfontanini";
    repo = "presenterm";
    tag = "v${version}";
    hash = "sha256-...06HsX28mLvTrWh5yIbo/a54M=";
  };

  buildInputs = [
    libsixel
  ];

  # ...
}
```

<!--
speaker_note: |
  2 MINUTES (5)
-->

Nix Package Manager
===

# Nix Store

``` +line_numbers
/nix/store/sm724q6cyqwwghbadxssw9v2xyns56yn-python3-3.11.9
/nix/store/zr51xbkmmkflpp1nm433vfgpkndhp64d-python3-3.11.9
```

# Package Registry

![nixpkgs](./assets/nixpkgs.png)

<!--
speaker_note: |
  1 MINUTES (6)
-->

Demo
===

# Nix REPL
## Loading Package Registry
## Exploration
## Building Packages
### Python with Various Dependencies
## Running Stuff

<!--
speaker_note: |
  5 MINUTES (11)

  nix repl

  :l <nixpkgs>
  <nixpkgs> # compare with channels/registry
  python3
  python3.withPackages # function
  python3.withPackages (p: [p.numpy])
  python3.withPackages (p: [p.jupyter])
  :b python3.withPackages (p: [p.numpy])

  Execute the binary and check imports ...
-->

NixOS
===

![nixos](./assets/neofetch.png)

<!-- newlines: 2 -->

<!-- column_layout: [1, 1] -->

<!-- column: 0 -->
- Entire OS managed by Nix
- Fully reproducible
- Only data not replicated

<!-- column: 1 -->
> https://github.com/f4z3r/nix

<!-- reset_layout -->

<!--
speaker_note: |
  2 MINUTES (13)
-->

Use Cases
===

## Dev Environments

- Pin tooling
- Ensure consistency
- Use abstractions: [DevBox](https://www.jetify.com/devbox)

## CI/CD

- Define pipelines as code
- Run locally

## Fleet Management

- Server management
- Replacement for pre-built ISOs / Packer

<!--
speaker_note: |
  3 MINUTES (16)

  Questions: 1-2 MINUTES
-->

<!-- vim:tw=60
-->
