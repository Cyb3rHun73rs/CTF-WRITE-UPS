## Challenge name: Scissors
### Category: MISC

![Screenshot 2025-05-03 222736](https://github.com/user-attachments/assets/16582165-6e2f-4919-9987-d887d671e6d4)

This challenge involved decoding ciphers. This site https://www.dcode.fr/cipher-identifier is very helpful for identifying and decoding ciphers.

The first cipher: `EGWYA4qbONIz4vTkzmuauKMKvTCtIzUQgvlZnuiLxhlJdDwabCgs1ENbk4GRw1XICC4YjcnyS1QaMTz1w7k07WUeM4DoxT7EqJUeTltnHM20K30ypav9t3Bi9AH5ok6kctrc77F53VFiOZ2OInsfIRPsZzQ1OIxl6fdRbD7ezDZaz0LxVbJ12WEqd4Fi0Iv5FPLOKvn3sKN875e3Tv8h9fm`

![Screenshot 2025-05-03 222757](https://github.com/user-attachments/assets/2fbb6003-8fb2-4c1e-8ade-3e90e6cddfa2)

The cipher is Base62 encoding, after decoding we get another cipher, Caesar. 

![Screenshot 2025-05-03 222845](https://github.com/user-attachments/assets/72d99d68-90d6-4ee6-9452-fe12caf18035)

The second cipher: `Av aol vul dov mpukz aopz zjyvss, ruvd aoha dpzkvt splz pu aol jvkl: IpaJAM{zljylaz_vm_aol_jhlzhy}.
Zopma aol slaalyz aopyallu aptlz, hz aol hujpluaz vujl kpk`

Identifying the second cipher.

![Screenshot 2025-05-03 223200](https://github.com/user-attachments/assets/0464b429-63e0-4148-8d9f-99f867515a71)

Decoding using ROT also works since Caesar cipher is a monoalphabetic cipher. Below is the decoded cipher.

![Screenshot 2025-05-03 223004](https://github.com/user-attachments/assets/251e2956-daf1-4930-9418-7bca8d8af666)

flag: `BitCTF{secrets_of_the_caesar}`

### summary
The challenge involved identifying and decoding two ciphers.
