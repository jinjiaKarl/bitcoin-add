# bitcoin-add

git clone https://github.com/jinjiaKarl/bitcoin-add.git

cd bitcoin-add

go build -o add

./add

0 - Having a private ECDSA key
14DAC18B7A0C1466E38F840BD9637FA3B0A48DE51F74062792DB779C4569901A
=======================
1 - Take the corresponding public key generated with it (65 bytes, 1 byte 0x04, 32 bytes corresponding to X coordinate, 32 bytes corresponding to Y coordinate)
raw public key 07A93EDAFA9110E29FBD39FE9E47150205C610883189649658755BE8C538D4B4506009DB1EDFC4B4434CC8E81429D6388E7A3DD3792957108997423F12CFCE20
=======================
2 - Perform SHA-256 hashing on the public key
2355E18185F00E497106A1579A85AE13629B4ADBF9B5EF2E2779401106AE55A8
=======================
3 - Perform RIPEMD-160 hashing on the result of SHA-256
94AE117E54101AE442BA8F9EF2B96A2D65C851C7
=======================
4 - Add version byte in front of RIPEMD-160 hash (0x00 for Main Network)
0094AE117E54101AE442BA8F9EF2B96A2D65C851C7
=======================
5 - Perform SHA-256 hash on the extended RIPEMD-160 result
7478386539A2D9C873A51AD883373D0FF51E02127CA858327780512347700EE0
=======================
6 - Perform SHA-256 hash on the result of the previous SHA-256 hash
C7A5FC58231C82D03EC29552C6364D50C51E42128911797FBD3B897D93D42A2B
=======================
7 - Take the first 4 bytes of the second SHA-256 hash. This is the address checksum
C7A5FC58
=======================
8 - Add the 4 checksum bytes from stage 7 at the end of extended RIPEMD-160 hash from stage 4. This is the 25-byte binary Bitcoin Address.
0094AE117E54101AE442BA8F9EF2B96A2D65C851C7C7A5FC58
=======================
9 - Convert the result from a byte string into a base58 string using Base58Check encoding. This is the most commonly used Bitcoin Address format
1EZ9XsWGd8iowSMiBuFPe4aC6nuxRZzhTm
=======================
=======================
=======================
=======================
0 - Having a private ECDSA key
14DAC18B7A0C1466E38F840BD9637FA3B0A48DE51F74062792DB779C4569901A
=======================
private wallet import format
1 - Add version byte in front of RIPEMD-160 hash (0x00 for Main Network)
8014DAC18B7A0C1466E38F840BD9637FA3B0A48DE51F74062792DB779C4569901A
=======================
2 - Perform SHA-256 hash on the extended RIPEMD-160 result
9B8C19A3469D7E2D8A3422713F8E1059CB1DD14B64523F5BFA5E9CB94A5D5A76
=======================
3 - Perform SHA-256 hash on the result of the previous SHA-256 hash
9B1D6F1D3F8F2B170BF1B0F845D1218EC3804C6C4AEBA5CB190A986F2980B053
=======================
4 - Take the first 4 bytes of the second SHA-256 hash. This is the address checksum
9B1D6F1D
=======================
5 - Add the 4 checksum bytes from stage 7 at the end of extended RIPEMD-160 hash from stage 4. This is the 25-byte binary Bitcoin Address.
8014DAC18B7A0C1466E38F840BD9637FA3B0A48DE51F74062792DB779C4569901A9B1D6F1D
=======================
private wallet import format 5HyUHKKZ2Kc8JF2diUFdTGBT8RrqyYag9ui9UUEyeNDopcFxbrc
=======================
