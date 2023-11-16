Data Manager Interface - unfinished
=============================

Data Manager Interface provides the following functions: 

- ven:func:`AddColumn`
- ven:func:`AddTable`
- ven:func:`DeleteRows`
- ven:func:`ExecuteAggregateFunction`
- ven:func:`ExecuteSelectAllLineByLineCommand`
- ven:func:`ExecuteSelectCommand`
- ven:func:`ExportColumnsToCSVFile`
- ven:func:`ExportColumnsToExcelFile`
- ven:func:`ExportColumnsToXMLFile`
- ven:func:`ExportSelectedToCSVFile`
- ven:func:`ExportSelectedToExcelFile`
- ven:func:`ExportSelectedToXMLFile`
- ven:func:`ExportToCSVFile`
- ven:func:`ExportToExcelFile`
- ven:func:`ExportToXMLFile`
- ven:func:`GetRowCount`
- ven:func:`GetSelectCommandRow`
- ven:func:`ImportFromCSVFile`
- ven:func:`ImportFromExcelFile`
- ven:func:`ImportFromXMLFile`
- ven:func:`Init`
- ven:func:`InsertRow`
- ven:func:`InsertSortedRow`
- ven:func:`LoadDataManagerContent`
- ven:func:`RemoveColumn`
- ven:func:`RemoveTable`
- ven:func:`RenameColumn`
- ven:func:`ResetManager`
- ven:func:`SaveDataManagerContent`
- ven:func:`Terminate`
- ven:func:`UpdateRows`

.. ven:function:: AddColumn(variable i_strTableName, variable i_strColumnName, variable i_iColumnType, variable i_bAllowDBNull, variable i_oValue)

This function adds a column to the specified table.

:params i_strTableName: The name of the table
:params i_strColumnName: The name of the column to be added
:params i_iColumnType: The type of column as an integer (

INPUT:
i_strTableName : name of the table (string)
i_strColumnName : name of the column (string)
i_iColumnType : type of the column (int) (see enum DATAMANAGERINTERFACEBASE::VALUTYPE)
                               String = 1, Integer = 2, Double = 3, Boolean = 4
i_bAllowDBNull : set whether null is allowed for the columns (bool)
i_oValue : value which shall bes set to all row values of the new column (object, regarding to 'i_iColumnType')
