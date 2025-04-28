University: ITMO University

Faculty: FTMI

Course: Cloud platforms as the basis of technology entrepreneurship

Year: 2024/2025

Group: UVB

Author: Silinik Elizaveta Sergeevna

Lab: Lab2

Date of create: 26.04.2025

Date of finished: 26.04.2025
1. Заходим в Cloud Run на Google Cloud Platform и нажимаем на Deploy
![image](https://github.com/user-attachments/assets/cac90f8a-8c3c-48bc-97c9-ad393bca3467)
2. Используем существующий сервис hello и выставим минимальные настройки сервиса. Установим 8080 порт. Даем доступ неавторизованным пользователям.
![image](https://github.com/user-attachments/assets/74740f8a-d361-409e-a994-b403ea96e037)
![image](https://github.com/user-attachments/assets/138d844e-418a-461c-8319-d80b3db401e7)
![image](https://github.com/user-attachments/assets/5644de63-1a1c-4cbc-a0b4-59bf46f0de85)
3. Проверяем, что сервис запущен
![image](https://github.com/user-attachments/assets/d10a0e00-49f1-4473-9f16-3921529b4a29)
![image](https://github.com/user-attachments/assets/9e8329fc-9b9c-47da-a2f5-299791799319)
4. Проверяем текущие Logs и Metrics
![image](https://github.com/user-attachments/assets/733f3d9b-fb1f-4711-b293-34401013ab40)
![image](https://github.com/user-attachments/assets/37913e95-03be-4e47-ba79-8b4b826b60ed)
5. Выставляем для данного Cloud Run 8090 порт и трафик на 50%
![image](https://github.com/user-attachments/assets/23fb99ee-a8b1-41a9-b7b7-0d6b79d3d3b0)
6. В логах видно, что контейнер теперь запускает порт 8090. Произошло обновление ReplaceService, после чего контейнер выводит сообщение о старте на новом порту
![image](https://github.com/user-attachments/assets/1f6828fd-fd76-4e2d-ac93-c3b5049897b2)
![image](https://github.com/user-attachments/assets/91f5d98b-8c8b-4df7-90a0-8f09f37b07ba)
![image](https://github.com/user-attachments/assets/7575227e-daa2-4345-8a94-5fcd1ae017dd)
![image](https://github.com/user-attachments/assets/8903a46a-9e77-4142-adac-0713355333e9)
