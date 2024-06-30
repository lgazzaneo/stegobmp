# Stegobmp
## TP implementacion de Cripto

Lautaro Nicolas Gazzaneo - 61484
Tristan Flechard - 66692


###  Para compilar los archivos correr el siguiente comando:
    javac Encryptor.java BMPReader.java StegoImage.java StegoBmp.java

### Para usar las funciones solo corran el comando 
```bash
java StegoBmp.java -embed -in <file> -b <bitmapfile> -out <bitmapfile> -steg <LSB1 | LSB4 | LSBI> [-pass <password>] [-a <aes128 | aes192 | aes256 | des>] [-m <ecb | cfb | ofb | cbc>]
```
```bash
java StegoBmp.java -extract -p <bitmapfile> -out <file> -steg <LSB1 | LSB4 | LSBI> [-pass <password>] [-a <aes128 | aes192 | aes256 | des>] [-m <ecb | cfb | ofb | cbc>]
```    
Examples 
```bash
java StegoBmp.java -extract -p data/ladoLSBIaesofbsalt0.bmp -out test -steg LSBI -pass margarita -a aes256 -m ofb
```

```bash
java StegoBmp -embed -in example.txt -b quilmes.bmp -out quilmesHidden.bmp -steg LSBI -pass password -a AES128 -m CBC
```

```bash
java StegoBmp -extract -p quilmesHidden.bmp -out example_out -steg LSBI -pass password -a AES128 -m CBC
```