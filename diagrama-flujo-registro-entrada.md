
## Diagrama Mermaid

## Diagrama Mermaid

```mermaid
flowchart TD
    A([Inicio: Usuario abre la aplicacion]) --> B[Capturar hora de entrada y coordenadas]
    B --> C{Hora de entrada antes de las 08:00?}
    C -->|Si| D{Ubicacion dentro del area de trabajo hasta 50m?}
    C -->|No| F["Registrado<br>Advertencia"]
    D -->|Si| E["Registrado<br>OK"]
    D -->|No| F
    E --> G([Fin])
    F --> G

    classDef ok fill:#90EE90,stroke:#006400,color:#000000,font-weight:bold
    classDef advertencia fill:#FF6961,stroke:#8B0000,color:#000000,font-weight:bold
    class E ok
    class F advertencia
