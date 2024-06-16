# Implement-Caesar-Cipher
Caesar Cipher in Python is an easy method to encrypt your message. Letter in a plain given text is changed to a letter that appears a certain number of positions farther down the alphabet. Decrypt key shows the number that how many times letters were shifted during encryption.
Author - Anurag Shrivastav
#A python program to illustrate Caesar Cipher Technique
def encrypt(text,s):
	result = ""

	# traverse text
	for i in range(len(text)):
		char = text[i]

		# Encrypt uppercase characters
		if (char.isupper()):
			result += chr((ord(char) + s-65) % 26 + 65)

		# Encrypt lowercase characters
		else:
			result += chr((ord(char) + s - 97) % 26 + 97)

	return result

#check the above function
text = "ATTACKATONCE"
s = 4
print ("Text : " + text)
print ("Shift : " + str(s))
print ("Cipher: " + encrypt(text,s))
