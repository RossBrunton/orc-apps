# multiplyConstant Actor #
For each octet in the data stream, multiplies it by a factor and then divides it by a divisor.

## Inputs ##
* **uint(size=8) Gin**: The stream to read values from.

## Outputs ##
* **uint(size=8) Gout**: The stream to write translated values out to.

## Usage ##
Inside this actor are two constants; `factor` and `divisor`. For each 8 bit value `x` read from `Gin`, `x * (factor / divisor)` will be written to `Gout` in the same order.

For each value, if the multiplication would result in an overflow, `255` is output instead.

## Notes ##
None.
