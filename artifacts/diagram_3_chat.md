# Диаграмма 3: Class Diagram - Система управления персоналом

## Промпт:
Представь, что ты системный архитектор. Напиши мне код для Mermaid диаграммы типа Class Diagram, которая описывает систему управления персоналом. Включи базовый класс Person с атрибутами (name, salary, department), классы-наследники Employee, Manager и Director. Добавь методы getSalary() и getBonus(). Покажи связь где Manager имеет список Employees. Обязательно добавь комментарий 'Author: GeoExe'.

## Ответ (сгенерировано Claude Haiku):

```mermaid
classDiagram
    class Person {
        #name: string
        #salary: float
        #department: string
        +getSalary() float
        +getDepartment() string
    }
    
    class Employee {
        #employeeId: string
        +getBonus() float
        +getDetails() string
    }
    
    class Manager {
        #teamSize: int
        +getBonus() float
        +addEmployee(emp: Employee)
        +removeEmployee(empId: string)
        +getTeamSalary() float
    }
    
    class Director {
        #bonus: float
        +getBonus() float
        +addDivision(manager: Manager)
        +getCompanySalary() float
    }
    
    Person <|-- Employee: наследование
    Person <|-- Manager: наследование
    Person <|-- Director: наследование
    Manager "1" --> "*" Employee: управляет
    Director "1" --> "*" Manager: управляет
```
