# Bleichenbachen-Attack
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
