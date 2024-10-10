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
