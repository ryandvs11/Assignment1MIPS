# Assignment1MIPS
# MIPS PROJECT FOR DR LI, BY RYAN DAVIS
.data
    message:  .asciiz "Enter string"
    userInput: .space 8

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

    #Displays Name
    li $v0, 4
    la $a0, userInput
    syscall
    
    # end program
    li $v0, 10      
    syscall
