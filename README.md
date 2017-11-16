.data
    buffer: .space 9 # Reserves 8 Characters
    message:  .asciiz "Enter string"
    userInput: .space 8
  
.text
  
main:
     # Get User Input
     li $v0, 8 
     la $a0, userInput 
     li $a1, 8
      syscall
  
     li $v0, 10      # end program
     #Displays Name
     li $v0, 4
     la $a0, userInput
     syscall
     
     # end program
     li $v0, 10      
      syscall
