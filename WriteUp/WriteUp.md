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

1.Make a new file named flag.txt and open the case program.  
![image](https://user-images.githubusercontent.com/74954683/165329362-8f6b1880-a164-4079-ae91-4b4460d9c8d1.png)  
2.Input any text in flag.txt.  
3.Get the pattern between the plaintext and key after been encrypted.  
![image](https://user-images.githubusercontent.com/74954683/165333077-24d7dccc-7004-4074-841a-e43c516b6ff3.png)  
4.Seperate the text in output.txt according to the pattern above.  
5.Make a new code to decrypt the text.  
![image](https://user-images.githubusercontent.com/74954683/165333452-0d7fc76a-6f67-4787-ad37-1151177f8ea8.png)  
6.Run the code and we get the flag.  

**FLAG:** anjay{symmetric_kind_of_encrypt}  

## Marsha and The Bear

**Description**  
Do you know what pyc is?  
**Case Program** [here](https://drive.google.com/file/d/1NCfal6WluGXGlytrVj1osxvCGFXZ2gyf/view?usp=sharing)   
**Solutions**   

1. Uncompyle file from .pyc to .py using uncompyle6 
![image](https://user-images.githubusercontent.com/74954683/177003255-615c3ea9-cf34-46f2-8e2c-94809f360a72.png)
2. Read and analyse the file 
3. Found a code with a sha256 type hash in the 'if' command and decompyle it
![image](https://user-images.githubusercontent.com/74954683/177003308-f1585749-f4c3-4eed-b8a6-ed6885c4488e.png)
4. Got the flag!
![image](https://user-images.githubusercontent.com/74954683/177003315-42354d15-08fc-407c-8fbb-ded5fe500554.png)

**FLAG:** anjay{73313}  

## Strop

**Description**  
stripped stropped, fligged flogged  
**Case Program** [here](https://drive.google.com/file/d/1lwPTVwr_-24IgRy7CtDy2CSbPPNh3aFF/view?usp=sharing)  
**Solutions**  

1. Check the file with 'strings' command
![image](https://user-images.githubusercontent.com/74954683/177003426-ea3bd48c-7d64-4365-b3b5-aabe89db282e.png)
2. Open IDA and found a function named 'sub_11E9'
![image](https://user-images.githubusercontent.com/74954683/177003440-a9947b12-0921-4acb-9d29-38d54e4d7590.png)
3. Found some ascii characters and rearrange according to the array
![image](https://user-images.githubusercontent.com/74954683/177003490-8aeb3b34-fcba-49d2-9a5c-1b9bd71a4c8b.png)
4. Found the flag!  
![image](https://user-images.githubusercontent.com/74954683/177003499-19886eaa-e719-4e00-aa27-43605c347a34.png)

**FLAG:** anjay{strip_sans}
