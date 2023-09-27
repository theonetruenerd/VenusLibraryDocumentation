Data Manager Interface - unfinished
=============================

Data Manager Interface provides the following functions: 

- py:func:`AddColumn`
- py:func:`AddTable`
- py:func:`DeleteRows`
- py:func:`ExecuteAggregateFunction`
- py:func:`ExecuteSelectAllLineByLineCommand`
- py:func:`ExecuteSelectCommand`
- py:func:`ExportColumnsToCSVFile`
- py:func:`ExportColumnsToExcelFile`
- py:func:`ExportColumnsToXMLFile`
- py:func:`ExportSelectedToCSVFile`
- py:func:`ExportSelectedToExcelFile`
- py:func:`ExportSelectedToXMLFile`
- py:func:`ExportToCSVFile`
- py:func:`ExportToExcelFile`
- py:func:`ExportToXMLFile`
- py:func:`GetRowCount`
- py:func:`GetSelectCommandRow`
- py:func:`ImportFromCSVFile`
- py:func:`ImportFromExcelFile`
- py:func:`ImportFromXMLFile`
- py:func:`Init`
- py:func:`InsertRow`
- py:func:`InsertSortedRow`
- py:func:`LoadDataManagerContent`
- py:func:`RemoveColumn`
- py:func:`RemoveTable`
- py:func:`RenameColumn`
- py:func:`ResetManager`
- py:func:`SaveDataManagerContent`
- py:func:`Terminate`
- py:func:`UpdateRows`

.. py:function:: AddColumn(variable i_strTableName, variable i_strColumnName, variable i_iColumnType, variable i_bAllowDBNull, variable i_oValue)

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
