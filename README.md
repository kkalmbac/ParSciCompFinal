DES requires 64 bits, 8 bytes
char is always one byte
strings are pretty much arrays of chars
Encryption is same as decryption with subkeys reversed
key is 64 bits, 8nth bit is error detection, odd parity required per byte

Initial Permutation
	potentially requires hard coding
	Since no cryptographic importance potentially ignorable
	Split into two 32 bit blocks
16 rounds
	left xor f(right) -> right
	right -> left
	f consists of
		expansion 32->48 bits, eight 6 bit pieces
			4 input, adjacent from left and right
		subkey xor expanded
		substitution (s-boxes)
		permutation
Final Permutation

key schedule
	56 bits selected
	two halves
	rotate left once or twice
	24 selected from permutation
	24 selected from left and right
	
Most permutations are most likely hard-coded
http://en.wikipedia.org/wiki/Data_Encryption_Standard
http://en.wikipedia.org/wiki/DES_supplementary_material
