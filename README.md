# Instalasi_DFTBplus

## Instalasi menggunakan git clone 
1. sudo apt install git 
```
2. Cloning Repositori DFTB+ 
```
git clone https://github.com/dftbplus/dftbplus
```
## Mensetting DFTB+
1. Membuka config.cmake 
```
nano config.cmake
```
3. Ubah text FALSE (Bila ada) pada line berikut menjadi TRUE
```
option(WITH_OMP "Whether OpenMP thread parallisation should be enabled" TRUE)
option
```
4. Instalasi gfortran dll 
```
FC=gfortran CC=gcc cmake -DCMAKE_INSTALL_PREFIX=tempat instalasi -B build .
```
5. Apabila terdapat library yang masih error, maka ketik berikut untuk menginstall library tsb : 
```
sudo apt install lib(namalibrary)-dev
sudo apt install libarpack2 
sudo apt install libarpack2-dev
```
6. Apabila masih ada yang error, maka bisa menghilangkan build yang dihasilkan dari penggunaan cmake dengan :
```
rm -rf build 
```
7. lanjutkan dengan mengulangi langkah 4
```
8. Membuild C Folder Build 
```
cmake --build build -- -j jumlahprosesor 
```
## Download parameter untuk DFTBplus 
1.  Download parameter slakos
```
./utills/get_opt_externals slakos
```
2. untuk mengetest dftb plus 
```
ctest -j jumlahprosesor
``` 
3. 
