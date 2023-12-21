run game need libssl.so
Here are two file:
1. libssl_1.0.0_32-bit.tar.gz
2. libssl_1.0.0_64-bit.tar.gz
extract
```shell
tar -xf libssl_1.0.0_32-bit.tar.gz
tar -xf libssl_1.0.0_64-bit.tar.gz
```
copy to current path
```shell
cd libssl_1.0.0_32-bit
cp libcrypto.so.1.0.0 libssl.so.1.0.0 {Stardew Valley}/game
cd ../libssl_1.0.0_64-bit
cp libcrypto.so.1.0.0 libssl.so.1.0.0 /usr/lib/
```