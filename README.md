# Projeto_AWS-S3_Resize-Scrypt_Python
Criação de um Script Python que altera o tamanho das imagens dentro do AWS S3
.
.
S3 Resize
.
.
Imaginando um cenário onde temos um website, e nesse website os usuários precisam fazer o upload de imagens, no entanto ela precisa ser realizado pelo site em uma dimensão especifica.
EX: 128x128
.
.
.
.
.
1) Função lambda que captura a imagem que o usuário faz o upload e depois converter a imagem para o tamanho que quisermos, deixando a versão original e também deixando uma versão thumbnail (miniatura)

2) Construir um Bucket S3 - ORIGEM, onde o usuário poderá fazer o upload da imagem dentro dela

3) Contruir um Bucket S3 - DESTINO, onde ficarão as imagens transformadas

4) Função lambda pega a imagem do Bucket S3 do tamanho que o usuário fez o upload e converta em 128x128, fazendo o carregamento para o Bucket S3 - DESTINO

5) Politica de IAM para permissões na Bucket de ORIGEM e DESTINO. (PUT, GET)

6) Trigger para monitorar o Bucket ORIGEM, onde se algum novo objeto entrar no bucket, rode o Script Python
