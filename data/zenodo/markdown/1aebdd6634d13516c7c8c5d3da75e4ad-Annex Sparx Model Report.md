| Annex Sparx Model Report  Version 1 |
| --- |
| |  | | --- | | Date/Time Generated: | 11/10/2020 5:05:21 PM | | Author: | Davide Basile (ISTI CNR Italy) | |
| | CREATED WITH |  | | --- | --- | |

Table of Contents

Model 3

Package1 3

ContextDefinition diagram 3

RBC2RBC diagram 3

Signals 4

*RBC\_USER\_CONNECT\_INDICATION 4*

*RBC\_USER\_DATA\_INDICATION 4*

*RBC\_USER\_DATA\_REQUEST 4*

*RBC\_USER\_DISCONNECT\_INDICATION 5*

*SAI\_CONNECT\_CONFIRM 5*

*SAI\_CONNECT\_INDICATION 5*

*SAI\_CONNECT\_REQUEST 5*

*SAI\_DATA\_INDICATION 5*

*SAI\_DATA\_REQUEST 6*

*SAI\_DISCONNECT\_INDICATION 6*

*SAI\_DISCONNECT\_REQUEST 6*

*SAI\_ERROR\_REPORT 6*

*sig 6*

*TICK 7*

CSL 7

*CSL 8*

CSL diagram 9

COMMS 9

NOCOMMS 14

Initial 18

RBC\_USER 18

*RBC\_USER 18*

RBC\_USER diagram 19

Stub 19

Initial 20

SAI 20

*SAI 20*

SAI diagram 21

Stub 21

Initial 22

RBC2RBC SI 22

*C\_CSL 23*

*C\_SAI 24*

*I\_SAI 24*

*C\_RBC\_USER 24*

*I\_CSL 25*

*I\_RBC\_USER 25*

# Model

Root Package

Model

Version Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 11/10/2020. Last modified 11/10/2020

## Package1

Package in package 'Model'

Package1

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/28/2020. Last modified 11/10/2020

### ContextDefinition diagram

Class diagram in package 'Package1'

The context definition identifies the CSL class that contains references to RBC\_USER class and SAI class.

ContextDefinition

Version 1.0

Davide Basile (ISTI CNR Italy) created on 10/1/2020. Last modified 11/10/2020



1. ContextDefinition

### RBC2RBC diagram

Class diagram in package 'Package1'

This diagram contains the executable state machine.

RBC2RBC

Version 1.0

Davide Basile (ISTI CNR Italy) created on 9/28/2020. Last modified 11/10/2020



1. RBC2RBC

### Signals

Package in package 'Package1'

Signals

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 9/29/2020

#### *RBC\_USER\_CONNECT\_INDICATION*

Trigger in package 'Signals'

Signal used by the CSL to inform the User about successful connection

RBC\_USER\_CONNECT\_INDICATION

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

#### *RBC\_USER\_DATA\_INDICATION*

Trigger in package 'Signals'

Signal used by the CSL to inform the User about incoming Data

RBC\_USER\_DATA\_INDICATION

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

#### *RBC\_USER\_DATA\_REQUEST*

Trigger in package 'Signals'

Signal used by the User to request the User send a data request to partner RBC (via SAI)

RBC\_USER\_DATA\_REQUEST

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

#### *RBC\_USER\_DISCONNECT\_INDICATION*

Trigger in package 'Signals'

Signal used by the User to request the User send a data request to partner RBC (via SAI)

RBC\_USER\_DISCONNECT\_INDICATION

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

#### *SAI\_CONNECT\_CONFIRM*

Trigger in package 'Signals'

Signal used by initiator SAI to inform initiator CSL about confirmation of connection

SAI\_CONNECT\_CONFIRM

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

#### *SAI\_CONNECT\_INDICATION*

Trigger in package 'Signals'

Signal used by called SAI to inform called CSL about connection with partner RBC

SAI\_CONNECT\_INDICATION

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

#### *SAI\_CONNECT\_REQUEST*

