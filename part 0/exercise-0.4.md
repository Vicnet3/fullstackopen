sequenceDiagram
    participant browser
    participant server
    
    note right of browser: the user write and click in save
    browser ->> server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    server -->> browser: redirection http 302 to /notes
    browser ->> server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    server -->> browser: response html document
    browser ->> server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server -->> browser: response http 200 to /main.css
    browser ->> server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    server -->> browser: response http 200 to /main.js
    browser ->> server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server -->> browser: response http 200 to /data.json


    





