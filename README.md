# OtterHugger

Best in class fileless polymorphic loader. Written in C.
Patches AMSI, ETW, never touches disk, silent as a mouse. I've tested this on different antiviruses including Windows Defender, Avast, Crowdstrike Falcon. 


DISCLAIMER: This requires licenses to Cobalt-Strike for authorized penetration testing. Do not attack machines you do not own or do not have permission to test.
The author will not be held liable for misuse of this product.

DEPENDANCIES
Requires SGN encoder https://github.com/EgeBalci/sgn/releases
Golang, pip, and python.


Installation one-liner
``` sudo wget https://github.com/CrypticGuava/OtterHugger/blob/main/OtterHugger & nano OtterHugger```

Usage
1. Generate shellcode from C2, enable AMSI patching there. It's not done natively with OtterHugger yet.
2. Encode with SGN
3. ``` bash xxd <payload> > "payload.h" ```
4. add payload.h as header of scripting tool of choice
5. add OtterHugger as main script
6. Compile
7. Follow ATT&CK matrix, this loader is for step 2 of ATT&CK.
8. GoPhish, SMTP spoof, MITM redirect, USB drop, msfconsole, etc. Just some examples. If you need a loader for an smb attack, this will work also. No phishing required.
9. Pwned


<img width="1815" height="662" alt="flow" src="https://github.com/user-attachments/assets/984a6132-e51e-4800-aa30-5442dad13781" />
credit@ EgeBalci

Fun fact: OtterHugger got its name because it acts as a "wrapper". Imagine an otter hugging an apple down a stream. OtterHugger "wraps" shellcode with additional customizations such as AMSI patching and converts them to an executable. It started out as a placeholder name but I've decided to give it lore post publishing. 


Challenge.
I challenge you to find any traditional antivirus that will detect this payload. It patches AMSI therefore antivirus does not even get the oppurtunity to scan it. Also it doesn't touch disk, ever. (Post exploitation detection does not count, you will eventually get detected by being "loud", OtterHugger is one of the better hacking resources out there, you're not going to be able to hashdump willy nilly using metasploit, no matter how you encode your payloads due to heuristics.)

Contact
GuavaMonkey4422@protonmail.com
