---
title: The objects you are adding to the designer use a different data connection than the designer is currently using
ms.date: 11/04/2016
ms.topic: reference
ms.assetid: 332ed2f3-3377-4d51-8e3b-fdb98231978e
author: gewarren
ms.author: gewarren
manager: douge
ms.technology: vs-data-tools
ms.workload:
  - "data-storage"
---
# The objects you are adding to the designer use a different data connection than the designer

The objects you are adding to the designer use a different data connection than the designer is currently using. Do you want to replace the connection used by the designer?

When you add items to the [!INCLUDE[vs_ordesigner_long](../data-tools/includes/vs_ordesigner_long_md.md)] ([!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)]), all items use one shared data connection. (The design surface represents the <xref:System.Data.Linq.DataContext>, which uses a single connection for all objects on the surface.) If you add an object to the designer that uses a data connection that differs from the data connection currently being used by the designer, this message appears. To resolve this error, you can choose to maintain the existing connection. If you make this choice, the selected object will not be added. Alternatively, you can choose to add the object and reset the <xref:System.Data.Linq.DataContext> connection to the new connection.

> [!NOTE]
> If you click **Yes**, all entity classes on the [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)] are mapped to the new connection.

## To replace the existing connection with the connection used by the selected object

- Click **Yes**.

    The selected object is added to the [!INCLUDE[vs_ordesigner_short](../data-tools/includes/vs_ordesigner_short_md.md)], and the DataContext.Connection is set to the new connection.

## To continue to use the existing connection and cancel adding the selected object

- Click **No**.

    The action is canceled. The DataContext.Connection remains set to the existing connection.

## See also

- [O/R Designer messages](../data-tools/o-r-designer-messages.md)
- [LINQ to SQL tools in Visual Studio](../data-tools/linq-to-sql-tools-in-visual-studio2.md)
