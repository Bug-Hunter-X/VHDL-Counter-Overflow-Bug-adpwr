# VHDL Counter Overflow Bug
This repository demonstrates a common bug in VHDL counters and its solution. The `buggy_counter.vhdl` file contains a counter that has a potential overflow problem.  The `fixed_counter.vhdl` demonstrates a corrected version.

## Bug Description
The buggy counter uses an integer type and does not properly handle the case when the counter reaches its maximum value (15).  The current implementation, while seemingly correct, can lead to unexpected behavior or simulation errors depending on the synthesizer or simulator. 

## Solution
The solution involves ensuring that the assignment to `internal_count` within the `if internal_count = 15 then` block is handled correctly to avoid potential issues. The corrected version is implemented in `fixed_counter.vhdl`