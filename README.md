# Bleichenbacher-Attack
Bleichenbacher Attack is based on the vulnerability associated with PKCS#1 v1.5
padding scheme of RSA. It was demonstrated by Daniel Bleichenbacher in 1998.
Bleichenbacher Attack is also called as Padding Orcale Attack or Adaptive Chosen
Ciphertext Attack. This attack is based on a padding oracle which reveals, if the
decrypted message is correctly padded according to PKCS#1 v1.5 or not. This attack is
called adaptive as the attacker choses the chosencipher depending on the previous
outcome of the attack from the server side. Return Of Bleichenbacher’s Oracle
Threat(ROBOT) was discovered 20 years later which suggests 5 test vectors which
checks vulnerability of the server to the Bleichenbacher attack. The attacker can also
create valid signature without leaking the private key using the ROBOT.

The Bleichenbacher Attack is being implemented using python code in google collab.

As a part of implementation, the Bleichenbacher Attack is being implemented in python  using Google Colaboratory.

The code consists of  step by step implementation of the Bleichenbacher Attack.

Initially we encode the given message using PKCS#1 v1.5 scheme:
      PKCS1(M) = 0x00 | 0x02 | [non-zero padding bytes] | 0x00 | [M].
Then we decode the PKCS#1 v1.5 string.
An oracle is being designed which tells whether the given ciphertext decodes to a valid PKCS#1 v1.5 encoding scheme, i.e. the first two bytes of the
  plaintext == "\x00\x02".
We find the smallest s >= lower_bound, such that (c*s^e)(mod n) decrypts to a PKCS#1 v1.5 conforming string.
Given the interval [a,b], we reduce the search only to relevant regions and stop when an ‘s’ value gives a PKCS#1 v1.5 conforming string.
We deal with interval overlaps when adding a new one to the list.
After finding the s value, we compute the new list of intervals.
Next, we perform Bleichenbacher Attack.
Input:
The input is already mentioned in the code in the hexadecimal format.

Output:
The output returns the total number of queries along with the actual message and the decrypted message. 

