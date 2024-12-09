# VHDL Counter with Potential Overflow

This repository demonstrates a common error in VHDL code: improper handling of integer overflow in a counter.

The `buggy_counter.vhdl` file contains a counter that might overflow without proper checks, which can result in unpredictable behavior.

The `fixed_counter.vhdl` provides a corrected version, adding checks to prevent overflows and ensuring reliable operation.

## How to Reproduce the Bug

1. Synthesize or simulate `buggy_counter.vhdl`.
2. Observe the counter behavior when it reaches its maximum value (15).
3. Compare it to the behavior of `fixed_counter.vhdl`.

## Understanding the Fix

The fix in `fixed_counter.vhdl` involves using a `unsigned` type instead of an integer for better overflow behavior. This prevents undefined behavior and ensures the counter wraps around predictably.