Trigger in package 'Signals'

Signal used by initiator CSL to ask to initiator SAI to open a connection with partner RBC

SAI\_CONNECT\_REQUEST

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

#### *SAI\_DATA\_INDICATION*

Trigger in package 'Signals'

Signal used by SAI to inform CSL about data received from partner RBC

SAI\_DATA\_INDICATION

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

#### *SAI\_DATA\_REQUEST*

Trigger in package 'Signals'

Signal used by CSL to request to SAI to send data to partner RBC

SAI\_DATA\_REQUEST

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

#### *SAI\_DISCONNECT\_INDICATION*

Trigger in package 'Signals'

Signal used by SAI to notify the CSL the disconnection

SAI\_DISCONNECT\_INDICATION

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

#### *SAI\_DISCONNECT\_REQUEST*

Trigger in package 'Signals'

Signal used by CSL to request to SAI to disconnect

SAI\_DISCONNECT\_REQUEST

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

#### *SAI\_ERROR\_REPORT*

Trigger in package 'Signals'

Signal used by SAI to report an error to CSL

SAI\_ERROR\_REPORT

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

#### *sig*

Signal in package 'Signals'

Generic type signal used for typing all signals in the model

sig

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

| ATTRIBUTES |
| --- |
| arg : String Private  The payload of the signal. In this model the payload is only one argument.  [ Is static True. Containment is Not Specified. ] |

#### *TICK*

Trigger in package 'Signals'

Signal used to encode the completion of a clock cycle

TICK

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/28/2020. Last modified 11/10/2020

### CSL

Class in package 'Package1'

The Communication Supervision Layer class.

CSL

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/28/2020. Last modified 11/10/2020

| ELEMENTS OWNED BY CSL |
| --- |
| CSL : StateMachine |

| ATTRIBUTES |
| --- |
| connect\_timer : int Private  Accumulating time since last SAI\_CONNECT\_REQUEST.  [ Is static True. Containment is Not Specified. ] |
| initiator : boolean Public  The attribute initiator is used to distinguish the initiator SAI from the called SAI  [ Is static True. Containment is Not Specified. ] |
| max\_connect\_timer : int Public  This attribute represents the maximum amount of time that CSL waits after the last connection request issued to the SAI, before issuing a new one.  [ Is static True. Containment is Not Specified. ] |
| max\_receive\_timer : int Public  The maximum amount of time the CSL waits for a message from SAI before closing the connection.  [ Is static True. Containment is Not Specified. ] |
| max\_send\_timer : int Public  The maximum amount of time in which the CSL sends a message to underlying layer SAI. When this threshold is reached, the CSL will issue a LifeSign message.  [ Is static True. Containment is Not Specified. ] |
| receive\_timer : int Private = 0  Accumulating time since last message received from SAI.  [ Is static True. Containment is Not Specified. ] |
| send\_timer : int Private = 0  Accumulating time since last message.  [ Is static True. Containment is Not Specified. ] |

| ASSOCIATIONS | |
| --- | --- |
| Association (direction: Source -> Destination) CSL2RBC\_USER  Each CSL has a reference to its own RBC\_USER for sending signals | |
| Source: Public (Class) CSL | Target: Public RBC\_USER (Class) RBC\_USER |
| Association (direction: Source -> Destination) CSL2SAI  Each CSL has a reference to its own SAI for sending signals | |
| Source: Public (Class) CSL | Target: Public SAI (Class) SAI |

#### *CSL*

StateMachine owned by 'CSL', in package 'Package1'

The CSL state machine

CSL

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

| ELEMENTS OWNED BY CSL |
| --- |
| COMMS : State |
| NOCOMMS : State |
| Initial : Initial State |

##### CSL diagram

StateMachine diagram in package 'Package1'

The CSL state machine

CSL

Version 1.0

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020



1. CSL

##### COMMS

State owned by 'CSL', in package 'Package1'

The CSL state machine COMMS state, where the connection is established

COMMS

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

