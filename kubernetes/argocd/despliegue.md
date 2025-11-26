# 🚀 Despliegue rápido de Argo CD con Helm (NodePort)

## Instalar Argo CD

```bash
helm repo add argo https://argoproj.github.io/argo-helm
helm repo update
kubectl create namespace argocd
helm install argocd argo/argo-cd -n argocd --create-namespace --set server.service.type=NodePort --set server.service.nodePort=30080
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d
kubectl get svc -n argocd
kubectl get nodes -o wide
helm uninstall argocd -n argocd

---

Solo copia todo esto en un archivo `argocd.md` y lo tendrás perfecto 📌  
¿Quieres que también te ponga la parte de **cómo acceder a la UI con NodePort** y **cambiar la contraseña del admin**? 😎
