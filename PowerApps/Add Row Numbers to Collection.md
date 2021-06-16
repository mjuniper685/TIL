# Adding Row Numbers to a Collection

I needed to add row numbers to a collection to use as a unique Id for a gallery update. The following worked courtesy of [PowerApps Guide](http://powerappsguide.com/blog/post/generating-row-numbers)

```
Clear(colNumberedInvoices);
ForAll(Invoices, 
       Collect(colNumberedInvoices,
               Last(FirstN(AddColumns(Invoices,
                                "RowNumber",
                                CountRows(colNumberedInvoices)+1
                           ), 
                           CountRows(colNumberedInvoices)+1
                    )
               )    
       )
)
```