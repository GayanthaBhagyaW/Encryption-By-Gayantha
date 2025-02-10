This is a credential encryption program written using Python, with following libraries
pip install pycryptodome pandas pyperclip
The prgram is using "PBKDF2" method with a "defined-key" ( such as a passsword) we call it the "Master key" which is a unique key around 32 Bytes (256 bit) as a requirement for AES encryption
to prevent patterns and make the Encryption Key unique , We then create a random 16 byte key which we call IV (Initialization Vector)
Program then encrypts the Data using AES in CFB mode using key derived using MasterKey + IV
the result encrypted output of the above is saved as Base64 format in a Text file to be able to retrive later

Benifits of this program,
- avoiding using Keyrings
- no encryption information saved on the system
  
