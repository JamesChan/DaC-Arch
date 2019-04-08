@startuml

rectangle "Capture Information" as ci <<$archimate/business-process>> #yellow

rectangle "Service A" as ServiceA <<$archimate/application-service>>

rectangle "Interface B" as IF_B <<$archimate/application-interface>>

rectangle "XXX" as XXX <<$archimate/application-component>>

rectangle "FM A" as FM_A <<FM>> 

XXX .up.|> ServiceA
XXX .up.|> IF_B


@enduml