| OUTGOING BEHAVIORAL RELATIONSHIPS |
| --- |
| Transition from COMMS to NOCOMMS  Effect: %SEND\_EVENT("RBC\_USER\_DISCONNECT\_INDICATION",CONTEXT\_REF(RBC\_USER))%;  this.receive\_timer=0;  this.send\_timer=0;  Triggers:  SAI\_DISCONNECT\_INDICATION Signal  Mapping to UMC rules:  R16\_ICSL\_IRBC\_rbcuserdisconnectindication  R16\_CCSL\_IRBC\_rbcuserdisconnectindication  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from COMMS to COMMS  Effect: this.send\_timer=0;  %SEND\_EVENT("SAI\_DATA\_REQUEST.sig("+signal.parameterValues.get("arg")+")",CONTEXT\_REF(SAI))%;  Triggers:  RBC\_USER\_DATA\_REQUEST Signal sig  Mapping to UMC rules:  R10\_ICSL\_ISAI\_saidatarequest  R10\_CCSL\_CSAI\_saidatarequest  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from COMMS to COMMS  Effect: this.receive\_timer = 0;  if (signal.parameterValues.get("arg") !="LifeSign") {  %SEND\_EVENT("RBC\_USER\_DATA\_INDICATION.sig("+signal.parameterValues.get("arg")+")",CONTEXT\_REF(RBC\_USER))%;  }  Triggers:  SAI\_DATA\_INDICATION Signal sig  Mapping to UMC rules:  R13\_ICSL\_IRBC\_rbcuserdataindication  R14\_ICSL\_handle\_lifesign  R13\_CCSL\_CRBC\_rbcuserdataindication  R14\_CCSL\_handle\_lifesign  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from COMMS to COMMS  Guard: this.receive\_timer<this.max\_receive\_timer && this.send\_timer==this.max\_send\_timer  Effect: this.send\_timer = 0;  this.receive\_timer = this.receive\_timer+1;  %SEND\_EVENT("SAI\_DATA\_REQUEST.sig(LifeSign)",CONTEXT\_REF(SAI))%;  Triggers:  TICK Signal  Mapping to UMC rules:  R12\_ICSL\_Timer\_okicsl\_ISAI\_saidatarequest  R12\_CCSL\_Timer\_okccsl\_CSAI\_saidatarequest  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from COMMS to NOCOMMS  Guard: this.receive\_timer==this.max\_receive\_timer  Effect: %SEND\_EVENT("RBC\_USER\_DISCONNECT\_INDICATION",CONTEXT\_REF(RBC\_USER))%;  %SEND\_EVENT("SAI\_DISCONNECT\_REQUEST",CONTEXT\_REF(SAI))%;  this.receive\_timer=0;  this.send\_timer=0;  Triggers:  TICK Signal  Mapping to UMC rules:  R17\_ICSL\_Timer\_okicsl\_IRBC\_rbcuserdisconnectindication\_ISAI\_saidisconnectrequest  R17\_CCSL\_Timer\_okccsl\_CRBC\_rbcuserdisconnectindication\_CSAI\_saidisconnectrequest  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from COMMS to COMMS  Guard: this.initiator==false  Effect: this.receive\_timer=0;  this.send\_timer=0;  %SEND\_EVENT("RBC\_USER\_CONNECT\_INDICATION",CONTEXT\_REF(RBC\_USER))%;  Triggers:  SAI\_CONNECT\_INDICATION Signal  Mapping to UMC rules:  R9\_CCSL\_CRBC\_rbcuserconnectindication  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from COMMS to COMMS  Triggers:  SAI\_ERROR\_REPORT Signal  Mapping to UMC rules:  R15\_ICSL\_IRBC\_rbcusererrorindication  R15\_CCSL\_CRBC\_rbcusererrorindication  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from COMMS to COMMS  Guard: this.receive\_timer < this.max\_receive\_timer && this.send\_timer<this.max\_send\_timer  Effect: this.send\_timer = this.send\_timer+ 1;  this.receive\_timer = this.receive\_timer+1;  Triggers:  TICK Signal  Mapping to UMC rules:  R11\_ICSL\_Timer\_okicsl  R11\_CCSL\_Timer\_okccsl  Mapping to Requirements:  (see mapping from UMC rules to requirements) |

