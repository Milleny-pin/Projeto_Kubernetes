```markdown
# 🚀 Kubernetes Web Apps: Nginx & Apache no Seu Cluster Local! 🌐

Este projeto demonstra a implantação de **duas aplicações web simples** – um servidor **Nginx** e um servidor **Apache** – em um ambiente **Kubernetes local**.

É uma ótima maneira de aprender os conceitos básicos de **contêineres**, **orquestração** e como suas aplicações podem viver no Kubernetes!

---

## ✨ O Que Este Projeto Faz?

- 🐳 **Contêineres Docker:** Empacota o Nginx e o Apache, juntamente com suas páginas HTML personalizadas, em imagens Docker leves.
- ☸️ **Orquestração com Kubernetes:** Utiliza manifestos YAML para definir como essas aplicações devem ser implantadas, gerenciadas e expostas.
- 💻 **Ambiente Local:** Tudo configurado para rodar facilmente na sua máquina, ideal para aprendizado e testes.

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia             | Descrição                                                                 |
|------------------------|---------------------------------------------------------------------------|
| 🐳 **Docker**          | Para construir e gerenciar as imagens dos contêineres.                    |
| ☸️ **Kubernetes (K8s)**| Orquestrador de contêineres para gerenciar as aplicações.                 |
| 🌐 **Nginx**           | Servidor web leve e de alta performance.                                  |
| 🔥 **Apache HTTP Server** | Servidor web robusto e amplamente utilizado.                         |
| 📄 **YAML**            | Linguagem de marcação para os manifestos do Kubernetes.                   |


---

## 🚀 Como Rodar (Passo a Passo)

### ✅ Pré-requisitos

- Docker Desktop (com Kubernetes habilitado) **ou** Minikube instalado e configurado.

---

### 📦 1. Clone o Repositório

```bash
git clone https://github.com/Milleny-pin/Projeto_Kubernetes.git
cd Projeto_Kubernetes
```

---

### 🐳 2. Construa as Imagens Docker

#### Para Nginx

```bash
cd nginx-app
docker build -t meu-nginx-app:1.0 .
cd ..
```

#### Para Apache

```bash
cd apache-app
docker build -t meu-apache-app:1.0 .
cd ..
```

> Certifique-se de que o Docker esteja rodando! 🐳

---

### ☸️ 3. Aplique os Manifestos do Kubernetes

Com o cluster local ativo, execute:

```bash
kubectl apply -f kubernetes/nginx-deployment.yaml
kubectl apply -f kubernetes/apache-deployment.yaml
```

---

### 🔍 4. Verifique as Implantações

```bash
kubectl get deployments
kubectl get pods
kubectl get services
```

---

### 🌐 5. Acesse as Aplicações

- **Nginx:** Acesse via  
  `http://localhost:<porta-do-nginx>`
  
- **Apache:** Acesse via  
  `http://localhost:<porta-do-apache>`

> Use `kubectl get services` para descobrir as portas.  
> Se estiver usando **Docker Desktop**, as portas do tipo `NodePort` serão mapeadas automaticamente para o `localhost`.

---

## 🧹 Limpeza (Opcional)

Remova os recursos do cluster com:

```bash
kubectl delete -f kubernetes/nginx-deployment.yaml
kubectl delete -f kubernetes/apache-deployment.yaml
```

---

### 🐳📦 Feito com Docker, Kubernetes e Café ☕  
Divirta-se explorando o mundo dos contêineres!
```
