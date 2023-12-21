# kube-demo

Что реализовано:
1. Простейший сервис
2. Подготовлены Kubernetes манифесты для развертывания приложения
3. Автоматизирован процесс развертывания сервиса через Github Actions
   
Запуск проекта на локальной машине:
Нужны предустановленные `kubectl`, `minikube` и `docker`
```
minikube start
eval $(minikube -p minikube docker-env)
docker build . -t myapp:latest
kubectl apply -f ./manifests
minikube service myapp-service
```
Проверка автоматизации:  
Успешное измение:  
![Image](https://github.com/m0rk0vka/images/raw/main/kube-demo/success.png)  
До:  
![Image](https://github.com/m0rk0vka/images/raw/main/kube-demo/before.png)  
После:  
![Image](https://github.com/m0rk0vka/images/raw/main/kube-demo/after.png)  
Уточнения:
1. Так как в задании вы попросили создание просто сервиса, то решил ограничиться простым `hello world`.
2. У меня много примеров сервисов с использованием различных библиотек и баз данных на github.
3. В новинку как раз было разобраться с развертыванием в Kubernetes и автоматизацией развертывания сервиса через GitHub Actions.
