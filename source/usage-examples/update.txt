=================
Update a Document
=================

.. default-domain:: mongodb


.. contents:: On this page
:local:
:backlinks: none
:depth: 2
:class: singlecol

Overview
--------

MongoDB offers methods to update an existing document for various use cases. Two of these are `collection.updateOne` and collection.findOneAndUpdate`. 

The ``movies`` collection contains documents similar to the following:

.. code-block:: 

{ _id: 6305, title: "Blacksmith Scene", plot: "Blacksmith Scene is an 1893 American short black-and-white silent film." },
{ _id: 6305, title: "The Great Train Robbery", plot: "A group of bandits stage a brazen train hold-up." },
{ _id: 6305, title: "The Land Beyond the Sunset", plot: "A young boy, opressed by his mother, goes on an outing in the country." },
{ _id: 6305, title: "A Corner in Wheat", plot: "A greedy tycoon decides, on a whim, to corner the world market in wheat." },
{ _id: 6305, title: "Gertie the Dinosaur", plot: "The cartoonist, Winsor McCay, brings the Dinosaurus back to life." }

Update a document and return it's results: 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~g
The `collection.findOneAndUpdate`  function is used to update an
existing document and return the original document in one single `atomic`
operation. If returnNewDocument was true, the operation would return the updated document instead.



Update a document:
~~~~~~~~~~~~~~~~~~
The `collection.updateOne` function is used to update an existing
document. Although you can perform a `find` operation after an update
since they are two separate operations, the document may be altered or
be deleted by another client by the time the `find` operation is
executed.