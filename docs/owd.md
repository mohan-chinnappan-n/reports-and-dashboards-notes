## Org-wide-defaults (OWD)


Organization-wide sharing defaults set the baseline access for your records. You can set the defaults separately for different objects.

When you update organization-wide defaults, sharing recalculation applies the access changes to your records. If you have **a lot of data**, the update can take longer.

If you are **increasing** the default access, such as from **Public Read Only** to **Public Read/Write**, your changes take effect **immediately**. All users get access based on the updated default access. Sharing recalculation is then run asynchronously to ensure that all redundant access from manual or sharing rules are removed.

If you are **decreasing** the default access, such as from **Public Read/Write** to **Public Read Only**, your changes take effect after recalculation is run.

When a custom object is on the **detail** side of a **master-detail** relationship with a standard object, its organization-wide default is set to **Controlled by Parent** and it is not editable.

The OWD settings can’t be changed from **private to public** for a custom object if Apex code uses the sharing entries associated with that object. 

For example, if Apex code retrieves the users and groups who have sharing access on a custom object Invoice__c (represented as Invoice__share in the code), you can’t change the object’s organization-wide sharing setting from private to public.



### Example

When the default access for **contacts** is **Controlled by Parent** and you increase the default access for **accounts, opportunities, or cases**, the changes take effect after recalculation is run.


### Notes:

Service contracts are always Private.



### References 

1. [Set Your Organization-Wide Sharing Defaults](https://help.salesforce.com/articleView?id=admin_sharing.htm&type=0)
