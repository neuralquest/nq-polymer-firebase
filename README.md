# Neuralquest

Work in progress. Still very much experimental.

Neuralquest is a platform that allows users to create organizations, develop and 
maintain processes that these organizations execute and assign users to roles
so that they can take part in the organization.

Visit [Neuralquest](https://neuralquest-395e9.firebaseapp.com/#.575d4c3f2cf3d6dc3ed83146...575d4c3f2cf3d6dc3ed83148.575d4c3f2cf3d6dc3ed83147) 

## The Model

Neuralquest is built around an extensible class model that contains all the key ingredients 
needed to develop and execute business processes. At the highest level we have:

* **Owners** Owners can be either users or organizations.
* **Resources** Resources can be either balance sheet or off-balance sheet. 
All resources have an owner.
* **Agreements** Agreements represent transactions between two or more owners and involve zero or more Resources.
Once initiated the agreement keeps track of its state, which in turn
determines who gets to use which View, to modify certain aspects of resources.
There are various kinds of agreements: Purchase, Rental, Membership etc.


The model comes with a set of Page and View objects that are allow 
users to browse published information.

* **Pages** Pages describe the structure of the UI in terms of tabs, sub-pages and widgets.
While navigate nested pages, we are at the same time we are navigating the data graph.
* **Widgets** There are various kins of Widgets: Form, Tree, Table, Document, 3D Diagram etc.
 Widgets display information through a View. 
* **Views** Views reference a class. They contain a collection of properties of that class,
that are to be displayed in the widget.
Views have a query that describes which objects should be displayed in the widget
depending on who you are, your relationship to the owner and the state of the object. 

The entire UI is generated dynamically from these objects.
When you develop you're own model you can can either reuse the standard set of Pages/Views or create you're own
through easy to use forms. All changes take place instantaneously.
 

Checkout the [3D Class Model](https://neuralquest-395e9.firebaseapp.com/#.5834c2a4425310133a49f129...56f87bcc5dde184ccfb9fc70.575d4c3f2cf3d6dc3ed8314c.2..575d4c3f2cf3d6dc3ed83159)

## Backend
Neuralquest currently uses the awesome Google Firebase as a backend but we
are very interested in what happening at [EOS.io](https://eos.io) 