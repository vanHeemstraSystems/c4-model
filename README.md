c4-model
# C4 Model

Based on "C4-PlantUML" at https://github.com/plantuml-stdlib/C4-PlantUML

Based on "Intro to C4 Architecture Diagrams and C4 PlantUML extension" at https://www.youtube.com/watch?v=n-e1FDAtBuM

Based on "C4 Model with PlantUML" at https://medium.com/software-architecture-foundations/software-architecture-modeling-with-c4-model-e9e61d952121

C4-PlantUML combines the benefits of PlantUML and the C4 model for providing a simple way of describing and communicate software architectures

## 100 - Introduction

## 200 - Requirements

- PlantUML Extension for Visual Studio Code

**How to install**
Launch VS Code Quick Open (Ctrl+P), paste the following command, and press enter.

```
ext install plantuml
```

Also Graphviz is required. On Linux you can install Graphviz as follows:

```
$ sudo apt install graphviz
```

## 300 - Building Our Application

Preview Diagram, whilst your cursor is active inside of your pulm file between the @startuml and @enduml syntax Press Alt + D to start PlantUML preview (option + D on MacOS).

Also you can generate images from your puml files (e.g. ```context.puml```) as follows:

```
$ cd containers/app/c4plantuml
$ java -jar plantuml-1.2023.10.jar context.puml
```

An updated image with the name of the diagram (see first line inside file, e.g. "@startuml autoware-context") will be autogenerated with the latest changes reflected, e.g. autoware-context.png.

![autoware-context.png](https://github.com/vanHeemstraSystems/c4-model/blob/main/containers/app/c4plantuml/autoware-context.png)

autoware-context.png

## 400 - Conclusion
