# Towers of Hanoi

An animated solution of the "Towers of Hanoi" puzzle with up to seven disks
for the HP-42S pocket calculator.

![](hanoi42s.gif)

Note: In the meantime, I've also implemented it for the SwissMicros DM42 as well
as for the HP-85, see further below.

## Installation

If you have a real HP-42S calculator, type in the program in `./src/hp42s-hanoi.txt`.
If you want to run it on [Free42](http://thomasokken.com/free42/), simply import
`./bin/hp42s-hanoi.raw`.

## Usage

 * XEQ "HANOI"
 * Enter the number of disks (1..7).
 * Press R/S.
 
After the puzzle is solved, press R/S for a restart.

## Implementation Notes

This puzzle has a nice recursive solution. However, for the implementation on a
pocket calculator, I decided to use an iterative approach. Refer to
[Wikipedia](https://en.wikipedia.org/wiki/Tower_of_Hanoi)
for some background information about this puzzle and the algorithms to solve it.

When running the program on Free42 you have to insert a pause at step 89, right
after the call to AGRAPH. Otherwise you will not see the disks moving around.
This is already done in the .raw file.

## Update - DM42 Version

I've now implemented a version for the
[SwissMicros DM42}(https://www.swissmicros.com/product/dm42), too.
It uses GrMod 2 (200x120 pixel) and handles up to 15 disks. Instead of
encoding the pile states in numbers, it uses a matrix. I've just adapted
the original HP-42S program so maybe the code is not very clean and optimized.

Usage is the same, just the program name changed and the maximum number of
disks is 15:

  * XEQ "HANOIX"
  * Enter the number of disks (1..15).
  * Press R/S.

![](dm42-hanoi.jpg)

## Update - HP-85 Version

I've now implemented a version for the HP-85. You can either type in the
program in `./src/hp85-hanoi.txt` or use Everet Kaser's great
[HP-85 emulator](https://www.kaser.com/hp85.html) and mount the disk image
`./bin/HP85-HANOI`.

Then, simply run the program, enter the number of disks (1..10) and enjoy.
Configure the emulator to run at natural (slower) speed, otherwise it runs too fast.

## References

I originally published this program on my HP calculator blog, see
[T&uuml;rme von Hanoi f&uuml;r HP-42S](http://calc.fjk.ch/turme-von-hanoi-fur-hp-42s/).
