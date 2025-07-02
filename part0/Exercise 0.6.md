sequenceDiagram
    participant browser
    participant server

    Note over browser: El usuario escribe una nota y pulsa "Save"

    Note right of browser: JavaScript recoge el contenido del input y crea un objeto nota

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: 201 Created
    deactivate server
