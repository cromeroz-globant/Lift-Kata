Lift Kata
==========

This repo has a starting position for doing the Lift Kata with an Approval testing approach. It includes a printer which
can print a lift system using ASCII art. There is only enough of an implementation to support this. Your job is to 
implement the rest of the software, so the lifts can move.

Understanding the ASCII Art
----------------------------

This is a sample printout from the lift printer:

	3     [A]                3
	2          [B]  ]C[      2
	1 v                      1
	0      *            [*D] 0

This information may help you to understand it:

- Each line corresponds to a floor. There are four floors numbered 0,1,2,3.
- There are four lifts, named 'A', 'B', 'C', 'D', each in its own column.
- There is a call on floor 1 to go down, which is marked with a 'v'.
- Lift 'C' has the doors open, the others all have their doors closed.
- Lift 'A' has a request for floor 0, which is marked with a *.
- Lift 'D' has a request for floor 0, and it is also on floor 0 with the doors closed.


Lift Kata Description
---------------------

Since lifts are everywhere, and they contain software, how easy would it be to write a basic one? Let's TDD a lift, 
starting with simple behaviors and working toward complex ones. Assume good input from calling code and concentrate on 
the main flow.

Lift features:

- A lift moves between a number of floors.
- A lift has a panel of buttons passengers can press to `request` floors.
- People can call the lift from other floors. A `call` has both, a floor and a desired direction.
- A lift has doors which may be open or closed.

In this repository, that much is already implemented. The following features aren't implemented:

- A lift fulfills a `request` when it moves to the requested floor and opens the doors.
- A lift fulfills a `call` when it moves to the correct floor, is about to go in the called direction, and opens the 
doors.
- A lift can only move between floors with the doors closed.

Lifts do not respond immediately or do everything at once. To simplify handling time in this exercise, the provided 
`LiftSystem` class has a `tick` method. Every time you call it, the lift system should simulate a unit of time passing, 
and update its state according to what changes occurred during that time period. `Lift`s can move between floors or open
their doors for example.

To simplify things, Lifts only accept new calls and requests when they are on a floor. (Then we don't have to model what
happens when they are between floors).

The starting code has a `Lift` class with basic attributes like a floor, requests and doors. Can you build on this code
and create something that fulfills all the desired features? Consider Object-Oriented design principles. Can you make 
`Lift` and `LiftSystem` into a well-designed encapsulated objects? 

Acknowledgements
----------------
This is a simplified Java version from [Emily Bache's](https://github.com/emilybache/Lift-Kata) original approach to the
Lift Kata, as described at https://kata-log.rocks/lift-kata

This project uses [Floobits](https://floobits.com)
[![Floobits Status](https://floobits.com/cromeroz-globant/Lift-Kata.svg)](https://floobits.com/cromeroz-globant/Lift-Kata/redirect)