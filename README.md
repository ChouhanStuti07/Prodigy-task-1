# Prodigy-task-1
IMPLEMENTATION OF CAESER CIPHER FOR ENCRYPTION AND DECRYPTION 
1.	caesar_cipher(text, shift, mode) function:
o	Takes three arguments: text (the message), shift (the number of positions to shift letters), and mode ('encrypt' or 'decrypt').
o	Initializes an empty string result to store the output.
o	If the mode is 'decrypt', it negates the shift value to reverse the encryption.
o	It iterates through each character (char) in the input text.
o	Inside the loop:
	It checks if the character is an alphabet letter using char.isalpha().
	If it's a letter, it determines the starting ASCII value (start) based on whether it's lowercase ('a') or uppercase ('A').
	It calculates the shifted_char by:
	Getting the ASCII value of the character (ord(char)).
	Subtracting the start value to get a 0-based index (0-25).
	Adding the shift value.
	Using the modulo operator (% 26) to wrap around the alphabet (e.g., shifting 'z' by 1 goes back to 'a').
	Adding the start value back to get the ASCII value of the shifted character.
	Converting the ASCII value back to a character using chr().
	The shifted_char is appended to the result.
	If the character is not a letter (e.g., space, punctuation), it's added to the result without modification.
o	Finally, the function returns the result string.
2.	User Input:
o	The code prompts the user to enter the message, the shift value, and the mode ('encrypt' or 'decrypt').
3.	Mode Validation and Output:
o	It checks if the entered mode is valid.
o	If the mode is valid, it calls the caesar_cipher function with the user's input and prints the resulting encrypted or decrypted text.
o	If the mode is invalid, it prints an error message.
