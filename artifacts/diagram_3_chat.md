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
        #team: List~Employee~
        +getBonus() float
        +addEmployee(emp: Employee)
        +removeEmployee(empId: string)
        +getTeamSalary() float
    }
    
    class Director {
        #divisions: List~Manager~
        +getBonus() float
        +addDivision(manager: Manager)
        +getCompanySalary() float
    }
    
    Person <|-- Employee
    Person <|-- Manager
    Person <|-- Director
    Manager "1" --> "*" Employee: manages
    Director "1" --> "*" Manager: oversees
    
    Note: "Author: GeoExe<br/>Иерархия управления<br/>персоналом компании"
```
