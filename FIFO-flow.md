graph TD
    A[Inicio] --> B[Recibir solicitud de reserva]
    B --> C{¿Hay asientos disponibles?}
    C -- Sí --> D[Asignar asiento al pasajero]
    D --> E[Actualizar cantidad de asientos disponibles]
    E --> F[Fin]

    C -- No --> G[Agregar pasajero a la cola de espera]
    G --> F

    F --> H[¿Se devuelve un asiento?]
    H -- Sí --> I[Actualizar cantidad de asientos disponibles]
    I --> J{¿Hay pasajeros en la cola de espera?}
    J -- Sí --> K[Asignar asiento devuelto al siguiente pasajero]
    K --> L[Actualizar cola de espera]
    L --> F
    J -- No --> F
    H -- No --> F
