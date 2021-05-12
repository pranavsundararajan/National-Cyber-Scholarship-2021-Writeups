# CH01 (500 pts)

## Description
Download the files and find a way to retrieve the encrypted data.

## Approach
When we unzip the [file](ch01.zip), we get 2 public keys and 2 encrypted files (which are the ciphertexts), so we can assume this is going to be RSA. I used RSACtfTool for this since it has a lot of functionality; here's the command I used to obtain the modulus and exponent for the public keys.

