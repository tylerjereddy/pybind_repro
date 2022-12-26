project('test', 'cpp')

py_mod = import('python')
py3 = py_mod.find_installation(pure: false)
py3_dep = py3.dependency()
incdir_pybind11 = run_command(py3,
  [
    '-c',
    'import pybind11; print(pybind11.get_include())'
  ],
  check: true
).stdout().strip()
inc_pybind11 = include_directories(incdir_pybind11)

pocketfft_threads = ['-DPOCKETFFT_NO_MULTITHREADING']
py3.extension_module('pypocketfft',
  'pypocketfft.cxx',
  cpp_args: pocketfft_threads,
  include_directories: inc_pybind11,
  install: true,
)
