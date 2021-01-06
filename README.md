# Mermaid

---

+ [Mermaid](https://mermaid-js.github.io/mermaid/#/)
+ [Live Editor](https://mermaid-js.github.io/mermaid-live-editor/)
+ [Markdown](https://www.markdownguide.org/basic-syntax/)
+ [Markdown Extended](https://www.markdownguide.org/extended-syntax/)
+ [Mermaid Editor](https://marketplace.visualstudio.com/items?itemName=tomoyukim.vscode-mermaid-editor)
+ [SVG Viewer](https://marketplace.visualstudio.com/items?itemName=cssho.vscode-svgviewer)
+ [Jira Feature Request](https://jira.atlassian.com/browse/BCLOUD-18559)

---

## Sequence Diagram

![User Login Image](mermaid/userLoginDiagram.svg)

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

