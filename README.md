# Kubernetes Apache Web App Lab

## 📌 Objective
To deploy and manage an Apache web application using Kubernetes.

---

## 🚀 Steps Performed

1. Created a deployment using Apache (httpd) image  
2. Exposed deployment using a NodePort service  
3. Accessed the application using port-forward  
4. Scaled the deployment to multiple replicas  
5. Introduced an error using wrong image  
6. Diagnosed the issue using `kubectl describe`  
7. Fixed the deployment image  
8. Verified Kubernetes self-healing by deleting a pod  

---

## ⚙️ Commands Used

-bash
kubectl create deployment apache --image=httpd
kubectl expose deployment apache --port=80 --type=NodePort
kubectl get pods
kubectl scale deployment apache --replicas=2
kubectl set image deployment/apache httpd=wrongimage
kubectl describe pod <pod-name>
kubectl set image deployment/apache httpd=httpd
kubectl delete pod <pod-name>

📊 Observations
Pods were created successfully
Application was accessible via port-forward
Scaling created multiple pods
Wrong image caused ImagePullBackOff error
Deployment recovered after fixing the image
Kubernetes recreated deleted pods automatically

✅ Conclusion
Kubernetes provides powerful features such as:

Easy deployment
Scaling applications
Self-healing capabilities
Efficient failure management
📸 Screenshots

(All screenshots are included in the repository)

🧠 Key Learning
Deployment ensures self-healing
Port-forward is only for debugging
Services expose applications
Scaling improves availability
