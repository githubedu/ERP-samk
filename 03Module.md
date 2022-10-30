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
Several occasions during the configuration of the **Manufacturing** module, it become difficult to advance, because it needs information provided by another module. To create a *work order* is necessary to create a product first.

![Require product info](assigments/img/03-productempty.png)

A product can be created in either of these modules **Manufacturing** module or in the **Stock Management** module or even on **Sales** module. On each of these modules there are some additional info related to the product and the module in use. The image below show the message when a product was being created in the **Stock Management** module and the module is not configured.

![Require product info](assigments/img/03-errorMessage.png)

## Selection
<img src="assigments/img/03-ModuleSelection.png" align="left" width="400px"/>
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nam commodo molestie feugiat. Suspendisse hendrerit vehicula quam, eu mollis dolor rhoncus a. Proin eget ex at odio venenatis faucibus sit amet nec mi. Sed vitae lacinia mi. Maecenas tincidunt imperdiet metus a egestas. Ut eget feugiat arcu. Sed laoreet quis mi non fermentum. Integer nisi erat, mattis at justo non, porta pellentesque enim. Aenean gravida mauris id purus finibus vestibulum. Aenean dapibus tortor quam, vitae elementum purus facilisis sit amet.

Donec scelerisque convallis tortor tristique egestas. Phasellus a elit eget ligula tempor aliquam. Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas. Ut nisl nunc, auctor vitae orci nec, maximus elementum dolor. Fusce ultricies nibh mauris, sit amet sollicitudin eros ultrices sit amet. Vivamus lobortis enim mauris, et hendrerit nibh aliquam id. Curabitur ante nunc, auctor at hendrerit quis, luctus sit amet purus. Suspendisse potenti. Duis commodo, nisi nec lacinia iaculis, quam nulla viverra quam, at pretium mi enim vel magna. Nullam vel turpis eget diam pellentesque euismod.

Nulla mollis scelerisque urna a vehicula. Nulla luctus lacus massa, eget convallis sem aliquam et. Class aptent taciti sociosqu ad litora torquent per conubia nostra, per inceptos himenaeos. Praesent finibus sit amet neque vel consectetur. Aliquam erat volutpat. Mauris eu ex id enim venenatis fermentum sit amet id nisl. Etiam tincidunt elit non ante pellentesque eleifend. Integer et ornare risus, quis consequat metus. Fusce justo ex, maximus nec elementum nec, interdum in turpis.

Nulla iaculis, diam vel facilisis lacinia, arcu leo egestas dui, sed molestie dolor elit euismod erat. Sed venenatis suscipit tellus, eu posuere lorem commodo ut. Ut non lacinia augue. Integer at facilisis nisl. Nunc est turpis, aliquam quis maximus eu, finibus eu turpis. Nullam id fringilla nisl. Nullam accumsan vestibulum neque, sit amet auctor odio dictum non. Nam feugiat, tortor eget cursus accumsan, eros nibh porta quam, vitae dignissim lectus leo in est.

In hac habitasse platea dictumst. Proin tristique justo ac urna posuere suscipit. Nunc finibus sodales leo nec ornare. Nam ut sagittis diam. Donec fringilla, odio quis lobortis vulputate, sem nisl vehicula nulla, ultrices gravida nunc enim sed enim. Nunc laoreet vestibulum finibus. Nulla nunc elit, consectetur eu lacus in, condimentum sollicitudin metus. Curabitur laoreet, enim vitae ullamcorper vulputate, turpis enim ultricies libero, ut semper enim elit sit amet neque. Nullam vitae felis vel ipsum volutpat vestibulum.