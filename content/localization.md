# Indian Localization

Functional Documentation

Dt:

1.1 Introduction

Localization is the process of adapting and customizing a product to meet the needs of a specific market, as identified by its language, culture, expectations, local standards and legal requirements.

**Indian localization** refers to the process of adapting a product or service to suit the cultural, linguistic, legal, and technical needs of the Indian market. Localization involves more than just translation?it also considers local customs, preferences, and user expectations. For companies aiming to enter or expand in India, understanding localization is crucial to ensure that their products resonate with local users and comply with regional requirements.

1.2 Why is Indian Localization Important ?


India is a culturally diverse and linguistically rich country with over 1.4 billion people, speaking more than 22 official languages and hundreds of dialects. This makes localization essential for businesses that want to deliver an effective user experience in India. A one-size-fits-all approach won't work in such a varied market.

1.3 Scope of Indian Localization.

- Tax

- General ledger

- Accounts payable

- Accounts receivable

- Inventory management

- Product information and management

- Organization and management

- Project and service management

- Fixed assets

- Retail

1.4  Indian localization strategy:

To address the tax (direct and indirect), financial accounting, and statutory reporting requirements for India, the strategy that Microsoft adopted involves providing localizations. This strategy consists of the following elements:

- Meet the central-level tax requirements that are described in the Indian Localization Scope section of this article.

- Meet state-specific and region-specific tax requirements if they are generic across all states in India.

- Meet tax requirements for export and import transactions.

- Deliver new regulatory feature requirements through configurations or new development, according to the localization scope and rules that are specified in this article, and according to implementation opportunities that are driven by the Finance roadmap.

- Deliver new regulatory features for all supported versions of Finance.

1.5 Tax rates covered:

- GST:

Outward supplies:

- Business-to-business (B2B) sales

- Business-to-consumer (B2C) sales

- Export sales

- Goods

- Services

- Sales:

- Non-GST items

- Zero-rated goods and services

- Exempted goods and services

- Reverse charge sales.

- Inward supplies:

- Supply from composite vendors

- Supply from unregistered vendors

- Supply from reverse charge vendors

- Supply from registered vendors

- Retail:

- Intrastate and interstate transactions

- Normal sales

- Customer orders

- Return orders

- Price-inclusive GST

- Price-exclusive GST

- Discounts and offers

- Exempted sales

- Replenishment

- Uniform invoice numbers and point of sale (POS) receipt numbers

**2.1 Functional Configuration**

**Configuring Company?s GSTIN in organization.**

Every Legal with accounting organization must have GSTIN no. configured. Under the Organization window child tab  under GSTIN tab, you can configure the company?s GSTIN no.  According to the GSTIN number, pan number and registered state will auto-fetch.

![Image 1](/images/uYl_Image_1.png)

After saving the GSTIN details, go to the information tab and configure the GSTIN number.

![Image 2](/images/qgp_Image_2.png)

**Configuring GSTIN for Business Partner:**

Go to the Business Partner window  under GSTIN child tab add the GSTIN number, GSTIN number will automatically update the pan and registered state field.  \
GSTIN now represents that Business Partner is registered with the government. If BP is having GSTIN, on the header the GST category field has to be selected as **Registered Regular. **Registered BP will fall under the B2B category of GSTR-1 report. \


![Image 3](/images/PnT_Image_3.png)

After saving the data of the GSTIN tab, configure the saved GSTIN in Business Partner- Location/Address.  As shown in the below image.

![Image 4](/images/BW3_Image_4.png)

**GST Tax Category:**

The GST category is based on the product HSN code and the nature of the transaction done. It can be an Inter-state transaction or Intra-state. We will be creating tax categories such as higher tax rate, lower tax rate, exempted tax rate, etc.

Create a tax category as **Low tax rate** category which will be further configured in tax rates. Similarly, other Tax categories can also be created. Considering Low Tax rate as 5%.

![Image 5](/images/FyQ_Image_5.png)


![Image 6](/images/Grc_Image_6.png)

**GST Tax Rates:**

Considering the above tax category will create the Tax Rate for Low Tax Category.

Firstly we will create a Parent Tax rate for Low tax rate. Give name as GST-Low tax rate, Adding the valid from date (date of applying the tax), configuring the Tax category, tick on Summary level (as sab tax rates will be configured under this Parent tax rate), selecting if Tax rate is for both sale and purchase, selecting Country and destination.

![Image 7](/images/6R4_Image_7.png)

Based on this nature of transactions, there are primarily three different types of GST ? State Goods and Services Tax or SGST. Central Goods and Services Tax or CGST. Integrated Goods and Services Tax or IGST. 

Based on these, Sub tax rates will be created for Parent Tax rate created as Low Tax rate.

