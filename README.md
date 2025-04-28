# Ciphashkill
Ciphash kill are compressed tables of ciphers and hashes
that are stored in a rainbow tables for hashes and phrases and letters
for ciphers.
```
Example
crackware --ciphash=cipher --AES 53616c7465645f5fea0cebfc1878c4f50b2d297bb9b164443ee152fe719b933d
crackware --ciphash=hash --Whirlpool e35626d2706c6a68c89e9fae0edccfa458bf0a7546c5d796ce4f98f6762a211feea41015ad0dae43b9e829f65de7d3318eaa6b646f93e86bb6728f168f3b271d
Output is helloguys 
```
Sometimes, multiple hashes are used, CrackWare requires specifications, using the hash-multiple parameter in input box
```
Example
crackware --ciphash=hash-multiple --Whirlpool(in this example the whirlpool hash is used first, and then encrypted by sha3-256 again) --SHA3-256 60f97bca9232e8d47e248eeffb7665ea79422afa076348b9fc3aa677609ebdfe
Comparing...
Reversing SHA3-256...
SHA3-256 Reversed: 90e73c08ea5f2bc77a6ba050aade50ee51d8824f19ab254a99a6ea1ea6500aca9300104f6a4531a003f8d018762bb7b94251f314ec7d3415d0b91440a6fa92b6
Comparing...
Reversing Whirlpool...
Unhashed password: examplepassword
```
When a Cipher or Hash is unknown, decryption requires special methods
```
Example
crackware --ciphash=unknown --identify 3f2390d0a7495de0ed6e994a2ddccbe2f0db351adf66812b262eb0498b18b5edfb6ca260c510900b1ba40fa91110b70317d7bd740bb71cd15cdd14b96d40582f
Identifying...
Calculating...
Probability: Hash 99%, Cipher 1%
128-character structure...
Can possibly be SHA-512 or SHA3-512...
SHA-512 output unknown
SHA3-512: socanalyst12345
```
If a hash is ciphered, it needs to be decrypted via another parameter

```
Example
crackware --ciphash=hashed-cipher --hash=sha1 --cipher=base64 c12042cbd926dfc3139b23be457f2861594f59f5
Comparing...
SHA1 Reversed: YmVlZi14c3MgaXMgcmVhbCBnb29k
Comparing Ciphertext...
Base64 Reversed: beef-xss is real good
```
Salts and Peppers can also be stripped from targeted hashes

```
crackware --ciphash=salt
```

```
Example
crackware --ciphash=cipher --all-use <cipher>
```
This is an example of all-use. It can only be used for ciphers
 Reversed: beef-xss is real good
```
Salts and Peppers can also be stripped from targeted hashes

```
crackware --ciphash=salt
```

```    
Example
crackware --ciphash=cipher --all-use <cipher>
```
This is an example of all-use. It can only be used for ciphers
