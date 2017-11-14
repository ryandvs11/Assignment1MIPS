.data
    message:  .asciiz "Enter string"
    userInput: .space 8
    loop: 

.text

main:

    
    # Shows Message
    li $v0, 4
    la $a0, message
    syscall

    # Get User Input
    li $v0, 8 
    la $a0, userInput 
    li $a1, 8
    syscall

    
    beq 
    addi $t0, $zero, 0
    addi $t1, $zero, 9
    slt, $s0, $t0, $t1
    syscall

    li $v0, 4
    la $a0, userInput
    syscall

    li $v0, 10      # end program
    syscall
