# 02 Process

## Company structure
![Kartano Tech Oy Business process](kartano/BusinessProcess.png)
Kartano Tech Oy is organized in seven departments and is arranged in a workflow allowing the information from customer reach the first departments in charge of initialize the manufacturing process and goes until the product is delivered to the customer. It's a push flow, this means that Sales push Manufacturing to produce, that push Logisitics to pack and ship, then push Customer support to install and support customer.

### Sales department
All the Customer Relationship Management, is performed by the Sales Department. This includes: Marketing, Market research, Sales forecast and finally the trade transaction itself. Sales provide a forecast to purchase department in order to anticipate quotations or even a risk order, to purchase raw material before validating a sales order. When a purchase order is received, a **Work Order** is created and assigned to Manufacturing.

### Purchase department
Control the raw material inventory, relationship with suppliers and place the purchase orders for any goods or services.

### Logistics
Manage the warehouse, receive goods and take care of packaging and shipment of final products to customers.

### Customer support
Take care of the customer experience, by organizing installations, trainings and any other customer need during the product life-cycle.

### Manufacturing
The production process is divided in three main workshops responsible for the **core** manufacturing of the company products. The PCB workshop, produce the *printed circuit board*. The Metal workshop, produce the device case and internal parts. Both departments supply the produced parts back to warehouse on which the parts become a sub-component. The Assembly workshop, work based on work orders, when all materials are available. When the WO is completed, the product is forward to the Logistics department.

### Support function 
Company general management and administrative tasks are performed by support functions that report directly to management, this include Finance, IT, HR and Facilities & Maintenance.

### Research & Development
The most important asset of the company is the intellectual property of the product, that include the hardware and software. As well the capability to develop further the products. The R&D department is responsible for product development. Another duty for R&D is to collaborate with the manufacturing process to assure quality and collect feedback for improvements. Sales and Customer support are also a source of feedback.

## Functional Requirement Specification
The benefits of an ERP system are somehow uncountable. The major distinction is shared information, it will remove the silos on which each department own a piece of information.     

The existing process of collecting information about customer *future plans*, possible leads, opportunities and converting into a sales forecast to allow purchase negotiate in advance or even manufacturing plan resources. It's completely informal and without traceability of updates. When sales department achieve certain confidentiality about a new contract, they send a *Heads up* email, to inform internally. A customer can place a purchase order (PO) at any moment, most of the cases is through an email.    
Sales process the PO adding into excel file to control and follow up invoice process, that is performed by Finance. Also a *work order* (WO) is created, printed and delivered to the Manufacturing department. Which will create the *Bill of Materials* (BOM) and a person will walk to the Warehouse to pickup the material and inform the warehouse team which materials and quantities are being consumed in order to update an standalone warehouse inventory control. Purchase, collect reports from this inventory control and merge with an excel file to trigger purchase when a minimum threshold has been reached.

### Modules
The existing process is completely manual, traceability relies on the email historic data. Relation between manufacturing and warehouse is prone to failure, resulting on incorrect information about stock level, that can cause material shortage, causing production stop and late deliveries.    
The *nice side* of an ERP system is that it will formalize many activities and allow rethink the way the company operates. Starting from a **CRM** module to support Sales in getting sales deals close and most important, provide reliable information to purchase department. The next module that is mandatory is the **Manufacturing** on which all the operation will be controlled. By having a manufacturing module, others modules are also needed to compliment the functionality of the ERP system, as: **Stock** and **Sales**. When a sales order is entered in the system, it will generate the work order, warehouse can already prepare the material and purchase will know that the stock is changing. This is the beauty of and ERP system, in the exact moment a single order has been confirmed, all actors receive the information. Even Customer support can start to plan installation travels.

### The ugly side
It require all the information is correct, everything! Nowadays, when the BOM is missing a component, it's easy to walk back to warehouse and pickup the part. With an ERP, it may be possible, but it will require a lot of rework to make sure everything is matching. Here is the danger side of an ERP implementation, lack of knowledge and expertise can cause that users allow bad information go inside the system. This can cause severe disruption.


[back HOME](https://code.33co.de/ehofmann/ERP-samk)