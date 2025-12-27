# cboy

An experimental GameBoy emulator written in C for educational purposes. It emulates the hardware, like the LR35902 CPU with its instruction set, MMU, and Display where the rendering is done with OpenGL, and you can play with your keyboard or joystick. Saving is now possible by storing the whole emulation state (CPU registers and memory), so you can immediately continue where you left off.

## Screenshots

![mario_land](images/screenshot1.png)
![pokemon_green](images/screenshot2.png)

## Building

```bash
git clone https://github.com/veeso/cboy-lego.git && cd cboy-lego
mkdir build && cd build
cmake -DRENDERER=FRAMEBUFFER -DCMAKE_EXE_LINKER_FLAGS="-latomic" ..
make
```

## Usage

```bash
export FRAMEBUFFER=/dev/fb1
./cboy <rom>
```

## Controls

| Key   | Keyboard    |
|-------|:-----------:|
|Up     | Up          |
|Down   | Down        |
|Left   | Left        |
|Right  | Right       |
|A      | A           |
|B      | S           |
|Start  | Q           |
|Select | W           |

## Framebuffer output instead OpenGL
