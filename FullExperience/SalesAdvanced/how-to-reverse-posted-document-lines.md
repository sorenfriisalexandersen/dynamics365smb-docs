---
title: "How to: Reverse Posted Document Lines"
ms.custom: na
ms.date: "03-03-2017"
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: "article"
helpviewer_keywords: 
  - "reversing, posted document lines"
  - "sales credit memos, reversing posted document lines"
  - "copying, posted document lines"
ms.assetid: 48d208dd-f5f8-4801-b3b1-5e31eaed5b9f
caps.latest.revision: 5
ms.author: "sgroespe"
manager: "terryaus"
translation.priority.ht: 
  - "da-dk"
  - "de-at"
  - "de-ch"
  - "de-de"
  - "en-au"
  - "en-ca"
  - "en-gb"
  - "en-in"
  - "en-nz"
  - "es-es"
  - "es-mx"
  - "fi-fi"
  - "fr-be"
  - "fr-ca"
  - "fr-ch"
  - "fr-fr"
  - "is-is"
  - "it-ch"
  - "it-it"
  - "nb-no"
  - "nl-be"
  - "nl-nl"
  - "ru-ru"
  - "sv-se"
---
# How to: Reverse Posted Document Lines
The **Get Posted Document Lines to Reverse** function is useful when you need to copy one or more lines that appear in one or more posted documents. This is particularly helpful when you are creating a return order or a credit memo and you want the costs to be an exact reversal of the original order. This means that the costs on the credit memo reflect the cost that was on the original document and that the prices include any discounts that may have been applied to that order.  
  
### To use the Get Posted Document Lines to Reverse function  
  
1.  In the document, on the **Actions** tab, in the **Functions** group, choose **Get Posted Document Lines to Reverse**. If you are working with a sales document, the **[\($ N\_5850 Posted Sales Document Lines $\)](../Topic/\($%20N_5850%20Posted%20Sales%20Document%20Lines%20$\).md)** window opens. If you are working with a purchase document, the **[\($ N\_5855 Posted Purchase Document Lines $\)](../Topic/\($%20N_5855%20Posted%20Purchase%20Document%20Lines%20$\).md)** window opens.  
  
2.  At the top of the window, select the **Show Reversible Lines Only** field if you want to see only lines that have quantities that have not yet been returned, or in the case of purchase lines, sold or consumed. For example, if a posted sales invoice quantity has already been returned, you may not want to return that quantity on a new sales return document. By selecting the **Show Reversible Lines Only** field, you can hide those posted document lines where the full quantities have already been returned, sold, or consumed.  
  
    > [!NOTE]  
    >  This field only works for posted shipments or receipts, and posted invoice lines, not for posted return or posted credit memo lines.  
  
3.  At the left side of the window, the different document types are listed, and the number in parentheses shows the number of documents available of each document type. In the **Document Type Filter** field, select the type of posted document lines you would like to use.  
  
4.  Select the lines that you would like to copy to the new document.  
  
    > [!NOTE]  
    >  If you use Ctrl\+A to select all lines, all lines within the filter you have set are copied, but the **Show Reversible Quantity Only** filter is ignored. For example, suppose you have filtered the lines to a particular document number with two lines, one of which has already been returned. Even if the **Show Reversible Quantity Only** field is selected, if you press Ctrl\+A to copy all lines, both lines are copied, instead of only the one that has not yet been reversed.  
  
5.  Choose the **OK** button to copy the lines to the new document. Press F5 to refresh the window and see the results in the document.  
  
 The following processes occur:  
  
-   For posted document lines of the type **Item**, a new document line is created that is a copy of the posted document line, with the quantity that has not yet been reversed. The **[\($ T\_37\_5811 Appl.\-from Item Entry $\)](../Topic/\($%20T_37_5811%20Appl.-from%20Item%20Entry%20$\).md)** field, for sales documents, or the **[\($ T\_39\_38 Appl.\-to Item Entry $\)](../Topic/\($%20T_39_38%20Appl.-to%20Item%20Entry%20$\).md)** field, for purchase documents, is filled in as appropriate, with the number of the item ledger entry of the posted document line.  
  
-   For posted document lines that are not of the type **Item**, such as item charges, a new document line is created that is a copy of the original posted document line.  
  
-   Calculates the **Unit Cost \(LCY\)** field on the new line from the costs on the corresponding item ledger entries.  
  
-   If the copied document is a posted shipment, posted receipt, posted return receipt, or posted return shipment, the unit price is calculated automatically from the item card.  
  
-   If the copied document is a posted invoice or credit memo, the unit price, invoice discounts, and line discounts from the posted document line are copied.  
  
-   If the posted document line contains item tracking lines, the **[\($ T\_336\_5811 Appl.\-from Item Entry $\)](../Topic/\($%20T_336_5811%20Appl.-from%20Item%20Entry%20$\).md)** field on the item tracking lines is filled with the appropriate item ledger entry numbers from the posted item tracking lines.  
  
 When you copy from a posted invoice or posted credit memo, the program copies any relevant invoice discounts and line discounts as valid at the time of posting that document from the posted document line to the new document line. Be aware, however, that if the **Calc. Inv. Discount** option is activated in either the purchases and payables setup or the sales and receivables setup, as pertains to the situation, the invoice discount will be newly calculated when you post the new document line. It can be, therefore, that the line amount for the new line is different than the line amount for the posted document line, depending on the new calculation of the invoice discount.  
  
> [!NOTE]  
>  Exact cost reversing of item tracking lines is not available from the purchase invoice or purchase credit memo documents.  
>   
>  If part of the quantity of the posted document line has already been reversed or sold or consumed, a line is created for only the quantity that remains in inventory or that has not been returned. If the full quantity of the posted document line has already been reversed, a new document line is not created.  
>   
>  If the flow of goods in the posted document is the same as the flow of goods in the new document, a copy of the original posted document line in the new document is created. The **Appl.\-from Item Entry** field, for sales documents, or **Appl.\-to Item Entry** field, for purchase documents, is not filled in because, in this case, exact cost reversing is not possible. For example, if you use the **Get Posted Document Lines to Reverse** function to get a posted sales credit memo line for a new sales credit memo, only the original posted credit memo line is copied to the new credit memo.  
  
## See Also  
 [\($ N\_6630 Sales Return Order $\)](../Topic/\($%20N_6630%20Sales%20Return%20Order%20$\).md)   
 [\($ N\_6640 Purchase Return Order $\)](../Topic/\($%20N_6640%20Purchase%20Return%20Order%20$\).md)   
 [How to: Assign Exact Cost Reversing in Sales](../Finance/how-to-assign-exact-cost-reversing-in-sales.md)   
 [How to: Assign Exact Cost Reversing in Purchases](../Finance/how-to-assign-exact-cost-reversing-in-purchases.md)   
 [How to: Close Open Item Ledger Entries Resulting from Fixed Application in the Item Journal](../Finance/how-to-close-open-item-ledger-entries-resulting-from-fixed-application-in-the-item-journal.md)