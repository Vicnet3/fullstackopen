sequenceDiagram
    participant browser
    participant server
    
    note right of browser: the user write and click in save
    browser ->> server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    server -->> browser: response http 201 created
