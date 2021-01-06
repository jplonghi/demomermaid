# Mermaid

---

## Documentation

+ [Mermaid](https://mermaid-js.github.io/mermaid/#/)
+ [Live Editor](https://mermaid-js.github.io/mermaid-live-editor/)
+ [Markdown](https://www.markdownguide.org/basic-syntax/)
+ [Markdown Extended](https://www.markdownguide.org/extended-syntax/)

## Browser extensions

+ [Google Chrome and Microsoft Edge Extension](https://chrome.google.com/webstore/detail/mermaid-diagrams/phfcghedmopjadpojhmmaffjmfiakfil/)

## VSCode extensions

+ [Mermaid Editor](https://marketplace.visualstudio.com/items?itemName=tomoyukim.vscode-mermaid-editor)
+ [SVG Viewer](https://marketplace.visualstudio.com/items?itemName=cssho.vscode-svgviewer)

## Other

+ [Jira Feature Request](https://jira.atlassian.com/browse/BCLOUD-18559)
+ [Mermaid Plugin for Confluence](https://marketplace.atlassian.com/apps/1214124/mermaid-plugin-for-confluence?hosting=server&tab=overview)
+ [Mermaid Integration for Confluence](https://marketplace.atlassian.com/apps/1222792/mermaid-integration-for-confluence?hosting=cloud&tab=overview)
+ [Mermaid Charts & Diagrams for Confluence](https://marketplace.atlassian.com/apps/1222572/mermaid-charts-diagrams-for-confluence?hosting=cloud&tab=overview)

---

## Sequence Diagram

```mermaid
sequenceDiagram
participant U as User
participant C as Client
participant S as Server
participant DB as Database

U ->> C: Fill username
U ->> C: Fill password
C ->> U: Enable "Login" button
U ->> C: Click "Login" button
C ->>+ S: POST /login
S ->>+ DB: SELECT FROM users
Note over S,DB: See login.py for impl. details
DB -->>- S: results
S -->>- C: { authenticated: true }
C ->> U: redirect /home
```

## Flowchart

```mermaid
graph LR

A(Start)

A --> B[Look for an item]

B --> C{Did you find it?}
C -->|Yes| D(Stop looking)
C -->|No| E{Do you need it?}
E -->|Yes| B
E -->|No| D
```

```mermaid
graph TB
A(Start)
A --> B[/Something/]
B --- C{{END}}

```

## State Diagrams

```mermaid
stateDiagram-v2
    [*] --> Still
    Still --> [*]

    Still --> Moving
    Moving --> Still
    Moving --> Crash
    Crash --> [*]
```

## Class Diagram

```mermaid
classDiagram
      Animal <|-- Duck
      Animal <|-- Fish
      Animal <|-- Zebra
      Animal : +int age
      Animal : +String gender
      Animal: +isMammal()
      Animal: +mate()
      class Duck{
          +String beakColor
          +swim()
          +quack()
      }
      class Fish{
          -int sizeInFeet
          -canEat()
      }
      class Zebra{
          +bool is_wild
          +run()
      }
```

```mermaid
classDiagram
class Square~Shape~{
    int id
    List~int~ position
    setPoints(List~int~ points)
    getPoints() List~int~
}

Square : -List~string~ messages
Square : +setMessages(List~string~ messages)
Square : +getMessages() List~string~
```

## Entity Relationship Diagrams

```mermaid
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE-ITEM : contains
    CUSTOMER }|..|{ DELIVERY-ADDRESS : uses
```
