---
title: Bookmark Object (Word)
keywords: vbawd10.chm2408
f1_keywords:
- vbawd10.chm2408
ms.prod: word
api_name:
- Word.Bookmark
ms.assetid: be6b0c7b-60ca-97e7-ef19-6de335da3197
ms.date: 06/08/2017
---


# Bookmark Object (Word)

Represents a single bookmark in a document, selection, or range. The  **Bookmark** object is a member of the **[Bookmarks](../../../api/Word.bookmarks.md)** collection. The **Bookmarks** collection includes all the bookmarks listed in the **Bookmark** dialog box ( **Insert** menu).


## Remarks

Using the Bookmark Object

Use  **Bookmarks** (index), where index is the bookmark name or index number, to return a single **Bookmark** object. You must exactly match the spelling (but not necessarily the capitalization) of the bookmark name. The following example selects the bookmark named "temp" in the active document.




```
ActiveDocument.Bookmarks("temp").Select
```

The index number represents the position of the bookmark in the  **[Selection](../../../api/Word.Selection.md)** or **[Range](range-object-word.md)** object. For the **[Document](../Objects-Properties-Methods/document-object-word.md)** object, the index number represents the position of the bookmark in the alphabetical list of bookmarks in the **Bookmarks** dialog box (click **Name** to sort the list of bookmarks alphabetically). The following example displays the name of the second bookmark in the **Bookmarks** collection.




```
MsgBox ActiveDocument.Bookmarks(2).Name
```

Use the  **[Add](../../../api/Word.Bookmarks.Add.md)** method to add a bookmark to a document range. The following example marks the selection by adding a bookmark named "temp."




```
ActiveDocument.Bookmarks.Add Name:="temp", Range:=Selection.Range
```

Remarks

Use the  **BookmarkID** property with a range or selection object to return the index number of a **Bookmark** object in the **Bookmarks** collection. The following example displays the index number of the bookmark named "temp" in the active document.




```
MsgBox ActiveDocument.Bookmarks("temp").Range.BookmarkID
```

You can use [predefined bookmarks](../Miscellaneous/predefined-bookmarks.md)with the  **Bookmarks** property. The following example sets the bookmark named "currpara" to the location marked by the predefined bookmark named "\Para".




```
ActiveDocument.Bookmarks("\Para").Copy "currpara"
```

Use the  **[Exists](../../../api/Word.Bookmarks.Exists.md)** method to determine whether a bookmark already exists in the selection, range, or document. The following example ensures that the bookmark named "temp" exists in the active document before selecting the bookmark.




```
If ActiveDocument.Bookmarks.Exists("temp") = True Then 
 ActiveDocument.Bookmarks("temp").Select 
End If
```


## Methods



|**Name**|
|:-----|
|[Copy](../../../api/Word.Bookmark.Copy.md)|
|[Delete](../../../api/Word.Bookmark.Delete.md)|
|[Select](../../../api/Word.Bookmark.Select.md)|

## Properties



|**Name**|
|:-----|
|[Application](../../../api/Word.Bookmark.Application.md)|
|[Column](../../../api/Word.Bookmark.Column.md)|
|[Creator](../../../api/Word.Bookmark.Creator.md)|
|[Empty](../../../api/Word.Bookmark.Empty.md)|
|[End](../../../api/Word.Bookmark.End.md)|
|[Name](../../../api/Word.Bookmark.Name.md)|
|[Parent](../../../api/Word.Bookmark.Parent.md)|
|[Range](../../../api/Word.Bookmark.Range.md)|
|[Start](../../../api/Word.Bookmark.Start.md)|
|[StoryType](../../../api/Word.Bookmark.StoryType.md)|

## See also


#### Other resources


[Word Object Model Reference](../../../api/overview/object-model-word-vba-reference.md)