# Assembly 'Hello World'

## Setup And Execution

Make sure you have NASM installed. For example on Ubuntu:
```apt install nasm```

To assemble .asm script into object file run:
```nasm -f elf32 -o helloworld.o helloworld.asm```

To create an executable file:
```ld -m elf_i386 -o helloworld helloworld.o```

Run:
```./helloworld```

This will print ```Hello World!```.

## Attribution

This tutorial was originally found on [John Hammond's](https://github.com/JohnHammond) [YouTube channel](https://www.youtube.com/c/JohnHammond010)
