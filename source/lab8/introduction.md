# Introduction

In this lab, we will look at how two voltages levels can be used to perform
arithmetic. By utilizing just two voltage levels, a "high" and a "low", we
create a binary system. The binary system is "a language" used to create
mathematical formulas, such as algebraic equations, but also logical
expressions. This branch of mathematics is called Boolean algebra, introduced
by George Boole, in which the values of the variables are either "true" or
"false" (also called "high" or "low"; "1" or "0"). The various terms for the
two states will be used interchangeably. The implementation of Boolean algebra
with circuitry and programming is called digital logic. Boolean algebra is
basis for the development of digital electronics.

In this lab we will build a one-bit full-adder, which adds three data bits,
which include data bits $x$ and $y$, and a carry bit $z$. The output of the
adder will be a one-bit result and a one-bit carry.

Note: The name "full-adder" comes from the fact that it can be constructed by
combining two half-adders, each of which adds only two bits.
