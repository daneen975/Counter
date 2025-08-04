Linked Counters - Lab 3

COE318: Object-Oriented Programming

Overview
This Java program implements a positional number system using linked Counter objects, where each digit is a separate object that may be linked to a "left neighbor" digit. The counters work together to represent numbers in an arbitrary base, and simulate the behavior of counting systems like base-4, base-10, etc.

This lab focuses on practicing object linking, using conditionals, and understanding recursive or chained behavior in objects.

Project Files
- Counter.java: Represents a single digit in the number system. Can link to a left neighbor to represent higher-order digits.
- CounterTry.java: A driver class that demonstrates the use of linked counters.

How It Works
Each Counter object:
- Holds a modulus (e.g., base 10 means modulus = 10)
- Holds its own current digit value
- Optionally holds a reference to a left neighbor Counter
- When increment() is called:
  - The digit increases by one
  - If it overflows (equals the modulus), it resets to zero
  - If it has a left neighbor, that neighbor is incremented recursively

The getCount() method returns the full number the Counter represents by combining the digits using positional math.
