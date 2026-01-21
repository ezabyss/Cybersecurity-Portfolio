## How the Caesar Cipher Works

The Caesar cipher is one of the oldest encryption techniques. It works by shifting each letter of the alphabet by a fixed number of positions.

For example, with a shift of 3:
- A becomes D
- B becomes E
- C becomes F
- X becomes A
- Y becomes B
- Z becomes C

This means the alphabet “wraps around” when it reaches the end.

### Example
Original text:
    hello

Encrypted with a shift of 3:
    khoor

Each letter is moved three places forward in the alphabet.

### Why It Is Weak
The Caesar cipher is weak because:
- There are only 25 possible shifts
- An attacker can easily try all shifts
- No secret key is required

Because of this, Caesar ciphers can be broken quickly using simple tools, such as character translation commands in Linux.

### Why We Used `tr` to Break It
In this lab, the encrypted text was shifted **3 letters to the left**, meaning:
- d maps back to a
- e maps back to b
- f maps back to c

The `tr` command was used to map the shifted alphabet back to the original alphabet, effectively reversing the Caesar cipher.
