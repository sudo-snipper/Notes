## encrypt

We can encrypt a file using GnuPG (GPG) using the following command:

```
gpg --symmetric --cipher-algo CIPHER message.txt
```

where CIPHER is the name of the encryption algorithm. You can check supported ciphers using the command
`gpg --version`.
The encrypted file will be saved as 
`message.txt.gpg`



The default output is in the binary OpenPGP format; however, if you prefer to create an ASCII armoured output, which can be opened in any text editor, you should add the option --armor. For example, 
```
gpg --armor --symmetric --cipher-algo CIPHER message.txt.
```


## decrypt 

You can decrypt using the following command:

```
gpg --output original_message.txt --decrypt message.gpg
```