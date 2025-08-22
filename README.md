## 5G CORE ARCHITECTURE 

<img src = "5GArchitecture.png" alt = " 5GArchitecture">

### UE → RAN → 5GC → DN Path

A 5G User Equipment (UE) (smartphone, IoT device, or CPE) first connects to the 5G New Radio (gNB).

The gNB relays signaling and user traffic towards the 5G Core (5GC), which acts as the brain of the network.

From there, traffic is routed towards Data Networks (DN), which could be the public Internet, enterprise networks, or edge-cloud services.

### Access and Mobility Management Function (AMF)

Acts as the control-plane anchor for the UE.

Handles mobility management, registration, reachability, paging, and serves as the first point of authentication signaling.

Think of it as the "front desk" of the 5G Core that manages signaling but not user data.

### Session Management Function (SMF)

Chosen by the AMF based on the UE’s service request.

Responsible for creating and maintaining PDU Sessions (data sessions).

Controls the User Plane Function (UPF) via rules: IP allocation, QoS enforcement, and traffic steering.

### User Plane Function (UPF)

The data traffic engine of 5G.

Forwards IP packets between the UE and external networks.

Supports advanced features like Uplink Classifier (UL-CL) and branching to local breakout (e.g., MEC/edge computing for ultra-low latency).

### Authentication Server Function (AUSF)

Validates UE credentials during initial attachment using 5G-AKA or EAP-AKA’ protocols.

Works with Unified Data Management (UDM) to fetch subscription profiles.

### Unified Data Management (UDM) & Unified Data Repository (UDR)

Stores subscriber data, profiles, and authentication vectors.

Provides subscription details like service entitlements, data plans, and roaming policies.

### Policy Control Function (PCF) & Application Function (AF)

PCF: Provides QoS and policy decisions (bandwidth allocation, slicing rules, charging control).

AF: Communicates application-level requirements (e.g., video streaming platform requests low latency), which are then enforced by PCF and SMF.


## Radio Protocol Architecture

<img src = "RADIO PROTOCOL ARCHITECTURE.png" alt = "Radio Protocol Architecture">


Both User Plane and Control Plane is made up of a common
 structure:
 • PHY
 • MAC
 • RLC
 • PDCP
 • User Plane, a layer called SDAP is sitting at the top of the radio stack.
 • Control Plane, the two layers RRC and NAS are sitting at the top of
 the stack.
 • NAS layer gets connected to AMF (Access and Mobility Management
 Function)
