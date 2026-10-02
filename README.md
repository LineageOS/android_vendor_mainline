# Android vendor tree for devices with mainline kernel

This repository is mostly for holding components which relies on modules that
has `visibility` limitation that contains `//vendor:__subpackages__` whitelist.

Before adding a new component here, consider if it can be added into
`device/mainline/common` repository instead.

To see how all the mainline repositories relate, read
[docs/REPOSITORIES.md](docs/REPOSITORIES.md).

The `generic_init` init program is documented in
[services/generic_init/docs/](services/generic_init/docs/README.md).
