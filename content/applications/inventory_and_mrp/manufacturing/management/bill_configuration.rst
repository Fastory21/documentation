=========================
Create Bills of Materials
=========================

A *Bill of Materials* is a document that defines the quantity of each component required to make
or deliver a finished product. It can also include various operations and individual step
guidelines needed to complete a production process. 

In Odoo Manufacturing, multiple BoMs can be linked to each product, so that even product variants
can have their own tailored BoMs.

Correctly setting up BoMs will help you optimize your manufacturing process and save time as a
result. 

Setting up a BoM
================
The simplest BoM setup is one without operations or instructions. In this case, you will manage
your production solely using Manufacturing Orders.

To create a BoM from the Manufacturing module, go to :menuselection:`Products --> Bills of
Materials`. If you click **Create**, the first thing you'll have to do is to specify the final
product. For an existing product, simply select it from the list, or create a new one on the spot.
Note that if you go through the product form to create your BoM, the product will already be set
for you.

For a standard Bill of Material, keep *BoM Type* set to *Manufacture this Product*, which is the
default setting. Then, specify the various components that make up the production of your final
product and their respective quantities. You can create components on the fly through the BoM, or
create components beforehand by going to the :menuselection:`Top Menu --> Products --> Create`, and
add them to the BoM later on. 


.. image:: bill_configuration/bom_1.png
    :align: center
    :alt: Set up a Bill of Materials.

.. warning::
   The destination location should **not** be a scrap location. A scrap location is where you put
   products that you don't need.

Using BoMs with Product Variants
---------------------------------------

As suggested above, you can assign BoMs to specific *Product Variants*. There are two ways to set
up BoMs for product variants, after the attributes have been configured on the product form.

You can create one BoM per variant by specifying the *Product Variant* in the dedicated field below
the product name. Alternatively, you can use one master BoM that contains all of the components, and
specify which variant each component applies to using the *Apply on Variants* column, as shown
below. 

.. image:: bill_configuration/bom_2.png
    :align: center
    :alt: Product Variants in the Bill of Materials. 


Adding Operations
=================

You can also add *Operations* to your BoM if you want workers to follow instructions or register
time spent. To use this feature, enable the *Work Orders* feature in the *Manufacturing* app
settings, as shown below.

.. image:: bill_configuration/bom_3.png
    :align: center
    :alt: Work Orders Setting. 

.. note::
         Each operation is unique, as it is always exclusively linked to one BoM. 
         Operations can be re-used when configuring a new BoM, with the *Copy Existing 
         Operations* feature.

.. image:: bill_configuration/bom_4.png
    :align: center
    :alt: *Copy Existing Operations* feature. 

Like components, operations can also be variant-specific, as shown below.

.. image:: bill_configuration/bom_5.png
    :align: center
    :alt: Variant-specific operations. 



Adding By-Products
==================

A *By-Product* is a product that is produced in addition to the main product of a BoM. Unlike the
primary product, there can be more than one by-product on a BoM. 

To add by-products to a BoM, you will first need to enable the *By-Products* feature from the
*Manufacturing* app settings.

.. image:: bill_configuration/bom_6.png
    :align: center
    :alt: By-Products setting. 

Once the feature is enabled, you can add by-products to your BoMs. If you have operations, you'll
need to specify exactly which operation the by-product will be produced from. 
