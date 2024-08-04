.. __why-rsa-is-not-secure.rst:

==============================================
Why RSA is not secure against Quantum Attacks
==============================================
This article is not done yet.

Introduction
-----------------
In my previous `article <https://yyueyangg.github.io/personal-docs/what-is-rsa.html>`__, I have introduced RSA as a widely-used cryptographic
algorithm. I have also warned that quantum computers may potentially break RSA encryption, rendering quantum attackers with powerful
quantum computers unfair capabilities which threatens secure communication. In this article, I would like to explain why RSA is not secure
against quantum attacks.

RSA's advantage against classical computers' attacks
-----------------------------------------------------
Assuming that e is fairly large enough, attacks on RSA is based largely on:

- finding the private key, d

- In order to calculate for d, an attacker would need to find out the value of the totient, phi_n

- phi_n is the result of multiplying p-1 and q-1

- Finding p-1 and q-1 would require the attacker to first factorize n into p and q, as n = pq

So, by rearranging the steps, an attacker would have to:

1. factorize n into p and q

2. calculate the totient phi_n by multiplying p-1 and q-1 

3. Using the totient to calculate for the private key, d


RSA encryption relies on the difficulty of factoring large number, n, into their prime components. This is a challenging task for 
classical computers, which is very likely unable to factorize n. 

RSA's disadvantage against quantum computers' attacks 
-------------------------------------------------------
Quantum computers, on the other hand, can utilize Shor's algorithm, which was developed by mathematician Peter Shor in 1994. 
Shor's algorithm allows quantum computers to factor large numbers, in this case, n, in polynomial time, making the task much more feasible compared to 
classical algorithms.

More about Shor's Algorithm
------------------------------
Shor’s algorithm factorises integers exponentially faster than the best-known classical algorithms.
The efficiency of Shor's algorithm on a sufficiently powerful quantum computer would make it possible to break RSA encryption by 
factoring the large numbers that are used as keys


So, is RSA vulnerable now?
--------------------------
The whole "quantum computers may break RSA encryption" is under the assumption that the number of qubits required by the quantum computer 
to perform the factorisation is sufficient to break RSA's encryption. 


Then when will RSA become vulnerable?
---------------------------------------


Conclusion
------------