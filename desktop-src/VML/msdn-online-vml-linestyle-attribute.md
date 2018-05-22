---
title: VML LineStyle Attribute
description: VML LineStyle Attribute
ms.assetid: 'eec5c1f3-5256-4104-b021-ebf799665752'
---

# VML LineStyle Attribute

This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9. Webpages and applications that rely on VML should be [migrated to SVG](http://go.microsoft.com/fwlink/p/?LinkID=236964) or other widely supported standards.

> [!Note]  
> As of December 2011, this topic has been archived. As a result, it is no longer actively maintained. For more information, see [Archived Content](https://msdn.microsoft.com/library/hh772377). For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](http://go.microsoft.com/fwlink/p/?linkid=204313).

 

Defines the line style of the stroke. Read/write. **String**.

**Applies To**

[Stroke](msdn-online-vml-stroke-element.md)

**Tag Syntax**

&lt;v: *element* linestyle=" *expression* "&gt;

**Script Syntax**

*element* .linestyle="*expression*"

*expression*=*element*.linestyle

**Remarks**

Values include:

-   Single (default)
-   ThinThin
-   ThinThick
-   ThickThin
-   ThickBetweenThin

*VML Standard Attribute*

**Example**

A double line is drawn with two thin strokes.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke linestyle="thinthin" />
   </v:line>
```



 

 



