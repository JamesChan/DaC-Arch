采用UML2.0标准的组件图，参考：http://plantuml.com/zh/component-diagram

```plantuml
@startuml
title 组件图

skinparam componentStyle uml2

package "Group A" as GA {
    [Component A]
    [Component B\nThis is Component B] as CompB #DDDDDD
    () "Interface B" as IF_B
}

note right of GB
    组件分类或物理子系统划分
end note

package "Group B" as GB #grey {
    component Comp3 #green
    [Component C] as CompC
    interface IF_C
    () "Interface A"
}

GA -[hidden]up- GB

note right of Comp3
    A note is 
    here
end note




interface "Interface D\nThis is interface D" as IF_D

note top of IF_D #red
    A note for interface D
end note


IF_B <- CompB
[Component A] .up.> IF_C: use
Comp3 - IF_C
CompB -down- IF_D
() "Interface A" -- Comp3
CompC ..> () "Interface A"


@enduml
```