Name - CGST-LTR, Valid Date from, Tax category, rate will be the 2.5 if the total CGST and SGTS is 5, configuring country and region, in more information in parent tax rate configure the created parent tax rate i.e., GST-Low tax rate and save.

![Image 8](/images/F3W_Image_8.png)

Follow the same for the remaining sub tax rates of low tax rate.

Create the Tax rates similar to the Low tax rate.

![Image 9](/images/C3b_Image_9.png)

**Creating GST Product Code:**

**What is HSN Code?**

Harmonized System of Nomenclature code (HSN Code) is used for classifying goods under GST. The codes have been issued by World's Customs Organization (WCO). They are used for the classification of commodities under various sections, chapters, headings, and sub-headings that belong to alike nature.

Every category of the product has been assigned HSN code, some products have the low tax rate or some have the luxury tax rate or some are exempted. We will move on with creating the product code for a low tax rate.

Go to the GST** Product Code window, ** create a new one, and select the product according to the business, as my organization is one shop destination. I will be creating a product with the name Indian sweets, checking the HSN code of the product and the tax percentage. Considering the low tax rate is 5 %. Tax category to be configured according to the product. Added GST Product code according to the government's criteria. Select HSN Sac type as HSN Code. 

![Image 10](/images/NzF_Image_10.png)

Multiple Product Code can be created as required for the business.

![Image 11](/images/nw0_Image_11.png)

**Configuration in Product window:**

Configure the GST product code which has been created for Indian sweets, and configure the tax category as low tax rate (5%).

![Image 12](/images/ack_Image_12.png)

 **What is** **E-Invoice & E-WayBill	:**

E-Invoice is a system in which B2B invoices are authenticated electronically by GSTN for further use on the common GST portal. Under the electronic invoicing system, an identification number will be issued against every invoice by the Invoice Registration Portal (IRP) to be managed by the GST Network (GSTN).

Under GST, an Electronic Way bill is required for movement of goods. A registered person cannot transport goods in a vehicle whose value exceeds Rs. 50,000 (Single Invoice/bill/delivery challan) without an e-way bill that is generated.

All invoice information is transferred from the government portal to both the GST portal and e-way bill portal in real-time. Therefore, it eliminates the need for manual data entry while filing GSTR-1 return as well as generation of part-A of the e-way bills, as the information is passed directly by the IRP to the GST portal.

**E-Invoice & E-WayBill Configurations:**

Go to the GST API Configurations window and configure the URL, client ID and Secret key for GST configuration, E-Invoice URL and E-WayBill.

Sandbox Mode - It helps to test and try or to experiment without letting other real functionality hampered.

In the Organization Window, the GSTIN tab GST userID and GST password has to be configured. This will only be useful for the Organization to generate the E-Invoice and E-Waybill.

![Image 13](/images/CeU_Image_13.png)

![Image 14](/images/pAT_Image_14.png)

**Flows :**

**Sales Order -**

Creating a Sales Order, based on the selected address after saving place of supply will automatically update with the selected address.

![Image 15](/images/Fig_Image_15.png)

Adding lines, based on the product selected and the tax category configured in the product window the same tax will be applied. As the Customer is from the same state, CGST and SGST tax will be applied.

![Image 16](/images/Fvb_Image_16.png)

The calculation of CGST and SGST tax can be seen in the line tax grand child tab or Tax tab of child tab. The taxable amount shows the total product net amount(without taxes), tax amount shows the CGST & SGST calculation on the net amount.

![Image 17](/images/Dqf_Image_17.png)

After completing the order we can see in the header, the total gross amount has been calculated (total net amount + GST).

![Image 18](/images/tF0_Image_18.png)

**Goods Shipment/E-Way Bill -**

Referring to the created sales order will proceed with creation of Goods Shipment. \
Create the header referring to SO and save the details, for lines click on create lines from. Completed the Goods Shipment. The document status will change from draft to complete. The E-way Bill generated status is NO, as we have not generated the E-Way bill.

![Image 19](/images/Fpk_Image_19.png)

Click on the E-Way Bill button and the E-Way Bill number will be generated. The status for E-way Bill will change to YES and its generated E-Way Bill number in the header under the E-Way Bill section as given below.

![Image 20](/images/R1C_Image_20.png)

**Sales Invoice/E-Invoice-**

Create Sales Invoice from Goods Shipment, Sales Invoice can also be created from the sales invoice window, also from create line from. E-Invoice generated is NO.

![Image 21](/images/XiK_Image_21.png)

After clicking on the E-Invoice button and refreshing the status will change to YES. After the E-Invoice generation, the E-invoice section will appear with the generated INR number and the QR code.

![Image 22](/images/isF_Image_22.png)
