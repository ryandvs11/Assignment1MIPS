# Assignment1MIPS
MIPS PROJECT FOR DR LI, BY RYAN DAVIS
# PROGRAM: Hello, World!
	.data # Data declaration section
	out_string: .asciiz "\nEnter a String!\n"
	.text # Assembly language instructions
main: 
	li $v0, 4 # system call code for printing string = 4
	la $a0, out_string # load address of string
# to be printed into $a0
	syscall # call operating system to perform operation
# in $v0
# syscall takes its arguments from $a0, $a1, ...
	li $v0, 10
syscall # Exit program
