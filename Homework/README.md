# OOAD-WEEK08

## Use Case Diagram 

### Usecase1_Stockmarket
Code

```
@startuml
left to right direction
skinparam packageStyle rect
actor :Retail Customer:
actor Producer
actor Seller

rectangle {
:Producer: --> (Large Volume Buying)
:Retail Customer: --> (Retail Selling)
:Seller: --> (Large Volume Buying)
:Seller: --> (Retail Selling)
:Seller: --> (Inventory Monitoring)
(Retail Selling) <|-- (Instant Retail selling)
(Retail Selling) <|-- (Delivery Retail Selling)
(Receiving Order) <|-- (Delivery Retail Selling):<<user>>
(Receiving Order) <|-- (Receiving Order via Phone)
(Large Volume Buying) <|-- (Urgent Buying):<<extend>>
}
@enduml
```
Diagram

<img src="https://github.com/weerapat1995/OOAD-WEEK08/blob/master/Homework/use%20case1.png?raw=true">

###Usecase2_Webservice
Code
```
@startuml
left to right direction
skinparam packageStyle rect
actor :User:
actor :Web Service:

rectangle {
:User: --> (Put Data For Calculation)
:User: --> (Get LCA)
:User: --> (Select Inventory)
(Put Data For Calculation) <-- :Web Service:
(Get LCA) <-- :Web Service:
(Select Inventory) <-- :Web Service:
(Get Available) <|-- (Select Inventory):<<include>>

}
@enduml
```
Diagram

<img src="https://github.com/weerapat1995/OOAD-WEEK08/blob/master/Homework/use%20case2.png?raw=true">

###Usecase3_Hospital
Code
```
@startuml
left to right direction
:Patient: --> (Cure)
:Patient: --> (Pay)
:Patient: --> (Cancel)
:Patient: --> (appointments)
(Cure) <-- :Doctor:
(Pay) <-- :Cashier:
(Cancel) <-- :Manager:
(appointments) <-- :Manager:
@enduml
```
Diagram

<img src="https://github.com/weerapat1995/OOAD-WEEK08/blob/master/Homework/use%20case3.png?raw=true">

###Usecase4_Scienceclassroom
Code 
```
@startuml
left to right direction
skinparam packageStyle rect
actor :Student:
actor :Teacher:
actor :authorities:

rectangle Scienceclassroom {
:Student: --> (Studying)
:Teacher: --> (Studying)
(Studying) --|> (Uses Scienceclassroom) :<<Uses>>
(Care Scienceclassroom) <-- :authorities:

}
@enduml
```

Diagram

<img src="https://github.com/weerapat1995/OOAD-WEEK08/blob/master/Homework/use%20case4.png?raw=true">

###Usecase5_PizzaShop
Code
```
@startuml
left to right direction
skinparam packageStyle rect
actor :Employe:
actor :Manager:
actor :Customer:
actor :Casher:

rectangle PizzaShopSystem {
:Employe: --> (Show Menu)
:Employe: --> (Select Menu)
:Employe: --> (Send Product)
:Manager: --> (Make Report)
(Show Menu) <-- (Customer)
(Select Menu) <-- (Customer)
(Send Product) <-- (Customer)
(Make Report) <-- (Casher)
(Calculate) <-- (Casher)
}
@enduml
```

Diagram

<img src="https://github.com/weerapat1995/OOAD-WEEK08/blob/master/Homework/use%20case5.png?raw=true">