| INCOMING BEHAVIORAL RELATIONSHIPS |
| --- |
| Transition from COMMS to COMMS  Effect: this.send\_timer=0;  %SEND\_EVENT("SAI\_DATA\_REQUEST.sig("+signal.parameterValues.get("arg")+")",CONTEXT\_REF(SAI))%;  Triggers:  RBC\_USER\_DATA\_REQUEST Signal sig  Mapping to UMC rules:  R10\_ICSL\_ISAI\_saidatarequest  R10\_CCSL\_CSAI\_saidatarequest  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from COMMS to COMMS  Effect: this.receive\_timer = 0;  if (signal.parameterValues.get("arg") !="LifeSign") {  %SEND\_EVENT("RBC\_USER\_DATA\_INDICATION.sig("+signal.parameterValues.get("arg")+")",CONTEXT\_REF(RBC\_USER))%;  }  Triggers:  SAI\_DATA\_INDICATION Signal sig  Mapping to UMC rules:  R13\_ICSL\_IRBC\_rbcuserdataindication  R14\_ICSL\_handle\_lifesign  R13\_CCSL\_CRBC\_rbcuserdataindication  R14\_CCSL\_handle\_lifesign  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from COMMS to COMMS  Guard: this.receive\_timer<this.max\_receive\_timer && this.send\_timer==this.max\_send\_timer  Effect: this.send\_timer = 0;  this.receive\_timer = this.receive\_timer+1;  %SEND\_EVENT("SAI\_DATA\_REQUEST.sig(LifeSign)",CONTEXT\_REF(SAI))%;  Triggers:  TICK Signal  Mapping to UMC rules:  R12\_ICSL\_Timer\_okicsl\_ISAI\_saidatarequest  R12\_CCSL\_Timer\_okccsl\_CSAI\_saidatarequest  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from COMMS to COMMS  Guard: this.initiator==false  Effect: this.receive\_timer=0;  this.send\_timer=0;  %SEND\_EVENT("RBC\_USER\_CONNECT\_INDICATION",CONTEXT\_REF(RBC\_USER))%;  Triggers:  SAI\_CONNECT\_INDICATION Signal  Mapping to UMC rules:  R9\_CCSL\_CRBC\_rbcuserconnectindication  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from NOCOMMS to COMMS  Guard: this.initiator==true  Effect: this.connect\_timer=this.max\_connect\_timer;  %SEND\_EVENT("RBC\_USER\_CONNECT\_INDICATION",CONTEXT\_REF(RBC\_USER))%;  Triggers:  SAI\_CONNECT\_CONFIRM Signal  Mapping to UMC rules:  R8\_ICSL\_IRBC\_rbcuserconnectindication  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from NOCOMMS to COMMS  Guard: this.initiator==false  Effect: %SEND\_EVENT("RBC\_USER\_CONNECT\_INDICATION",CONTEXT\_REF(RBC\_USER))%;  Triggers:  SAI\_CONNECT\_INDICATION Signal  Mapping to UMC rules:  R8\_CCSL\_CRBC\_rbcuserconnectindication  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from COMMS to COMMS  Triggers:  SAI\_ERROR\_REPORT Signal  Mapping to UMC rules:  R15\_ICSL\_IRBC\_rbcusererrorindication  R15\_CCSL\_CRBC\_rbcusererrorindication  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from COMMS to COMMS  Guard: this.receive\_timer < this.max\_receive\_timer && this.send\_timer<this.max\_send\_timer  Effect: this.send\_timer = this.send\_timer+ 1;  this.receive\_timer = this.receive\_timer+1;  Triggers:  TICK Signal  Mapping to UMC rules:  R11\_ICSL\_Timer\_okicsl  R11\_CCSL\_Timer\_okccsl  Mapping to Requirements:  (see mapping from UMC rules to requirements) |

