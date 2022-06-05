# Build/Compile source code of this project

## Set up Developing Environment
Currently only support building x86 `TARGET` (32bit) (i386/80386 machine) with [GNU toolchain](https://www.gnu.org/software/software.html).

(Comment/Uncomment `TARGET` and 'host building machine'in Makefile for quick set up)

### Linux/[WSL2](https://docs.microsoft.com/en-us/windows/wsl/compare-versions)

- x86_64 host

  - install (Arch/Debian/Kali/Ubuntu)`nasm`, `gcc`, `binutils`, `gdb`

- aarch64 host

  - (Debian/Kali/Ubuntu) install `gcc-multilib-x86-64-linux-gnu` package (this will give you the compilers, binutils and debugger) and `nasm` as x86 assembler

### MacOS

- Apple Silicon Chips

  - use [Homebrew](https://brew.sh) install
    - for elf32-i386 target (32bit OS developing): `i686-elf-binutils`, `i686-elf-gcc`, `i386-elf-gdb` and `nasm`
    - for elf64-x86-64 target: `x86_64-elf-binutils`, `x86_64-elf-gcc`, `x86_64-elf-gdb` and `nasm`

  - the system `$PATH` should be set to `/opt/homebrew/bin` for Apple Silicon Mac

- Intel Chips

  - the system `$PATH` should be set to `/usr/local/bin` for Intel Mac