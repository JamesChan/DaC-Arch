调用 http://www.plantuml.com/plantuml/proxy 进行在线渲染

image is here as followed:

![](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.github.com/plantuml/plantuml-server/master/src/main/webapp/resource/test2diagrams.txt)


![](http://www.plantuml.com/plantuml/proxy?cache=no&src=https://raw.githubusercontent.com/JamesChan/DaC-Arch/master/PlantUML/component-view.puml)


Picure by Drawio:

![](./test_drawio_pic.dio.svg)

Test PlantUML embeded in MD:

方法1：

```plantuml
@startuml
Bob->Alice: This is a test
@enduml
```

方法2：

```plantuml
@startuml
!includeurl https://raw.githubusercontent.com/linux-china/plantuml-gist/master/src/main/uml/plantuml_gist.puml
@enduml
```