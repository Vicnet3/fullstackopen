```mermaid
sequenceDiagram
    participant browser
    participant server
    
    Note right of browser: the user accesses the spa page
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa
    server-->>browser: response html document
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server-->>browser: response http 200 to /main.css
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/spa.js
    server-->>browser: response http 200 to /spa.js
    browser->>server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    server-->>browser: response http 200 to /data.json
