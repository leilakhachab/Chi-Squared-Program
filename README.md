# Chi-Squared-Program
# Caesar Cipher Cracker

# What it does
Automatically decrypts a Caesar-shift cipher without knowing
the key, using chi-squared analysis of letter frequencies.

# How it works
For each of the 25 possible shifts, the ciphertext is decrypted and its 
letter frequency distribution is compared against standard English 
letter frequencies using a chi-squared goodness-of-fit test:

    χ² = Σ (O - E)² / E

where:
O is the observed count of each letter in the candidate plaintext 
and
E is the expected count based on known English letter frequencies. 

The shift with the lowest chi-squared score is taken as the correct key, 
since its letter distribution deviates least from real English.

## Usage
Edit the `ciphertext` variable in `Chi-square-cryptanalysis.R` and run:

    Rscript Chi-square-cryptanalysis.R

It will output the detected shift and the decrypted message.
