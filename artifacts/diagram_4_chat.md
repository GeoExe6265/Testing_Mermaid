# Диаграмма 4: ER Diagram - Система управления университетом

## Промпт:
Представь, что ты системный архитектор. Напиши мне код для Mermaid диаграммы типа ER Diagram, которая описывает систему управления университетом. Включи сущности: Student, Course, Professor, Department, Grade. Покажи отношения: Student зарегистрирован на Course, Professor преподает Course, Course принадлежит Department, Student получает Grade за Course. Добавь основные атрибуты каждой сущности. Обязательно добавь комментарий 'Author: GeoExe'.

## Ответ (сгенерировано Claude Haiku):

```mermaid
erDiagram
    DEPARTMENT ||--o{ COURSE : contains
    DEPARTMENT ||--o{ PROFESSOR : employs
    PROFESSOR ||--o{ COURSE : teaches
    STUDENT ||--o{ GRADE : receives
    COURSE ||--o{ GRADE : awards
    STUDENT ||--o{ COURSE : enrolls

    DEPARTMENT {
        int dept_id PK
        string name
        string head_name
        string location
    }

    PROFESSOR {
        int prof_id PK
        string name
        string email
        int dept_id FK
        string specialization
    }

    COURSE {
        int course_id PK
        string title
        string code
        int dept_id FK
        int prof_id FK
        int credits
    }

    STUDENT {
        int student_id PK
        string name
        string email
        string address
        int enrollment_year
    }

    GRADE {
        int grade_id PK
        int student_id FK
        int course_id FK
        string letter_grade
        float gpa_points
        string semester
    }
    
    note "Author: GeoExe"
```
