# Pie Charts

Pie charts are percentage-based. A pie chart models percentage-based data as individual slices of pie. Each data set must be defined as a new instance of the [`SingleValueColumn` object](https://docs.liferay.com/ce/apps/frontend-taglib/latest/javadocs/com/liferay/frontend/taglib/chart/model/SingleValueColumn.html). Follow these steps to configure your portlet to use pie charts. 

1. Import the chart taglib along with the `PieChartConfig` and `SingleValueColumn` classes into your bundle's `init.jsp` file:

    ```jsp
    <%@ taglib prefix="chart" uri="http://liferay.com/tld/chart" %>
    <%@ page import="com.liferay.frontend.taglib.chart.model.percentage.pie.PieChartConfig" %>
    <%@ page import="com.liferay.frontend.taglib.chart.model.SingleValueColumn" %>
    ```

1. Add the following Java scriptlet to the top of your `view.jsp`:

    ```java
    <%
    PieChartConfig _pieChartConfig = new PieChartConfig();

    _pieChartConfig.addColumn(
      new SingleValueColumn("data1", 85.4)
    );

    %>
    ```

1. Add the `<chart>` taglib to the `view.jsp`, passing the `_pieChartConfig` as the `config` attribute's value:

    ```jsp
    <chart:pie
      config="<%= _pieChartConfig %>"
    />
    ```

![A pie chart models percentage-based data as individual slices of pie.](./pie-chart/images/01.png)

Awesome! Now you know how to create pie charts for your apps. 

## Related Topics

* [Donut Charts](./donut-chart.md)
* [Pie Charts](./pie-chart.md)
* [Using Clay Taglibs in Your Portlet](../clay-tag-library.md)