---
layout: page
title: Contextual Tabs
---

A contextual tab is visible when a particular object in an app is selected. Contextual tabs cannot exist outside a contextual tab group, so we need to create a contextual tab group (`RibbonContextualTabGroup`) and bind a tab to this group. `RibbonContextualTabGroup` needs to be added to the `Ribbon.ContextualGroups` collection:

```xaml
<!--Contextual Tab Groups-->
<Fluent:Ribbon.ContextualGroups>
    <Fluent:RibbonContextualTabGroup Header="Tools" Visibility="Visible"
        x:Name="toolsGroup" Background="Green" BorderBrush="Green" />
</Fluent:Ribbon.ContextualGroups>
```

And associate a tab to this group:

```xaml
<!--Contextual Tabs-->
<Fluent:RibbonTabItem Header="CT" Group="{Binding ElementName=toolsGroup}"/>
```

`RibbonContextualTabGroup` is not visible by default. To show or hide a contextual tab you must set the `RibbonContextualTabGroup.Visibility` property to `Visible` or `Collapsed`.