# CONVERSAO-TEMPERATURA
É uma simples aplicação para converter temperatura que foi desenvolvida para fins de teste a partir do treinamento INICIATIVA KUBERNETES Por FABRICIO VERONEZ .

## Como rodar o projeto?

* Pré condiçaõ Git, Docker, K3d, Kubectl instalados
* Clone esse repositório.
* Rode o ambiente com os comandos.

##-NO TERMINAL
```
git clone https://github.com/vladetec/conversao-temperatura.git
cd conversao-temperatura
cd k8s
k3d cluster create mycluster --servers 1 --agents 3 -p "8080:30000@loadbalancer"
kubectl apply -f deployment.yaml

```
## Links

[Conversao-Temperatura](http://localhost:8080/)
[Comandos-K3d](https://k3d.io/v5.2.2/usage/commands/)
[Comandos-Kubectl](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands)
## Comandos Uteis no Docker

##- Criar e Listar imagem Docker
```
docker image build -t conversao-temperatura . 
docker image ls
```
##- Rodar e Listar container Docker
```
docker container run -d -p 8080:8080 conversao-temperatura
docker container run -d -p 8080:8080 <Id>
docker container ls
```

##- Remover imagem e container Docker
```
docker container rm -f <ID>
docker image rmi -f <ID>
```
##_ Outros comandos usados
```
docker ps -a
docker login
docker push vladedocker/conversao-temperatura:v1
docker tag vladedocker/conversao-temperatura:v1 vladedocker/conversao-temperatura:latest
docker push vladedocker/conversao-temperatura:latest
docker image prune
docker container prune
```



