---
title: "How to: Set Up Customers for OIOUBL"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "EAN location numbers, customers"
  - "OIOUBL, customers"
  - "customers, setting up for OIOUBL"
  - "electronic invoices, setting up customers"
ms.assetid: e910fe6d-6221-4a04-9fb5-d098a79d396b
caps.latest.revision: 11
ms.author: "edupont"
manager: "terryaus"
translation.priority.ht: 
  - "da-dk"
---
# How to: Set Up Customers for OIOUBL
To create Offentlig Information Online UBL \(OIOUBL\) documents for customers in the public sector, you must add OIOUBL information to the relevant customers.  
  
 This topic only describes fields that apply to OIOUBL. For more information, see [How to: Register New Customers](../../Sales/how-to-register-new-customers.md).  
  
### To set up customers for OIOUBL  
  
1.  In the **Search** box, enter **Customers**, and then choose the related link.  
  
2.  Open the customer that you want to enable for OIOUBL.  
  
3.  On the **Invoicing** FastTab, fill in the fields as described in the following table.  
  
    |[!INCLUDE[bp_tablefield](../../ApplicationDesign/includes/bp_tablefield_md.md)]|[!INCLUDE[bp_tabledescription](../../ApplicationDesign/includes/bp_tabledescription_md.md)]|  
    |---------------------------------|---------------------------------------|  
    |**\($ T\_18\_13600 EAN No. $\)**|Enter the European Article Numbering \(EAN\) location number for the customer. For more information, see [EAN Location Number](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Denmark/ean-location-number.md).|  
    |**\($ T\_18\_13601 Account Code $\)**|Enter the account code for the customer.<br /><br /> Customers in the public sector provide an account code when they place an order or requisition. Based on the value of this field, the account code is included in the OIOUBL documents that you create in [!INCLUDE[navnow](../../ApplicationDesign/includes/navnow_md.md)]. In accordance with **Lov om Offentlige Betalinger** and related statutes, the customer is entitled to withhold payment until they receive an invoice with the relevant account code. For more information, see [\($ T\_18\_13601 Account Code $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Denmark/-$-t_18_13601-account-code-$-.md).|  
    |**\($ T\_18\_13604 OIOUBL Profile Code $\)**|Specifies the profile that this customer requires for electronic documents if this is different from the default profile that you specified in the **\($ N\_459 Sales & Receivables Setup $\)** window.|  
    |**\($ T\_18\_13605 OIOUBL Profile Code Required $\)**|Specifies if this customer requires a profile code for electronic documents. **Tip:**  If the **\($ T\_18\_13605 OIOUBL Profile Code Required $\)** field is selected, you cannot post a sales document for this customer unless you have specified a profile.|  
  
 These fields are specific to OIOUBL. The values are used in all OIOUBL documents that you create for this customer. For more information, see [OIOUBL Electronic Invoicing Overview](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Denmark/oioubl-electronic-invoicing-overview.md).  
  
## See Also  
 [How to: Register New Customers](../../Sales/how-to-register-new-customers.md)   
 [How to: Set Up OIOUBL](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Denmark/how-to-set-up-oioubl.md)   
 [How to: Create Electronic Documents by Using OIOUBL](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Denmark/how-to-create-electronic-documents-by-using-oioubl.md)   
 [OIOUBL Electronic Invoicing Overview](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Denmark/oioubl-electronic-invoicing-overview.md)   
 [EAN Location Number](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Denmark/ean-location-number.md)   
 [\($ T\_18\_13600 EAN No. $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Denmark/-$-t_18_13600-ean-no.-$-.md)   
 [\($ T\_18\_13601 Account Code $\)](../../LocalFunctionalityForMicrosoftDynamicsNav2016/Denmark/-$-t_18_13601-account-code-$-.md)