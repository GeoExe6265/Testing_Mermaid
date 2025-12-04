# Диаграмма 5: Gantt Chart - Разработка веб-приложения

## Промпт:
Представь, что ты системный архитектор. Напиши мне код для Mermaid диаграммы типа Gantt Chart, которая описывает этапы разработки веб-приложения. Включи: Дизайн (2 недели) → Фронтенд разработка (3 недели, после дизайна) → Бэкенд разработка (4 недели, параллельно с фронтенд) → Тестирование (2 недели, после обоих) → Развертывание (1 неделя). Покажи зависимости и параллельные процессы. Добавь комментарий 'Author: GeoExe' в заголовок.

## Ответ (сгенерировано Claude Haiku):

```mermaid
gantt
    title Разработка веб-приложения (Author: GeoExe)
    dateFormat YYYY-MM-DD
    
    section Design
    UI/UX Design           :des1, 2024-01-01, 14d
    
    section Frontend
    Setup & Architecture   :fe1, after des1, 3d
    Component Development  :fe2, after fe1, 7d
    Integration Testing    :fe3, after fe2, 3d
    
    section Backend
    API Design & Setup     :be1, after des1, 5d
    Database Schema        :be2, after be1, 5d
    API Endpoints          :be3, after be2, 7d
    
    section QA
    Integration Tests      :qa1, after fe3, 5d
    Performance Testing    :qa2, after qa1, 5d
    
    section Deployment
    Staging Deploy         :dep1, after qa2, 3d
    Production Release     :dep2, after dep1, 2d
```
