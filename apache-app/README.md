🚀 Kubernetes Web Apps: Nginx & Apache no Seu Cluster Local! 🌐
Este projeto demonstra a implantação de duas aplicações web simples – um servidor Nginx e um servidor Apache – em um ambiente Kubernetes local. É uma ótima maneira de entender os conceitos básicos de contêineres, orquestração e como suas aplicações podem viver no Kubernetes!

✨ O Que Este Projeto Faz?
Contêineres Docker: Empacota o Nginx e o Apache, juntamente com suas páginas HTML personalizadas, em imagens Docker leves.

Orquestração com Kubernetes: Utiliza manifestos YAML para definir como essas aplicações devem ser implantadas, gerenciadas e expostas dentro de um cluster Kubernetes.

Ambiente Local: Tudo configurado para rodar facilmente na sua máquina, ideal para aprendizado e testes.

🛠️ Tecnologias Utilizadas
Docker: Para construir e gerenciar as imagens dos contêineres.

Kubernetes (K8s): O orquestrador de contêineres para gerenciar a implantação.

Nginx: Servidor web leve e de alta performance.

Apache HTTP Server: Servidor web robusto e amplamente utilizado.

YAML: Linguagem de marcação para os manifestos do Kubernetes.

🚀 Como Rodar (Passo a Passo)
Siga estes passos para colocar as aplicações no ar no seu cluster Kubernetes local:

Pré-requisitos:
Certifique-se de ter o Docker Desktop (com Kubernetes habilitado) ou Minikube instalado e configurado na sua máquina.

Clone o Repositório:

git clone https://github.com/Milleny-pin/Projeto_Kubernetes.git
cd seu-repositorio

Construa as Imagens Docker:
Navegue até os diretórios nginx-app e apache-app e construa as imagens:

# Para Nginx
cd nginx-app
docker build -t meu-nginx-app:1.0 .
cd ..

# Para Apache
cd apache-app
docker build -t meu-apache-app:1.0 .
cd ..

Certifique-se de que o Docker esteja rodando!

Aplique os Manifestos do Kubernetes:
Com seu contexto Kubernetes configurado para o cluster local, aplique os arquivos YAML:

kubectl apply -f kubernetes/nginx-deployment.yaml
kubectl apply -f kubernetes/apache-deployment.yaml

Verifique as Implantações:
Confira se os pods e serviços estão rodando:

kubectl get deployments
kubectl get pods
kubectl get services

Acesse as Aplicações:

Nginx: Acessível via http://localhost:<porta-do-nginx> (verifique a porta do serviço Nginx com kubectl get services).

Apache: Acessível via http://localhost:<porta-do-apache> (verifique a porta do serviço Apache com kubectl get services).

Se estiver usando Docker Desktop, as portas NodePort serão mapeadas para o localhost.

🧹 Limpeza (Opcional)
Para remover as aplicações do seu cluster:

kubectl delete -f kubernetes/nginx-deployment.yaml
kubectl delete -f kubernetes/apache-deployment.yaml

