---
title: OptionGroup.OnDblClick Property (Access)
keywords: vbaac10.chm10867
f1_keywords:
- vbaac10.chm10867
ms.prod: access
api_name:
- Access.OptionGroup.OnDblClick
ms.assetid: f1dfb135-716f-4db3-1d4a-89c4b28b40f8
ms.date: 06/08/2017
---


# OptionGroup.OnDblClick Property (Access)

Sets or returns the value of the  **On Dbl Click** box in the **Properties** window. Read/write **String**.


## Syntax

 _expression_. 'OnDblClick'

 _expression_ A variable that represents an **OptionGroup** object.


## Remarks

This property is helpful for programmatically changing the action Microsoft Access takes when an event is triggered. For example, between event calls you may want to change an expression's parameters, or switch from an event procedure to an expression or macro, depending on the circumstances under which the event was triggered. 

The  **DblClick** event occurs when a user presses and releases the left mouse button twice over an object within the double-click time limit of the system.

The  **OnDblClick** value will be one of the following, depending on the selection chosen in the **Choose Builder** window (accessed by clicking the **Build** button next to the **On Dbl Click** box in the object's **Properties** window):


- If Expression Builder is chosen, the value will be "= _expression_", where  _expression_ is the expression from the Expression Builder window.
    
- If Macro Builder is chosen, the value is the name of the macro. 
    
- If Code Builder is chosen, the value will be "[Event Procedure]". 
    
If the  **On Dbl Click** box is blank, the property value is an empty string.


## Example

The following example associates the  **Click** event with the "OK_DblClick" event procedure for the button named "OK" on the "Order Entry" form, if there is currently no association.


```vb
With Forms("Order Entry").Controls("OK") 
 If .OnDblClick = "" Then 
 .OnDblClick = "[Event Procedure]" 
 End If 
End With 

```


## See also


[OptionGroup Object](Access.OptionGroup.md)
