University: ITMO University

Faculty: FTMI

Course: Cloud platforms as the basis of technology entrepreneurship

Year: 2024/2025

Group: UVB

Author: Silinik Elizaveta Sergeevna

Lab: Lab2

Date of create: 05.05.2025

Date of finished: 05.05.2025

В рамках лабораторной работы рассматривается пример приложения (AI-чатбот для поддержки клиентов) с тремя стадиями жизненного цикла:
- Начальная разработка
- Тестирование партнерами
- Продовое (production) решение

1. Начальная разработка (100 пользователей/месяц):
- Только текстовые запросы
- Нет загрузки файлов
- Минимальная стоимость

Описание архитектуры:
- Firebase Hosting - Хостинг статичного фронтенда
- Cloud Functions (2nd Gen) - Бекенд
- Dialogflow ES - NLP-движок для простых сценариев
- Firestore - Хранение истории чатов

![image](https://github.com/user-attachments/assets/09e03dca-bfaa-45e6-afba-b843b0d88d84)
![image](https://github.com/user-attachments/assets/36708abf-ad5b-473b-aef7-771486b85d47)
Итого: $11.20

Обоснование:
- Firebase Hosting: нулевая стоимость для старта, мгновенное развертывание SPA (React/Vue).
- Cloud Functions: дешевле Cloud Run при низкой нагрузке. Не требует управления инфраструктурой.
- Dialogflow ES: не требует обучения моделей. Подходит для простых диалогов
- Firestore: проще и дешевле Cloud SQL для хранения истории чатов

2. Тестирование партнерами (1000 пользователей/месяц): 
- Добавлена загрузка файлов (скриншоты)
- Требуется аналитика диалогов
- Рост нагрузки

Изменение:
- Замена Cloud Functions → Cloud Run: гибкость (можно добавить кастомные ML-модели). Дешевле GKE для средних нагрузок.
- Замена Dialogflow ES → Vertex AI: точность выше, чем у Dialogflow ES. Возможность дообучения под специфичные задачи.
- Замена Firestore → Cloud SQL: необходим для сложных SQL-запросов (аналитика пользователей).
- Memorystore (Redis): уменьшает нагрузку на БД для частых запросов (например, повторяющиеся вопросы)
- Cloud Storage: появилась загрузка файлов
![image](https://github.com/user-attachments/assets/168c3df1-b025-4f53-ad50-b6a8f700cc99)
![image](https://github.com/user-attachments/assets/162f0296-04cb-474d-9db4-a277c12561b9)
Итого: $151

3. Продовое решение (5000 пользователей/месяц)
- Добавлена загрузка файлов (скриншоты)
- Требуется аналитика диалогов
- Рост нагрузки

Изменение:
- Замена Vertex AI → Gemini Nano: для сложных запросов ($0.00025/1K токенов).
- Замена Firebase Hosting → Cloud CDN: уменьшает задержку для глобальной аудитории
- Замена Cloud SQL → Cloud SQL (HA): отказоустойчивость при росте нагрузки
![image](https://github.com/user-attachments/assets/01478767-baf7-4079-9775-57cba96b6453)
![image](https://github.com/user-attachments/assets/8e0e9ad3-1fa8-4d09-b9c5-2fe1810f11a4)
Итого: $490.50
