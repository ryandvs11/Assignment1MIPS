# Assignment1MIPS
# MIPS PROJECT FOR DR LI, BY RYAN DAVIS
.data
    buffer: .space 20 # Reserves 20 Characters
    str1:  .asciiz "Enter string" # prompts user to enter a string

.text

main:
    la $a0, str1    # Load and print string
    li $v0, 4
    syscall

    li $v0, 10      # end program
    syscall
