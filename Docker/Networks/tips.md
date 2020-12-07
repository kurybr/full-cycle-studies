Tipos de Network:

- bridge 
    - Network padrão do docker, que é usada para comunicar entre imagens.

- host 
    - Network usada para mesclar a rede do computador com a rede do container.

- overlay
    - Network usada para mesclar a rede do roteador com as redes do container. 
        - vários dockers de vários computadores se comunicam entre si.

-maclan

-none
    - Isola o container, e não permite que ele se comunique com nenhuma rede ( inclusive de internet )



Cria uma rede nova no docker ! 
docker network create --driver bridge {network}

<!-- Ao criar um container se você vincular ele a uma network, você consegue pingas as maquinas usando o alias ao invés do IP -->
docker run -dit --name {container} --network {network} bash

<!-- Pluga um container ja existente dentro de uma rede -->
docker network connect {network} {container}



<!-- Ele já mescla a rede do docker host com o container  -->
<!-- Como o nginx usa naturalmente a porta 80, se digitar localhost ele já em tese acessaria o nginx -->
docker run --rm -d --name nginx --network host nginx




<!-- Acessando o host de dentro do ambiente docker -->
http://host.docker.internal:80801