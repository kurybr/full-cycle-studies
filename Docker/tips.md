<!-- Apaga todas as imagens do computador -->
docker rm $(docker ps -a -q) -f


<!-- 
Qualquer arquivo .sh que finaliza com exec "$@" 
muito importante no uso do entrypoint
-->

<!-- Sobe o repositório para o dockerhub -->
<!-- Prestar atenção no nome da imagem deve possuir username/nome-do-container -->
docker push (nome do container) 