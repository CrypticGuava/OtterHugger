# OtterHugger

Best in class fileless polymorphic loader. Written in C.
Patches AMSI, ETW, never touches disk, silent as a mouse.

DISCLAIMER: This requires licenses to Cobalt-Strike for authorized penetration testing. Do not attack machines you do not own or do not have permission to test.
The author will not be held liable for misuse of this product.

DEPENDANCIES
Requires SGN encoder https://github.com/EgeBalci/sgn/releases
Golang, pip, and python.


Installation one-liner
``` sudo curl https://github.com/CrypticGuava/OtterHugger/tree/main && curl https://github.com/EgeBalci/sgn/releases &&  cd ~/Downloads/OtterHugger/ && sudo chmod +x sgn ```

Usage
1. Generate shellcode from C2
2. Encode with SGN
3. xxd <payload> > "payload.h"
4. add payload.h as header of scripting tool of choice
5. add OtterHugger as main script
6. Compile
7. Follow ATT&CK matrix, this loader is for step 2 of ATT&CK.
8. GoPhish, SMTP spoof, MITM redirect, USB drop, msfconsole, etc.
9. Pwned


<img width="1815" height="662" alt="flow" src="https://github.com/user-attachments/assets/984a6132-e51e-4800-aa30-5442dad13781" />
credit@ EgeBalci




Challenge.
I challenge you to find any traditional antivirus that will detect this payload. It patches AMSI therefore antivirus does not even get the oppurtunity to scan it. Also it doesn't touch disk, ever. (Post exploitation detectopn does not count, you will eventually get detected by being "loud")

Contact
GuavaMonkey4422@protonmail.com
