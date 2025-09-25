1. Analog (continuous) - all real life phys values
![[analog_signal.excalidraw]]
2. Digital (numbers - less errors than analog)
	- low voltage (0V) -> $0_{(2)}$
	- high voltage (3.3V, 5V) -> $1_{(2)}$

# ADC:
![[analog_signal_conversion.excalidraw]]
1. Sampling
2. Quantization (depends on bit depth)
	2 bits -> 4 lvls ($2^2$)
3. Encoding

analog never != digital

# Number systems
### every number system has:
1. base (radix)
2. set of digits
3. positional value ($digit * base^{position}$)


- Decimal (0-9)
- Binary(0, 1)
	bit - 0/1
	byte = 8 bits
	nibble = 4 bits
	word = 16 bits

	**n bits can represent $2^n$ states**
	**$2^8$ = 256 states**
- Octal (0-7) *e.g. Unix for permissions*
- Hexadecimal (0-9 && A-F) *color codes \#ff00ff, mac address*
	1 hex digit = 4 bits