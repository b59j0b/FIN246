java c
ASSIGNMENT 2
FIN246
Spring 2025
DUE:    Monday, March 3th at the beginning of class (3:25pm EST)
1. Using the last 4 digits of your student number, look up Bitcoin block 820000 + last 4 digits of your id (Example, if the last 4 digits are 1234, look up block 761234) at the following site:      
https://www.blockchain.com/explorer
Once you have the details of the block loaded, answer the following:
(a) How many leading 0s are in the final hash?
(b) Click on the hash for the block to see the transaction detail:
(i)   What is the nonce?
(ii)   How many possible nonce calculations are there?
(c) Looking at the transaction detail, what details are publicly available on the blockchain? What do you not see?
(d) Why is the first transaction in this block different from the rest in terms of input/output matching? What is going on here?
2. Go to https://bestwallettoken.com/en
   Evaluate the BestWalletToken ($BEST) initial coin offering based on details you can find:
(a) Who are the executives, directors and major owners of the company and were is it located? Is the company owned through holding $BEST? Explain based on what you can learn.
(b) How is the coin/token mined (proof of work, proof of stake, etc.)? Explain.
(c) How does the staking rewards work? Does the buyer of the $BEST token profit from the business operations? Explain.
(d) Is this token a security under the Howey test? Apply the test in detail and consider arguments for and against the test applying.
3. Find the address pair (n,e) that matches the last 4 digits of your student number in FIN246 Blockchain-RSA(Spring 2025).xlsx (posted with the assignment). These are addresses from a simulated Bitcoin-type blockchain based on RSA public key cryptography. Each address pair (n,e) applies to transactions in the blockchain (which can be messages or amounts of coins).
(a ) Your friend, Bob, who believes their communications are being monitored sends you a 10 alphanumeric password using RSA public-key encryption. He sent 10 separate numbers (one for each letter/number) to the public address (n,e) associated with the last 4 digits of your student number. Each number is given in the FIN246 Blockchain - RSA file. After you decrypt this password, you can then communicate with Bob through shared files/social media and/or other places where knowing the password allows access.
(i) Break the RSA address (n,e) by finding p, q, (p-1), (q-1), d. (Note: you will have to use process below to break the RSA pair (n,e) and find d).
(ii) Use d to unencrypt each of the 10 代 写FIN246 ASSIGNMENT 2 Spring 2025Matlab
代做程序编程语言numbers (Note: you will need https://www.dcode.fr/modular-exponentiation:)
(iii) Each resulting number is in ASCII form, which you should convert to alphanumeric using the =char() function in Excel
(iv) Write out the password (which is case sensitive)
(b) Choose a pair (n*,e*) from the Unassigned tab in the spreadsheet where n* contains at least 4 different digits from your student number and transfer coins equal to the last four digits of your student number from the given address (n,e,) to this new address (n*,e*).
(i ) Find the d* that goes with the new address (n*, e*)
(ii ) Calculate the transaction message using
https://www.dcode.fr/modular-exponentiation:
m          (n + tokens + n*)       mod n
(iii ) Then calculate the digital signature, c, again using the online calculator:
digital signature:          c          md      mod n          
(iv) Write out the transaction details: n, tokens, n*, c
(v) Verify the transaction by calculating    
m          ce      mod n                This should be the same m as calculated above using
         m          (n + tokens + n*)       mod n
Details of FIN246 Blockchain  RSA:   Each block address is a number pair [n, e] where n = p x q and e is the public key   (which is actually an exponent variable). The factors p and q are not known publicly, but can be determined by factoring n. (Hint: the prime numbers used in this assignment are all chosen from the primes listed in a tab in the spreadsheet)
A valid transaction on this blockchain requires a digital signature, c, to prove that the sender has the private key, d, to the address. This digital signature is of the message, m, is created by taking the transfer block address n and adding to it the message (number of tokens and the new owner’s block address n* (example: 582918502 + 5361 + 624530918 = 1207454781).
“Breaking” RSA public key cryptography requires:
For each block address, you are given n, e. If you can factor n into p x q, then you can follow the steps in the RSA algorithm (see the Wiki page for additional help):
   (i) Find (p-1)(q-1)
   (ii) Find the least common multiple (lcm) of (i):    in excel use =lcm((p-1),(q-1))
   (iii) Find Use the totient function to find d:   d= (lcm((p-1) , (q-1)) + 1) / e
[Note: this can be a tricky step, so I have carefully chosen all pairs, n, e, so that d is an integer result]
   (iv) Verify your solution by using https://www.dcode.fr/modular-exponentiation   
to prove with modular arithmetic   that 1    d x e mod lcm    

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