##### NOCOMMS

State owned by 'CSL', in package 'Package1'

The CSL state machine NOCOMMS state, where the connection is not established

NOCOMMS

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/29/2020. Last modified 11/10/2020

| OUTGOING BEHAVIORAL RELATIONSHIPS |
| --- |
| Transition from NOCOMMS to COMMS  Guard: this.initiator==true  Effect: this.connect\_timer=this.max\_connect\_timer;  %SEND\_EVENT("RBC\_USER\_CONNECT\_INDICATION",CONTEXT\_REF(RBC\_USER))%;  Triggers:  SAI\_CONNECT\_CONFIRM Signal  Mapping to UMC rules:  R8\_ICSL\_IRBC\_rbcuserconnectindication  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from NOCOMMS to COMMS  Guard: this.initiator==false  Effect: %SEND\_EVENT("RBC\_USER\_CONNECT\_INDICATION",CONTEXT\_REF(RBC\_USER))%;  Triggers:  SAI\_CONNECT\_INDICATION Signal  Mapping to UMC rules:  R8\_CCSL\_CRBC\_rbcuserconnectindication  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from NOCOMMS to NOCOMMS  Guard: this.initiator==false  Triggers:  TICK Signal  Mapping to UMC rules:  R7\_CCSL\_Timer\_okccsl  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from NOCOMMS to NOCOMMS  Guard: this.initiator==true && this.connect\_timer<this.max\_connect\_timer  Effect: this.connect\_timer = this.connect\_timer+1;  Triggers:  TICK Signal  Mapping to UMC rules:  R7\_ICSL\_Timer\_okicsl  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from NOCOMMS to NOCOMMS  Guard: this.initiator==true && this.connect\_timer==this.max\_connect\_timer  Effect: this.connect\_timer = 0;  %SEND\_EVENT("SAI\_CONNECT\_REQUEST",CONTEXT\_REF(SAI))%;  Triggers:  TICK Signal  Mapping to UMC rules:  R6\_ICSL\_Timer\_okicsl\_ISAI\_connectrequest  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from NOCOMMS to NOCOMMS  Triggers:  RBC\_USER\_DATA\_REQUEST Signal sig  SAI\_DISCONNECT\_INDICATION Signal  SAI\_ERROR\_REPORT Signal  SAI\_DATA\_INDICATION Signal sig  Mapping to UMC rules:  R1\_ICSL\_discard\_userdata,  R2\_ICSL\_discard\_dsconnectindication,  R3\_ICSL\_discard\_errorreport,  R4\_ICSL\_discard\_dataindication,  R1\_CCSL\_discard\_userdata,  R2\_CCSL\_discard\_dsconnectindication,  R3\_CCSL\_discard\_errorreport,  R4\_CCSL\_discard\_dataindication  Mapping to Requirements:  (see mapping from UMC rules to requirements) |

