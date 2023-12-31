# AES 256

This code uses the OpenSSL library to create random keys and to encrypt a message as given by the user. 
The program will encrypt and then decrypt using the AES-256 encryption algorithm. You will notice that each time, despite the input being the same,
the ciphertext is different. The reason behind that is not only that the keys are randomly generated each time the program runs,
but it is also due to the initialisation vector being random as well.
This practice of keeping the IV random as well is used on production servers and where it is used, the IV is also transmitted with the ciphertext
in order for the recipient side to be able to decrypt the message.

A special note should go to the OPENSSL_cleanse(void *ptr, size_t len) function that is used in the main().
This OpenSSL function has several characteristics:<br>
			1. Overwrites memory (fills the memory the ptr is pointing to with the value 0).<br>
			2. Resistant to compiler optimizations (several compilers might optimize the code that clears memory out, thinking it is redundant; this resistance ensures the memory is indeed cleared).<br>
			3. Very beneficial when dealing with sensitive information where there's a risk of memory exposure.<br>
