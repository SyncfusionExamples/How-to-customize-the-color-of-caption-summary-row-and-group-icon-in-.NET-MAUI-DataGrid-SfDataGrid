# How to customize the color of caption summary row and group icon in .NET MAUI DataGrid (SfDataGrid) ?
In this article, we will show you how to customize the color of caption summary row and group icon in [.NET MAUI DataGrid](https://www.syncfusion.com/maui-controls/maui-datagrid).

## Xaml
The code below defines a resource in a .NET MAUI ContentPage that sets the group icon color to orange. It also sets the caption summary row background to light blue and configures to group data by EmployeeID and Name columns in SfDataGrid.

```
<ContentPage.BindingContext>
    <local:EmployeeViewModel x:Name="viewModel" />
</ContentPage.BindingContext>

<ContentPage.Resources>
    <ResourceDictionary>
        <Color x:Key="SfDataGridGroupIconColor">Orange</Color>
    </ResourceDictionary>
</ContentPage.Resources>

<syncfusion:SfDataGrid x:Name="dataGrid"
                    AllowGroupExpandCollapse="True"
                    GroupingMode="Multiple"
                    ColumnWidthMode="Auto"
                    GridLinesVisibility="Both"
                    HeaderGridLinesVisibility="Both"
                    AutoGenerateColumnsMode="None"
                    ItemsSource="{Binding Employees}">

    <syncfusion:SfDataGrid.DefaultStyle>
        <syncfusion:DataGridStyle CaptionSummaryRowBackground="LightBlue" />
    </syncfusion:SfDataGrid.DefaultStyle>

    <syncfusion:SfDataGrid.GroupColumnDescriptions>
        <syncfusion:GroupColumnDescription ColumnName="EmployeeID" />
        <syncfusion:GroupColumnDescription ColumnName="Name" />
    </syncfusion:SfDataGrid.GroupColumnDescriptions>

    <syncfusion:SfDataGrid.Columns>
        <syncfusion:DataGridNumericColumn MappingName="EmployeeID"
                                        Format="#"
                                        HeaderText="Employee ID" />
        <syncfusion:DataGridTextColumn MappingName="Name"
                                    HeaderText="Employee Name" />
        <syncfusion:DataGridTextColumn MappingName="Title"
                                    HeaderText="Designation" />
        <syncfusion:DataGridDateColumn MappingName="HireDate"
                                    HeaderText="Hire Date" />

    </syncfusion:SfDataGrid.Columns>
</syncfusion:SfDataGrid>
```

<img src="https://support.syncfusion.com/kb/agent/attachment/inline?token=eyJhbGciOiJodHRwOi8vd3d3LnczLm9yZy8yMDAxLzA0L3htbGRzaWctbW9yZSNobWFjLXNoYTI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6IjQwNTE5Iiwib3JnaWQiOiIzIiwiaXNzIjoic3VwcG9ydC5zeW5jZnVzaW9uLmNvbSJ9.mbR6I-uZuONbRVdCkUH9ipV7eBwitN1y7ko9NOOuX_A" width=800/>

[View sample in GitHub](https://github.com/SyncfusionExamples/How-to-customize-the-color-of-caption-summary-row-and-group-icon-in-.NET-MAUI-DataGrid-SfDataGrid)

Take a moment to explore this [documentation](https://help.syncfusion.com/maui/datagrid/overview), where you can find more information about Syncfusion .NET MAUI DataGrid (SfDataGrid) with code examples. Please refer to this [link](https://www.syncfusion.com/maui-controls/maui-datagrid) to learn about the essential features of Syncfusion .NET MAUI DataGrid (SfDataGrid).
 
##### Conclusion
 
I hope you enjoyed learning about how to customize the color of caption summary row and group icon in SfDataGrid.
 
You can refer to our [.NET MAUI DataGrid’s feature tour](https://www.syncfusion.com/maui-controls/maui-datagrid) page to learn about its other groundbreaking feature representations. You can also explore our [.NET MAUI DataGrid Documentation](https://help.syncfusion.com/maui/datagrid/getting-started) to understand how to present and manipulate data. 
For current customers, you can check out our .NET MAUI components on the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/maui) to explore our .NET MAUI DataGrid and other .NET MAUI components.
 
If you have any queries or require clarifications, please let us know in the comments below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [Direct-Trac](https://support.syncfusion.com/create) or [feedback portal](https://www.syncfusion.com/feedback/maui?control=sfdatagrid), or the feedback portal. We are always happy to assist you!