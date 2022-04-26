# CTF Write Up 1


| No | Case Title                     | Category              | Flag              
|----|--------------------------------|-----------------------|-----------------------------------------
| 1. | Etpenced Enkripsen System      | Cryptography          | anjay{symmetric_kind_of_encrypt}
| 2. | Marsha and The Bear            | Reverse Engineering   | anjay{73313}
| 3. | Strop                          | Reverse Engineering   | anjay{strip_sans}

## Etpenced Enkripsen System

**Description**  
sistem sistem apa yang encryptionnya advanced?  
**Case Program** [here](https://drive.google.com/file/d/1qwj0zfJ2rtYAyqBBeJ8_rRjIYaHuMZcQ/view?usp=sharing)  
**Output.txt:** 7f58d3bc1a17c6288f50aa52489c326fc2eb0abc76d010879abc6cc0153c24863051b11aa49ab82efed1f2b85e327bbe  
**Solutions**  
1. Make a new file named flag.txt and open the case program.  
![image](https://user-images.githubusercontent.com/74954683/165329362-8f6b1880-a164-4079-ae91-4b4460d9c8d1.png)  
2. input any text in flag.txt.  
3. Get the pattern between the plaintext and key after been encrypted.  
![image](https://user-images.githubusercontent.com/74954683/165333077-24d7dccc-7004-4074-841a-e43c516b6ff3.png)  
4. Seperate the text in output.txt according to the pattern above.
5. Make a new code to decrypt the text.  
![image](https://user-images.githubusercontent.com/74954683/165333452-0d7fc76a-6f67-4787-ad37-1151177f8ea8.png)  
6. run the code and we get the flag.  

**FLAG:** anjay{symmetric_kind_of_encrypt}  

