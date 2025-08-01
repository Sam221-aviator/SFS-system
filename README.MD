# Sam Linux From Scratch(SFS)

This system is a custom kernel build system like Minix, Unix or Linux. This kernel is just for fun not for productions. The oringinal code is by nanobyte_os or nanobyte. I use his code to make this kernel. If you want something to be added in our linux distro variants, contact ust at mmbk88221@gmail.com

## Running

Run this command in your terminal
```bash
make
```

After running the command, you will see this in your terminal.

```bash
mkdir -p build
nasm src/main.asm -f bin -o build/main.bin
cp build/main.bin build/main_floppy.iso
truncate -s 1440k build/main_floppy.iso
```

To run the operating system, run this command.

```bash
qemu-system-i386 -fda build/main_floppy.iso
```
