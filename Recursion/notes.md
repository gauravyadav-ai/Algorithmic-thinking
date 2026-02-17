NOTES- 
Recursion is not about function calls.
Recursion is about breaking a problem into smaller identical problems.

Every recursive solution has:
1-State (what changes?)
2-Choice (what options do I have?)
3-Base Case (when do I stop?)
If one is missing → infinite recursion.

If you want to truly "get" recursion, you need a problem that is simple enough to hold in your head but complex enough to show why the Call Stack matters.

Tower of Hanoi
It is the gold standard for visualizing Tree Recursion, where one function call triggers multiple new branches


You have 3 rods (Source, Auxiliary, Target) and n disks of different sizes.
Goal: Move all disks from Source to Target.
Rule 1: Only one disk can be moved at a time.
Rule 2: A larger disk can never be placed on top of a smaller disk.

The Recursive Logic
To move n disks, the logic is deceptively simple:
Move n−1 disks from Source to Auxiliary.
Move the nth (largest) disk from Source to Target.
Move the n−1 disks from Auxiliary to Target.

The Golden Rule (LOCK THIS IN)
Trust the function to solve the smaller problem.
Do not think about the full problem inside the function.
​​This is the "Mental Shift." If you try to trace every step of recursion in your head, you will get lost. To master recursion, you have to be comfortable with not knowing exactly what happens inside the "black box."


