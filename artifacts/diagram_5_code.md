```mermaid
gantt
    title Разработка веб-приложения (Author: GeoExe)
    dateFormat YYYY-MM-DD
    
    section Design
    UI/UX Design           :design, 2024-01-01, 14d
    
    section Frontend
    Setup & Architecture   :frontend1, after design, 3d
    Component Development  :frontend2, after frontend1, 7d
    Integration Testing    :frontend3, after frontend2, 3d
    
    section Backend
    API Design & Setup     :backend1, after design, 5d
    Database Schema        :backend2, after backend1, 5d
    API Endpoints          :backend3, after backend2, 7d
    
    section QA
    Integration Tests      :test1, after frontend3 backend3, 5d
    Performance Testing    :test2, after test1, 5d
    
    section Deployment
    Staging Deploy         :deploy1, after test2, 3d
    Production Release     :deploy2, after deploy1, 2d
    
    milestone Project Start, 2024-01-01, 0d
    milestone Go Live, 2024-02-21, 0d
```
