# Minimum Viable Product  
## Демонстрація роботи ArgoCD
[![youtube](https://i9.ytimg.com/vi_webp/UWQXKywAitA/mq1.webp?sqp=CNS5hLEG-oaymwEmCMACELQB8quKqQMa8AEB-AH-CYAC0AWKAgwIABABGE4gYihlMA8=&rs=AOn4CLBFa_8mxQJdlObqidokdTPmXMK9mQ)](https://youtu.be/UWQXKywAitA)  
  
## Демонстрація роботи програми в середовищі Kubernetes  
Створюємо псевдоним для команди kubectl  
```bash
alias k=kubectl
```  
Перевіряємо наявні сервіси  
```bash
k get svc
```  
Активуємо порт для сервісу ambassador  
```bash
k port-forward -n demo svc/ambassador 8088:80
```  
Перевіряємо відповідь порту  
```bash
curl localhost:8088
```  
Завантажуємо файл з інтернету на комп'ютер  
```bash
wget -O /tmp/ua.png https://kampot.org.ua/uploads/img/avka/17.png
```  
Перевіряємо наявність і доступність файлу  
```bash
open /tmp/ua.png
```  
Даємо додатку скачаний малюнок і отримуємо бажаний результат в ascii graphics  
```bash
curl -F 'image=@/tmp/ua.png' localhost:8088/img/
```  
Демонстрація  
  
[![youtube](https://i9.ytimg.com/vi/J_z-brrT6V4/mq1.jpg?sqp=CKi3hLEG-oaymwEmCMACELQB8quKqQMa8AEB-AHUBoAC4AOKAgwIABABGEsgXyhlMA8=&rs=AOn4CLAROgKlvGitMA4fnMfv8z7QPMDSJw)](https://youtu.be/J_z-brrT6V4)