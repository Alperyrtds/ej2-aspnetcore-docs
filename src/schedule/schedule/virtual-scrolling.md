---
title: "Virtual scrolling in ASP.Net Core Scheduler"
component: "Scheduler"
description: "This section demonstrtes how to dynamically load the resources and events as you scroll through the scheduler"
---

# Virtual scrolling

To achieve better performance in the Scheduler when loading a large number of resources and events, we have added virtual scrolling support in the timeline views to load a large set of resources and events instantly as you scroll. You can dynamically load large number of resources and events in timeline view of the Scheduler by setting `true` to the `allowVirtualScrolling` property within the timeline view-specific settings. The virtual loading of events is possible in Agenda view, by setting `allowVirtualScrolling` property to `true` within the agenda view specific settings.

{% aspTab template="schedule/virtual-scroll/vScroll", sourceFiles="data.cs"  %}

{% endaspTab %}

**Note:** For now, the virtual loading of resources and events is available only for timeline views. In the future, we plan to port the same virtual loading on all other applicable Scheduler views.

> You can refer to our [ASP.NET Core Scheduler](https://www.syncfusion.com/aspnet-core-ui-controls/scheduler) feature tour page for its groundbreaking feature representations. You can also explore our [ASP.NET Core Scheduler example](https://ej2.syncfusion.com/aspnetcore/Schedule/Overview#/material) to knows how to present and manipulate data.
