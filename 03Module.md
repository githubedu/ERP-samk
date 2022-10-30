# 03 Modules & more

An ERP system from a single vendor can be the only system in use by a company or a part, a component, of the entire ERP solution of a company that use several vendors. Each ERP system is conceived as a group of modules, that interact with information flow between the modules ou exporting and importing data between different solutions.

## Details
In order to evaluate one module, for this exercise the **Manufactuing** module, the approach is to configure the module and identify the interaction with others modules as well the difficulties or pecularities during the task execution.

## Module Configuration
Setting up a **Manufacturing** module require a keen eye on details, but sometimes not so detailed in order to avoid complications.    
The sequence to setup the module on my testing [axelor ERP](https://erp.33co.de) instance is the following:
1. Setup Country, City, Company information
2. Create workshop, in [Kartano Tech Oy](https://code.33co.de/ehofmann/ERP-samk/src/branch/master/02Process.md) case is the PCB Workshop, Metal Workshop and Assembly Workshop
3. Add cancel reasons, during setup I do not know what is the need of such *Cancel Reasons*, I considered as issues in production that could cancel an order
4. Product approvals, in this item I created inspection step that will approve the product, to be validated at the end.
5. Machine types. In this case I added twelve type of machines that are necessary to create PCB *"Printed Circuit Boards"*
6. Machines. Here I added the machine that is producing according each manufacturing step. Each machine belong to a *Machine Type* group.
7. Work Centers. Here machines are grouped in order to produce the product, also capacity and costing settings are defined. I will need to return to this settings after adding products to the system, as this information is necessary to define the process cost.

## Creating orders
Still some configurations are empty or not clear what are the requirements, by checking the [documentation](https://docs.axelor.com/abs/5.0/functional/manufacturing.html#introduction) I decide to follow the manual flow and configure the product.

## Integration
Several occasions during the configuration of the **Manufacturing** module the system show messages requesting to setup another module in order to continue the configuration or even to use the manufacturing module to create a work order. 
![Require product info](img/03-productempty.png)
The example below ilustrate the message when I was trying to create a work order, then the system require a product to be created and during the product creation that can be on the **Manufacturing** module or in the **Stock Management** module, the system show a message requesting to configure the *Stock Management* module. 
![Require product info](img/03-errorMessage.png)