| INCOMING BEHAVIORAL RELATIONSHIPS |
| --- |
| Transition from COMMS to NOCOMMS  Effect: %SEND\_EVENT("RBC\_USER\_DISCONNECT\_INDICATION",CONTEXT\_REF(RBC\_USER))%;  this.receive\_timer=0;  this.send\_timer=0;  Triggers:  SAI\_DISCONNECT\_INDICATION Signal  Mapping to UMC rules:  R16\_ICSL\_IRBC\_rbcuserdisconnectindication  R16\_CCSL\_IRBC\_rbcuserdisconnectindication  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from COMMS to NOCOMMS  Guard: this.receive\_timer==this.max\_receive\_timer  Effect: %SEND\_EVENT("RBC\_USER\_DISCONNECT\_INDICATION",CONTEXT\_REF(RBC\_USER))%;  %SEND\_EVENT("SAI\_DISCONNECT\_REQUEST",CONTEXT\_REF(SAI))%;  this.receive\_timer=0;  this.send\_timer=0;  Triggers:  TICK Signal  Mapping to UMC rules:  R17\_ICSL\_Timer\_okicsl\_IRBC\_rbcuserdisconnectindication\_ISAI\_saidisconnectrequest  R17\_CCSL\_Timer\_okccsl\_CRBC\_rbcuserdisconnectindication\_CSAI\_saidisconnectrequest  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from Initial to NOCOMMS  Effect: if (this.initiator) this.connect\_timer=this.max\_connect\_timer;  Initially the connect\_timer is reset to max\_connect\_timer for the initiator CSL, such that the request for connection is immediate |
| Transition from NOCOMMS to NOCOMMS  Guard: this.initiator==false  Triggers:  TICK Signal  Mapping to UMC rules:  R7\_CCSL\_Timer\_okccsl  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from NOCOMMS to NOCOMMS  Guard: this.initiator==true && this.connect\_timer<this.max\_connect\_timer  Effect: this.connect\_timer = this.connect\_timer+1;  Triggers:  TICK Signal  Mapping to UMC rules:  R7\_ICSL\_Timer\_okicsl  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from NOCOMMS to NOCOMMS  Guard: this.initiator==true && this.connect\_timer==this.max\_connect\_timer  Effect: this.connect\_timer = 0;  %SEND\_EVENT("SAI\_CONNECT\_REQUEST",CONTEXT\_REF(SAI))%;  Triggers:  TICK Signal  Mapping to UMC rules:  R6\_ICSL\_Timer\_okicsl\_ISAI\_connectrequest  Mapping to Requirements:  (see mapping from UMC rules to requirements) |
| Transition from NOCOMMS to NOCOMMS  Triggers:  RBC\_USER\_DATA\_REQUEST Signal sig  SAI\_DISCONNECT\_INDICATION Signal  SAI\_ERROR\_REPORT Signal  SAI\_DATA\_INDICATION Signal sig  Mapping to UMC rules:  R1\_ICSL\_discard\_userdata,  R2\_ICSL\_discard\_dsconnectindication,  R3\_ICSL\_discard\_errorreport,  R4\_ICSL\_discard\_dataindication,  R1\_CCSL\_discard\_userdata,  R2\_CCSL\_discard\_dsconnectindication,  R3\_CCSL\_discard\_errorreport,  R4\_CCSL\_discard\_dataindication  Mapping to Requirements:  (see mapping from UMC rules to requirements) |

##### Initial

Initial State owned by 'CSL', in package 'Package1'

The CSL state machine initial state

| OUTGOING BEHAVIORAL RELATIONSHIPS |
| --- |
| Transition from Initial to NOCOMMS  Effect: if (this.initiator) this.connect\_timer=this.max\_connect\_timer;  Initially the connect\_timer is reset to max\_connect\_timer for the initiator CSL, such that the request for connection is immediate |

### RBC\_USER

Class in package 'Package1'

The RBC\_USER class is only a stub.

RBC\_USER

Version 1.0 Phase 1.0 Proposed

DavideDavide Basile (ISTI CNR Italy) created on 10/1/2020. Last modified 11/10/2020

| ELEMENTS OWNED BY RBC\_USER |
| --- |
| RBC\_USER : StateMachine |

| ASSOCIATIONS | |
| --- | --- |
| Association (direction: Source -> Destination) CSL2RBC\_USER  Each CSL has a reference to its own RBC\_USER for sending signals | |
| Source: Public (Class) CSL | Target: Public RBC\_USER (Class) RBC\_USER |

#### *RBC\_USER*

StateMachine owned by 'RBC\_USER', in package 'Package1'

The RBC\_USER state machine

RBC\_USER

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 10/1/2020. Last modified 11/10/2020

| ELEMENTS OWNED BY RBC\_USER |
| --- |
| Stub : State |
| Initial : Initial State |

##### RBC\_USER diagram

StateMachine diagram in package 'Package1'

The RBC\_USER state machine

