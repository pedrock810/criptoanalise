- [Versão em Português](#versão-em-português)
- [English Version](#english-version)

## Versão em Português

O objetivo dessa aplicação web é fazer transferências de arquivos entre utilizadores de forma segura. Para isso, foram utilizadas cifras AES-CBC e o protocolo de chaves públicas e privadas RSA, além de garantir a integridade dos arquivos com códigos HASH. A transferência dos arquivos é feita utilizando base de dados, onde todos os usuários podem acessar os arquivos presentes nela, entretanto, somente o dono da respectiva chave privada pode fazer o download do arquivo decifrado. Abaixo encontram-se representações da aplicação em funcionamento.

1. Criação de um token
![image](https://github.com/user-attachments/assets/d2749451-825b-4ed0-830d-15ed85436f6a)

Ao criar um token, um arquivo .zip é baixado contendo uma chave pública e uma chave privada RSA. O token e sua respectiva chave pública ficam salvos na base de dados MySQL.

2. Enviar arquivo
![image](https://github.com/user-attachments/assets/fad726c4-1f44-4bb8-94e8-9b6c1e2d8860)

Para enviar um arquivo, basta digitar o token de quem irá o receber. Dessa forma, o arquivo será enviado para a base de dados cifrado com a chave pública do token selecionado. Além disso, pode-se definir se o arquivo será cifrado e/ou compactadado (zip) antes do envio ser efetuado.

3. Receber arquivo
![image](https://github.com/user-attachments/assets/3e8004f9-1305-41ad-934c-59d40278edd2)

Na primeira parte dessa seção, é possível digitar o seu token para listar todos os arquivos que estão associados à ele, para que, dessa forma, seja possível obter o ID do arquivo desejado, assim como sugere a imagem acima.

![image](https://github.com/user-attachments/assets/6372cdf7-2ba5-455e-aeac-f4add87c3960)

Após identificar o ID do arquivo desejado, basta digitá-lo na segunda seção deste collapse e selecionar o arquivo .pem que contém a chave privada válida para fazer o download do arquivo já decifrado (caso ele tenha sido cifrado).

## English Version
The purpose of this web application is to securely transfer files between users. To this end, AES-CBC ciphers and the RSA public and private key protocol were used, in addition to ensuring the integrity of the files with HASH codes. The files are transferred using a database, where all users can access the files contained in it; however, only the owner of the respective private key can download the decrypted file. Below are representations of the application in operation.

1. Creating a token
![image](https://github.com/user-attachments/assets/d2749451-825b-4ed0-830d-15ed85436f6a)

When creating a token, a .zip file is downloaded containing an RSA public key and a private key. The token and its respective public key are saved in the MySQL database.

2. Send file
![image](https://github.com/user-attachments/assets/fad726c4-1f44-4bb8-94e8-9b6c1e2d8860)

To send a file, simply enter the token of the person who will receive it. This way, the file will be sent to the database encrypted with the public key of the selected token. In addition, you can define whether the file will be encrypted and/or compressed (zip) before sending it.

3. Receive file
![image](https://github.com/user-attachments/assets/3e8004f9-1305-41ad-934c-59d40278edd2)

In the first part of this section, you can enter your token to list all the files that are associated with it, so that you can obtain the ID of the desired file, as suggested in the image above.

![image](https://github.com/user-attachments/assets/6372cdf7-2ba5-455e-aeac-f4add87c3960)

After identifying the ID of the desired file, simply enter it in the second section of this collapse and select the .pem file that contains the valid private key to download the already decrypted file (if it has been encrypted).
