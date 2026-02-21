## Encryption

Encryption involves transforming data into a secure format (plain text to cipher text), ensuring only users with the correct key can retrieve the original data. It serves primarily to safeguard data during transmission or storage.

**Key Points:**
- Protects data confidentiality.
- Utilized in HTTPS for secure web communication.
- Prominent Algorithms: AES, RSA, Blowfish.

### Types of Encryption

1. **Symmetric Encryption**: This uses the same key for both encryption and decryption. Examples include AES and Blowfish.
   
- It is important to keep the key secret, as anyone with the key can decrypt the data.
- Faster than asymmetric encryption, making it suitable for encrypting large amounts of data.
- Ciphertext is same length as the plaintext.

2. **Asymmetric Encryption**: This uses a pair of keys, one for encryption (public key) and one for decryption (private key). Examples include RSA and ECC.

- The public key can be shared openly, while the private key must be kept secret.
- Slower than symmetric encryption, making it less suitable for encrypting large amounts of data, but ideal for secure key exchange and digital signatures.
- Ciphertext is typically longer than the plaintext due to the use of key pairs and additional data for security.

## Encoding

Encoding is the process of converting data to facilitate transfer between systems and applications. It maintains data integrity and usability and employs publicly available algorithms for conversion.

**Key Points:**
- Ensures data integrity during transmission.
- Algorithms publicly available for decoding.
- Prominent Algorithms: ASCII, UNICODE, URL Encoding, Base64.

## Hashing

Hashing is a one-way process where data is converted into a fixed-length alphanumeric string, known as a hash or message digest. It serves to verify data integrity, often used for checksum verification.

**Key Points:**
- Irreversible transformation.
- Ensures data integrity through checksum verification.
- Identical data produces identical hashes.
- Prominent Algorithms: MD5, SHA-1, SHA-256.
- Commonly used for data integrity verification and password storage
