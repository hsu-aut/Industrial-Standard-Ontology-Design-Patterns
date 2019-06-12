The ANSl/ISA-TR88.00.02-2015 [1] technical report is intended to build upon and formalize the concepts of the PackML guidelines 
and to show application examples. PackML is used to provide a standard description of states for comparison of machine statuses 
among different types of machines. The concepts used in this standard describe general states and transitions of a 
packaging machine, but could be used to describe the states and transitions of any machine. This is due to the reason, 
that the state machine is very generic and does not hold any concept specific to packaging machines.

There are mainly three separate state machines (see Fig. 1):
* Active, with two main sub-states:
  * Acting state: States which represents some processing activity
  * Wait state: States used to identify that a machine has achieved a defined set of conditions
* Stopping: states and transitions that result in a stopped machine
* Aborting: states and transitions that result in an aborted machine program

A detailed description of all states can be found in the rdfs:comment of the ODP or the standard [ANSl/ISA ANSl/ISA-TR88.00.02-2015].

![](./pictures/ISA88_SM1.png?raw=true "ISA 88 State Machine")<br></br>
Figure 1: PackML state machine overview

Fig. 2 shows the states that are contained within the “Active” state machine of Fig. 1. The state machine contains PackML 
defined states and transitions. Transitions called „SC“ do fire as soon as the state is complete. The state „Held“ represents 
the interrupt of executing because of internal disturbances, while the „Suspended“ state reflects the interrupt because of 
external disturbances.

![](./pictures/ISA88_SM2.png?raw=true "ISA 88 State Machine")<br></br>
Figure 2: PackML main state machine

Exemplary Competency Questions that could be answered with this ODP:<br></br>
Table 1: Example Competency Questions
![](./pictures/ISA88_exCQ.png?raw=true "exampleCQ")

[1] ANSl/ISA-TR88.00.02-2015] ANSl/ISA-TR88.00.02-2015. Machine and Unit States: 
An implementation example of ANSl/ISA-88.00.01, 02.2015.
