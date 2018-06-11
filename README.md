# bitcoin-add

git clone https://github.com/jinjiaKarl/bitcoin-add.git

cd bitcoin-add

go build -o add

./add

运行结果如下：
0 - Having a private ECDSA key
78A259B7E77DB73A43DBB53D955420FDA443120244CED69B5FE49BDAF4713689
=======================
1 - Take the corresponding public key generated with it (65 bytes, 1 byte 0x04, 32 bytes corresponding to X coordinate, 32 bytes corresponding to Y coordinate)
raw public key BB921C503BCB4D3041BF0A907AD44A192CF540355D4CCBE588472E825F332CA22AE116AF6B7DFC2A3950614E39EDDCF48FC63B837458B9EC28A6AEA06FCAAC70
=======================
2 - Perform SHA-256 hashing on the public key
48E746B21D0A603C20555E72FF06E932E352693AD2E487BA7DB5E0F9132E6648
=======================
3 - Perform RIPEMD-160 hashing on the result of SHA-256
FA451D7DF2B0865F1E6223F18298D30F5BBB912E
=======================
4 - Add version byte in front of RIPEMD-160 hash (0x00 for Main Network)
00FA451D7DF2B0865F1E6223F18298D30F5BBB912E
=======================
5 - Perform SHA-256 hash on the extended RIPEMD-160 result
B7DFEC31A5342039715A4BA317905A98C6C60615F24B832ACBCF59C5190F5E19
=======================
6 - Perform SHA-256 hash on the result of the previous SHA-256 hash
F5C16BF8951937E145180A9F72F1B1616D0FCFAA39B99629EC2DCCBDA5053E9F
=======================
7 - Take the first 4 bytes of the second SHA-256 hash. This is the address checksum
F5C16BF8
=======================
8 - Add the 4 checksum bytes from stage 7 at the end of extended RIPEMD-160 hash from stage 4. This is the 25-byte binary Bitcoin Address.
00FA451D7DF2B0865F1E6223F18298D30F5BBB912EF5C16BF8
=======================
9 - Convert the result from a byte string into a base58 string using Base58Check encoding. This is the most commonly used Bitcoin Address format
1PpJjAdmXYMb1fxFvafkgcAZxf76tRsXrw
=======================
=======================
=======================
=======================
0 - Having a private ECDSA key
78A259B7E77DB73A43DBB53D955420FDA443120244CED69B5FE49BDAF4713689
=======================
private wallet import format
1 - Add version byte in front of RIPEMD-160 hash (0x00 for Main Network)
8078A259B7E77DB73A43DBB53D955420FDA443120244CED69B5FE49BDAF4713689
=======================
2 - Perform SHA-256 hash on the extended RIPEMD-160 result
37207BFCBD70B2BB2A04EE57F5CB61AF3AC580FCC0B9B8A99BA1F25579E3FCBF
=======================
3 - Perform SHA-256 hash on the result of the previous SHA-256 hash
5ADDFCA53F842352CDD06ED39A20A6B470C9C836012D80014CFBA0EE07072DBD
=======================
4 - Take the first 4 bytes of the second SHA-256 hash. This is the address checksum
5ADDFCA5
=======================
5 - Add the 4 checksum bytes from stage 7 at the end of extended RIPEMD-160 hash from stage 4. This is the 25-byte binary Bitcoin Address.
8078A259B7E77DB73A43DBB53D955420FDA443120244CED69B5FE49BDAF47136895ADDFCA5
=======================
private wallet import format 5JjR26kVh84d9XaZ9s4NzrHmJ9abhmgtUSJHNrMzKCZUWhfZoqn
=======================
