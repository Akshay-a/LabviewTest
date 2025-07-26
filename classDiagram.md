Class Diagram for Scientific Computations Project
Below is the class diagram describing the classes in the LabVIEW project, rendered using PlantUML syntax.
@startuml
' Define the Calculation class
class Calculation {
  +Input A: Double
  +Input B: Double
  +Input C: Double
  +Calculate(): Double
}

' Note about the Main VI
note right of Calculation
  Main.vi is not a class but a VI that uses
  an instance of Calculation for computation
  and provides the UI.
end note

' Relationships
Main --> Calculation : instantiates and uses

@enduml

Description

Calculation Class:
Attributes:
Input A: Double: Coefficient A for the quadratic formula.
Input B: Double: Coefficient B for the quadratic formula.
Input C: Double: Coefficient C for the quadratic formula.


Methods:
Calculate(): Double: Computes the quadratic formula result using inputs A, B, and C.




Main VI:
Not a class, but a LabVIEW VI that serves as the user interface.
Instantiates and interacts with the Calculation class to perform computations.
Contains front panel controls (A, B, C, Calculate button, Stop button) and an indicator (Result).



This diagram keeps the structure minimal, reflecting the simplicity of the project while clearly documenting the OOP components and their interactions.
