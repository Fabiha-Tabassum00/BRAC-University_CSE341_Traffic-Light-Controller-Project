# Microprocessors — Traffic Light Controller (8086 Assembly)

A traffic-light control system for a four-way intersection, written in **x86 (8086) assembly** and built as the project for a Microprocessors course. It runs in a DOS environment using BIOS/DOS interrupts (`INT 21H`) for keyboard input and screen output.

## Skills Demonstrated

- **8086 assembly programming** — `.MODEL SMALL` structure, data and code segments, registers, and the stack
- **DOS interrupts** — character input (`AH=1`), string output (`AH=9`), and program termination (`AH=4C00H`) via `INT 21H`
- **Control flow** — conditional jumps (`CMP`/`JE`), labels, and `LOOP`-based timed cycles with `CX` counters
- **Procedures** — reusable subroutines with `CALL`/`RET` for display, delay, and formatting
- **Input validation** — rejecting invalid keypresses and re-prompting the user

## The Intersection

The system manages four directions — **North-West, South-East, East-North, West-South** — assigning each a Green, Yellow, or Red state so that only one direction flows at a time while the others are held.

## Features

1. **Traffic light control** — the user selects which direction gets the green light (types 1–4); the program validates the input and re-prompts on anything invalid.
2. **Current light status display** — prints the Red/Yellow/Green state of all four directions for the selected configuration.
3. **Timed light cycles** — an automated sequence that holds Green for 10 counts, Yellow for 5, and Red for 10, using `LOOP` counters to simulate signal timing.
4. **Manual override for pedestrians** — an override mode where pressing `2` sets all lights red (stop) and `0` sets all lights green, for pedestrian crossing control.

## Building & Running

This program targets the 8086 and DOS. Run it with an assembler and emulator such as **emu8086** or **DOSBox with TASM/MASM**:

1. Open `Project.asm` in emu8086 (or assemble with TASM/MASM under DOSBox).
2. Assemble and link.
3. Run the executable and follow the on-screen prompts to select a direction, watch the timed cycle, and try the manual override.

## Author

**Fabiha Tabassum Poroma**