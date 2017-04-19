# Towers of Hanoi

An animated solution of the "Towers of Hanoi" puzzle with up to seven disks
for the HP-42S pocket calculator.

![](hanoi42s.gif)

## Installation

If you have a real HP-42S calculator, type in the program in ./src/hp42s-hanoi.txt.
If you want to run it on [Free42](http://thomasokken.com/free42/), simply import
./bin/hp42s-hanoi.raw.

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

## References

I originally published this program on my HP calculator blog, see
[T&uuml;rme von Hanoi f&uuml;r HP-42S](http://calc.fjk.ch/turme-von-hanoi-fur-hp-42s/).
