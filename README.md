c4-model
# C4 Model

Based on "C4-PlantUML" at https://github.com/plantuml-stdlib/C4-PlantUML

Based on "Intro to C4 Architecture Diagrams and C4 PlantUML extension" at https://www.youtube.com/watch?v=n-e1FDAtBuM

Based on "C4 Model with PlantUML" at https://medium.com/software-architecture-foundations/software-architecture-modeling-with-c4-model-e9e61d952121

Based on "Diagrams as Code – C4 diagrams with Azure icons" at https://andysprague.com/2023/01/11/diagrams-as-code-c4-diagrams-with-azure-icons/

Based on "sprague.andy.plantuml.c4" at https://github.com/andysprague44/sprague.andy.plantuml.c4

Based on "Plant UML in Visual Studio Code // Config file" at https://stackoverflow.com/questions/66709936/plant-uml-in-visual-studio-code-config-file?rq=1

C4-PlantUML combines the benefits of PlantUML and the C4 model for providing a simple way of describing and communicate software architectures. The addition of Azure icons helps to visualize Azure systems too.

## 100 - Introduction

Read "Diagrams as Code – C4 diagrams with Azure icons" at https://andysprague.com/2023/01/11/diagrams-as-code-c4-diagrams-with-azure-icons/

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

Install extension 'plantuml' and leave all default settings. Test correct installation by opening testdot.wsd and previewing with Alt + D. Should see preview with PlantUML version, and message "Installion seems OK". 

**Note**: If you have not installed GraphViz first, you may get an error as a message instead of an OK.

### To update diagram

- Open the relevant .wsd file
- Preview with Alt + D (or, right-click -> Preview Current Diagram)
- Once done, right click - > Export Current Diagram, choose png format
- View rendered diagram in 'out' folder

### To generate custom sprites

See <https://plantuml.com/sprite> e.g.
- java -jar plantuml.jar -encodesprite 16z prius.svg   

If plantuml.jar is not on your PATH, look for it in a folder 

java -jar "C:\Program Files\PlantUML\plantuml.jar" -encodesprite 16z prius.svg 

## 300 - Building Our Application

Preview Diagram, whilst your cursor is active inside of your pulm file between the @startuml and @enduml syntax Press Alt + D to start PlantUML preview (option + D on MacOS).

Also you can generate images from your puml files (e.g. ```C1_SystemContext.wsd```) as follows:

```
$ cd containers/app/c4plantuml/docs/diagrams
$ java -jar plantuml-1.2023.10.jar C1_SystemContext.wsd
```

**TIP**: Help with plantuml can be retrieved as follows: ```$ java -jar plantuml-1.2023.10.jar -h```

An updated image with the name of the diagram (see first line inside file, e.g. "@startuml C1_My_Example_Platform_SystemContext") will be autogenerated in the ```out``` directory with the latest changes reflected, e.g. C1_SystemContext/C1_My_Example_Platform_SystemContext.png.

![C1_My_Example_Platform_SystemContext.png](https://github.com/vanHeemstraSystems/c4-model/blob/main/containers/app/c4plantuml/docs/diagrams/C1_SystemContext/C1_My_Example_Platform_SystemContext.png)

out/C1_SystemContext/C1_My_Example_Platform_SystemContext.png

## 400 - Conclusion
