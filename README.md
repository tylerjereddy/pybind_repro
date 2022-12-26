# How to reproduce the bug with pybind11 2.10.2

- Use Windows mingw toolchain (I use the popular "Git for Windows"
program/terminal and setup a Python 3.10 virtualenv)
- `meson setup builddir`
- `cd builddir`
- `ninja`
- `python -c "import pypocketfft"` (error with `2.10.2` and not `2.10.1`)
