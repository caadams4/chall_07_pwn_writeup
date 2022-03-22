# chall_07_pwn_writeup

Recon the binary:

  Checksec: has RWX segemnts and executable stack 
  file: 64 bit dynamically linked

We know we can execute shellcode from the stack, but no smashing.

Now lets recon the binary w/ radare 2.

![image](https://user-images.githubusercontent.com/79220528/159482349-8796c35f-cef5-465b-8943-d8bec7ef2af6.png)

No vuln or win function. Interesting fgets and a call to the fgets' input. 

Lets insert some shellcode. 

![image](https://user-images.githubusercontent.com/79220528/159482726-db98689e-f077-45f1-88aa-52e5a416b22c.png)
