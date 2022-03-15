# Bitwise operator

## & AND
Sets each bit to 1 if both bits are 1
`5 & 1 = 1 (0101 & 0001 = 0001)`

## | OR
Sets each bit to 1 if one of two bits is 1
`5 | 2 = 7 (0101 & 0010 = 0111)`

## ^ XOR
Sets each bit to 1 if only one of two bits is 1
`5 ^ 1 = 4 (0101 ^ 0001 = 0100)`

## ~ NOT
Inverts all the bits
`~ 5 = 10 (~0101 = 1010)`

## << Zero fill left shift
Shifts left by pushing zeros in from the right and let the leftmost bits fall off
`5 << 1 = 10 (0101 << 1 = 01010)`

## >> Signed right shift
Shifts right by pushing copies of the leftmost bit in from the left, and let the rightmost bits fall off
`5 >> 1 = 2 (0101 >> 1 = 0010)`

## >>> Zero fill right shift
Shifts right by pushing zeros in from the left, and let the rightmost bits fall off
`5 >>> 1 = 2 (0101 >>> 1 = 0010)xs`