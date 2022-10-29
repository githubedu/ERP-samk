# 03 Modules & more

An ERP system from a single vendor can be the only system in use by a company or a part, a component, of the entire ERP solution of a company that use several vendors. Each ERP system is conceived as a group of modules, that interact with information flow between the modules ou exporting and importing data between different solutions.

## Setting up
It's quite common that I try to setup something, but is needed another setting from other part of the system.

### Sequence
Setting up a **Manufacturing** module require require a keen eye on details, but sometimes not so detailed in order to avoid complications.    
The sequence to setup the module on my testing [axelor ERP](https://erp.33co.de) instance is the following:
1. Setup Country, City, Company information
2. - Create workshop, in [Kartano Tech Oy](https://code.33co.de/ehofmann/ERP-samk/src/branch/master/02Process.md) case is the PCB Workshop, Metal Workshop and Assembly Workshop
3. Add cancel reasons, during setup I do not know what is the need of such *Cancel Reasons*, I considered as issues in production that could cancel an order
4. Product approvals, in this item I created inspection step that will approve the product, to be validated at the end.
5. Machine types. In this case I added twelve type of machines that are necessary to create PCB *"Printed Circuit Boards"*
6. Machines. Here I added the machine that is producing according each manufacturing step. Each machine belong to a *Machine Type* group.
7. Work Centers. Here machines are grouped in order to produce the product, also capacity and costing settings are defined. I will need to return to this settings after adding products to the system, as this information is necessary to define the process cost.


