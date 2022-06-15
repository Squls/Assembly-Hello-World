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

## Explanation

### Registers


| 32-bit | 64-bit | Name        | Use                                              |
|--------|--------|-------------|--------------------------------------------------|
| eax    | rax    | Accumulator | For I/O port access, arithmetic, interrupt calls |
| ebx    | rbx    | Base        | As a base pointer for memory access              |
| ecx    | rcx    | Counter     | As a loop counter and for shifts                 |
| edx    | rdx    | Data	| for I/O port access, arithmetic, some interrupt  |

More on registers on [Wikipedia](https://en.wikipedia.org/wiki/X86#32-bit)

### Commands

#### mov

Moves data between registers the first is the destination and the second specifies the source. For example in our script on line 10 we are moving the contents of message into the ecx register:

```mov ecx, message```

#### int

Interrupt

## Attribution

The basis for this guide was originally found on [John Hammond's](https://github.com/JohnHammond) [YouTube channel](https://www.youtube.com/c/JohnHammond010)
