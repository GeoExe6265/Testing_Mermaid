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