RBC\_USER

Version 1.0

Davide Basile (ISTI CNR Italy) created on 10/1/2020. Last modified 11/10/2020



1. RBC\_USER

##### Stub

State owned by 'RBC\_USER', in package 'Package1'

The RBC\_USER state machine stub state

Stub

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 10/1/2020. Last modified 11/10/2020

| OUTGOING BEHAVIORAL RELATIONSHIPS |
| --- |
| Transition from Stub to Stub  Triggers:  RBC\_USER\_CONNECT\_INDICATION Signal  RBC\_USER\_DATA\_INDICATION Signal sig  RBC\_USER\_DISCONNECT\_INDICATION Signal |

| INCOMING BEHAVIORAL RELATIONSHIPS |
| --- |
| Transition from Stub to Stub  Triggers:  RBC\_USER\_CONNECT\_INDICATION Signal  RBC\_USER\_DATA\_INDICATION Signal sig  RBC\_USER\_DISCONNECT\_INDICATION Signal |
| Transition from Initial to Stub |

##### Initial

Initial State owned by 'RBC\_USER', in package 'Package1'

The RBC\_USER state machine initial state

| OUTGOING BEHAVIORAL RELATIONSHIPS |
| --- |
| Transition from Initial to Stub |

### SAI

Class in package 'Package1'

The Safety Application Intermediate sub-layer class. This class is now only a stub.

SAI

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/28/2020. Last modified 11/10/2020

| ELEMENTS OWNED BY SAI |
| --- |
| SAI : StateMachine |

| ATTRIBUTES |
| --- |
| initiator : boolean Public  The attribute initiator is used to distinguish the initiator SAI from the called SAI  [ Is static True. Containment is Not Specified. ] |

| ASSOCIATIONS | |
| --- | --- |
| Association (direction: Source -> Destination) CSL2SAI  Each CSL has a reference to its own SAI for sending signals | |
| Source: Public (Class) CSL | Target: Public SAI (Class) SAI |

#### *SAI*

StateMachine owned by 'SAI', in package 'Package1'

The SAI state machine

SAI

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/30/2020. Last modified 11/10/2020

| ELEMENTS OWNED BY SAI |
| --- |
| Stub : State |
| Initial : Initial State |

##### SAI diagram

StateMachine diagram in package 'Package1'

The SAI state machine

SAI

Version 1.0

Davide Basile (ISTI CNR Italy) created on 9/30/2020. Last modified 11/10/2020



1. SAI

##### Stub

State owned by 'SAI', in package 'Package1'

The stub state of the SAI state machine

Stub

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/30/2020. Last modified 11/10/2020

| OUTGOING BEHAVIORAL RELATIONSHIPS |
| --- |
| Transition from Stub to Stub  Guard: this.initiator==true  Triggers:  SAI\_CONNECT\_REQUEST Signal |
| Transition from Stub to Stub  Triggers:  SAI\_DATA\_REQUEST Signal sig  SAI\_DISCONNECT\_REQUEST Signal |

| INCOMING BEHAVIORAL RELATIONSHIPS |
| --- |
| Transition from Initial to Stub |
| Transition from Stub to Stub  Guard: this.initiator==true  Triggers:  SAI\_CONNECT\_REQUEST Signal |
| Transition from Stub to Stub  Triggers:  SAI\_DATA\_REQUEST Signal sig  SAI\_DISCONNECT\_REQUEST Signal |

##### Initial

Initial State owned by 'SAI', in package 'Package1'

The initial state of the SAI state machine

| OUTGOING BEHAVIORAL RELATIONSHIPS |
| --- |
| Transition from Initial to Stub |

### RBC2RBC SI

Artifact «executable statemachine» in package 'Package1'

This executable state machine represents a composition of an initiator RBC with called RBC. Only the CSL classes are developed, whilst each RBC\_USER and SAI acts as environment to own CSL.

RBC2RBC SI

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/28/2020. Last modified 11/10/2020

