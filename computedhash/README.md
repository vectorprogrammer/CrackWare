# Precomputed Hash Tables
These are series of pre computed hash tables similar but not rainbow tables as they are forged by  sending a random string into a hash algorithim and puts the uncomputed passwords with the hashed passwords
```
Example
crackware -r --hash=sha256 3700adf1f25fab8202c1343c4b0b4e3fec706d57cad574086467b8b3ddf273ec
crackware -r --hash=sha512 fb997d5c01ebcf962d820b3b0e7f8bfeeb7f4bd337cc83682f2af90d252c20c5d85744b7c6bb94f48139f690a61e4ad317d6107e4310efc016d9287266b5172b
#Output is password12345
Another Example
crackware -r --hash=sha384 0fa76955abfa9dafd83facca8343a92aa09497f98101086611b0bfa95dbc0dcc661d62e9568a5a032ba81960f3e55d4a
crackware -r --hash=490c161444dcd7f4b3916833377c0a55
#Output is 12345
Example 3
crackware -r --hashfile=sha384file db2a301927bc0fbe3d36f2739527be7b55a6937135ab0e1f99eb4f3e3c5450ccb3173d9322a077f3b091408e436596bd
```
