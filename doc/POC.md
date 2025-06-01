# Proof of Concept: Розгортання ArgoCD у кластері Kubernetes

## Інструкція

### 1. Створити namespace для ArgoCD:

```bash
kubectl create namespace argocd
```

### 2. Встановити ArgoCD через офіційний YAML:

```bash
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

### 3. Отримати пароль для користувача `admin`:

```bash
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```

### 4. Зробити port-forwarding для api-серверу:

```bash
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

### 5. Відкрити у браузері інтерфейс ArgoCD:

```
http://localhost:8080
```

### 6. Ввести логін та пароль:

* **Username:** `admin`
* **Password:** (отриманий на кроці 3)
