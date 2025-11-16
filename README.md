<!-- BANNER DO PROJETO -->
<p align="center">
  <img src="https://img.shields.io/badge/KUBERNETES-WEB%20APPS-blue?style=for-the-badge&logo=kubernetes" />
  <img src="https://img.shields.io/badge/DOCKER-CONTAINERS-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/NGINX%20%2B%20APACHE-WEB%20SERVERS-green?style=for-the-badge&logo=nginx" />
</p>

<h1 align="center">🚀 Kubernetes Web Apps: Nginx & Apache no Seu Cluster Local! 🌐</h1>

<p align="center">
Este projeto demonstra a implantação de <b>duas aplicações web simples</b> — uma com <b>Nginx</b> e outra com <b>Apache</b> — executando em um <b>cluster Kubernetes local</b>.
<br>
É ideal para treinar conceitos de <b>contêineres</b>, <b>orquestração</b> e <b>deploy cloud-native</b>.
</p>

---

## ✨ O Que Este Projeto Faz?

- 🐳 **Contêineres Docker:** Empacota o Nginx e o Apache com páginas HTML personalizadas.  
- ☸️ **Orquestração com Kubernetes:** Manifests YAML definem deployments e services.  
- 💻 **Ambiente Local:** Funciona com Docker Desktop ou Minikube.

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Descrição |
|-----------|-----------|
| 🐳 **Docker** | Criação e gerenciamento das imagens. |
| ☸️ **Kubernetes (K8s)** | Orquestração dos serviços e pods. |
| 🌐 **Nginx** | Servidor web leve e rápido. |
| 🔥 **Apache** | Servidor web robusto e muito utilizado. |
| 📄 **YAML** | Linguagem usada nos manifests do Kubernetes. |

---

## 🚀 Como Rodar o Projeto

<details>
  <summary><b>📌 1. Pré-requisitos</b> (clique para expandir)</summary>
<br>

- Docker Desktop **com Kubernetes habilitado**, ou  
- Minikube instalado e configurado  
- Kubectl instalado  

</details>

---

<details>
  <summary><b>📦 2. Clone o Repositório</b></summary>
<br>

```bash
git clone https://github.com/Milleny-pin/Projeto_Kubernetes.git
cd Projeto_Kubernetes
</details>
<details> <summary><b>🐳 3. Construa as Imagens Docker</b></summary> <br>
🔹 Nginx
bash
Copiar código
cd nginx-app
docker build -t meu-nginx-app:1.0 .
cd ..
🔹 Apache
bash
Copiar código
cd apache-app
docker build -t meu-apache-app:1.0 .
cd ..
</details>
<details> <summary><b>☸️ 4. Aplique os Manifests do Kubernetes</b></summary> <br>
bash
Copiar código
kubectl apply -f kubernetes/nginx-deployment.yaml
kubectl apply -f kubernetes/apache-deployment.yaml
</details>
<details> <summary><b>🔍 5. Verifique o Status</b></summary> <br>
bash
Copiar código
kubectl get deployments
kubectl get pods
kubectl get services
</details>
<details> <summary><b>🌐 6. Acesse as Aplicações</b></summary> <br>
Nginx:
http://localhost:<porta-do-nginx>

Apache:
http://localhost:<porta-do-apache>

Use kubectl get services para verificar as portas expostas (NodePort).

</details>
🧹 Limpeza do Cluster
Remova tudo facilmente:

bash
Copiar código
kubectl delete -f kubernetes/nginx-deployment.yaml
kubectl delete -f kubernetes/apache-deployment.yaml
<p align="center"> 🐳☸️ Feito com <b>Docker</b>, <b>Kubernetes</b> e muito <b>Café ☕</b> <br> Aproveite para explorar ainda mais o mundo Cloud Native! </p> ```
