@startuml
title logical view mapped to physical view
sprite $aService jar:archimate/application-service
sprite $aAppComponent jar:archimate/application-component
sprite $aComponent jar:archimate/component
sprite $aFunction jar:archimate/function
sprite $aInterface jar:archimate/interface

legend left
实现架构(逻辑视图到物理视图之间实现映射关系)图例
<$aInterface> : Interface（逻辑架构图元）
<$aService> : Service（逻辑架构图元）
<$aFunction>：FM（逻辑架构图元主要对象，SASD方法下的逻辑功能/OOAD方法下的主动类）
<$aComponent> : Component（物理架构图元之一：对应so/dll等一般开发态最小物理颗粒）
<$aAppComponent>: Application Component(物理架构图元之一:对应RPM、特性组件等部署态物理对象)
endlegend

rectangle "Capture Information" as ci <<$archimate/business-process>> #yellow

rectangle "Service A" as ServiceA <<$archimate/application-service>>

rectangle "Interface B" as IF_B <<$archimate/application-interface>>
rectangle "Interface A" as IF_A <<$archimate/application-interface>>

IF_B -up-|> IF_A

rectangle "YYY" as YYY <<$archimate/application-component>>

rectangle "XXX\nThis is XXX component" as XXX <<$archimate/application-component>>
rectangle "FM A\nThis is a functional module\nimplemented by XXX component" as FM_A <<FM>>

rectangle "FM B\nThis is a functional module\nimplemented also by XXX component" as FM_B <<FM>>

XXX .up.|> ServiceA
XXX .up.|> IF_B
YYY .up.|> IF_A
YYY ..> ServiceA
XXX --> FM_A
XXX --> FM_B

@enduml


参考：http://plantuml.com/zh/archimate-diagram