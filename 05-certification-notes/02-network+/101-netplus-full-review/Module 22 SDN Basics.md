## Module 22 – SDN Basics

### 🧱 What is SDN?
- **Software-Defined Networking** = Controlling network devices through **software** instead of logging into each one manually.
- Separates **control plane** (decision-making) from **data plane** (actual packet forwarding).
- Managed centrally, usually by an SDN controller.

---

## SDN Architecture Layers

1. **Application Layer**
   - Apps that request network services (e.g., security policies, QoS rules).
2. **Control Layer** (Control Plane)
   - Centralized SDN controller.
   - Decides **where traffic should go**.
   - Communicates with devices via **Southbound APIs**.
3. **Infrastructure Layer** (Data Plane)
   - Physical/virtual switches & routers.
   - Forwards traffic based on instructions from the controller.

---

## Key Terms
- **Southbound API** – Connects SDN controller to network devices.
  - Common example: **OpenFlow**.
- **Northbound API** – Connects applications to SDN controller.
- **Centralized Management** – All configs, policies, and updates pushed from one place.

---

## Benefits of SDN
- **Automation** – Deploy new configs instantly to all devices.
- **Flexibility** – Quickly adapt network paths & policies.
- **Programmability** – Use code/scripts to manage network behavior.
- **Cost-Effective** – Often runs on commodity hardware.

---

## SDN in the Real World
- **Cloud Data Centers** – Dynamically allocate network resources.
- **WAN Optimization** – SD-WAN is a popular SDN use case.
- **Security** – Centralized ACLs & segmentation policies.

---

## Exam Pointers
✅ Control plane = decision-making; data plane = packet forwarding.  
✅ OpenFlow = common SDN protocol.  
✅ Northbound = apps → controller; Southbound = controller → devices.  
✅ Centralized control increases agility but can be a single point of failure if not redundant.  