| STRUCTURAL PART OF RBC2RBC SI |
| --- |
| C\_CSL : Property  The Called CSL |
| C\_SAI : Property  The called SAI |
| I\_SAI : Property  the initiator SAI |
| C\_RBC\_USER : Property  The called RBC\_USER |
| I\_CSL : Property  the initiator CSL |
| I\_RBC\_USER : Property  The initiator RBC\_USER |

#### *C\_CSL*

Property owned by 'RBC2RBC SI', in package 'Package1'

The Called CSL

C\_CSL

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 10/14/2020. Last modified 10/29/2020

| OUTGOING STRUCTURAL RELATIONSHIPS |
| --- |
| Connector from C\_CSL to C\_RBC\_USER  [ Direction is 'Unspecified'. ] |
| Connector from C\_CSL to C\_SAI  [ Direction is 'Unspecified'. ] |

| RUN STATES | OPERATOR | VALUE | NOTES |
| --- | --- | --- | --- |
| initiator | = | false | The called CSL |
| max\_send\_timer | = | 1 | these values are not significant, they are just a possible set-up of parameters |
| max\_receive\_timer | = | 2 | these values are not significant, they are just a possible set-up of parameters |

#### *C\_SAI*

Property owned by 'RBC2RBC SI', in package 'Package1'

The called SAI

C\_SAI

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 10/16/2020. Last modified 10/29/2020

| INCOMING STRUCTURAL RELATIONSHIPS |
| --- |
| Connector from C\_CSL to C\_SAI  [ Direction is 'Unspecified'. ] |

| RUN STATES | OPERATOR | VALUE | NOTES |
| --- | --- | --- | --- |
| initiator | = | false | The called SAI |

#### *I\_SAI*

Property owned by 'RBC2RBC SI', in package 'Package1'

the initiator SAI

I\_SAI

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 10/16/2020. Last modified 10/29/2020

| INCOMING STRUCTURAL RELATIONSHIPS |
| --- |
| Connector from I\_CSL to I\_SAI  [ Direction is 'Unspecified'. ] |

| RUN STATES | OPERATOR | VALUE | NOTES |
| --- | --- | --- | --- |
| initiator | = | true | The initiator SAI |

#### *C\_RBC\_USER*

Property owned by 'RBC2RBC SI', in package 'Package1'

The called RBC\_USER

C\_RBC\_USER

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 10/1/2020. Last modified 10/29/2020

| INCOMING STRUCTURAL RELATIONSHIPS |
| --- |
| Connector from C\_CSL to C\_RBC\_USER  [ Direction is 'Unspecified'. ] |

#### *I\_CSL*

Property owned by 'RBC2RBC SI', in package 'Package1'

the initiator CSL

I\_CSL

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 9/28/2020. Last modified 10/29/2020

| OUTGOING STRUCTURAL RELATIONSHIPS |
| --- |
| Connector from I\_CSL to I\_RBC\_USER  [ Direction is 'Unspecified'. ] |
| Connector from I\_CSL to I\_SAI  [ Direction is 'Unspecified'. ] |

| RUN STATES | OPERATOR | VALUE | NOTES |
| --- | --- | --- | --- |
| initiator | = | true | The initiator CSL |
| max\_send\_timer | = | 1 | these values are not significant, they are just a possible set-up of parameters |
| max\_connect\_timer | = | 3 | these values are not significant, they are just a possible set-up of parameters |
| max\_receive\_timer | = | 2 | these values are not significant, they are just a possible set-up of parameters |

#### *I\_RBC\_USER*

Property owned by 'RBC2RBC SI', in package 'Package1'

The initiator RBC\_USER

I\_RBC\_USER

Version 1.0 Phase 1.0 Proposed

Davide Basile (ISTI CNR Italy) created on 10/1/2020. Last modified 10/29/2020

| INCOMING STRUCTURAL RELATIONSHIPS |
| --- |
| Connector from I\_CSL to I\_RBC\_USER  [ Direction is 'Unspecified'. ] |