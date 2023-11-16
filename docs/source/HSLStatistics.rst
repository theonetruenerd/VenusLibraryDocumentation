HSLStatistics
===================================

https://github.com/theonetruenerd/VenusPackages/blob/main/HSLStatistics.pkg

The HSLStatistics library is designed to easily allow the user to perform basic statistical functions easily. It adds the following functions:

  - :ven:func:`Stat_Average`
  - :ven:func:`Stat_StdDeviation`
  - :ven:func:`Stat_CorrelationCoefficent`
  - :ven:func:`Stat_RSQ`
  - :ven:func:`Stat_Slope`
  - :ven:func:`Stat_Intercept`
  - :ven:func:`Stat_Min`
  - :ven:func:`Stat_Max`

.. ven:function:: Stat_Average(array DataArray)

  This function returns the average of a data set input as an array

  :params DataArray: The input array of data from which the average is calculated
  :type DataArray: Array
  :return: The calculated average of the array
  :rtype: Variable

.. ven:function:: Stat_StdDeviation(array DataArray)

  This function returns the standard deviation of a data set input as an array

  :params DataArray: The input array of data from which the standard deviation is calculated
  :type DataArray: Array
  :return: The calculated standard deviation of the array
  :rtype: Variable

.. ven:function:: Stat_CorrelationCoefficient(array XArray, array YArray)

  This function returns the correlation coefficient (r-value) of a paired data set

  :params XArray: The array of X data values in the paired set
  :params YArray: The array of Y data values in the paired set
  :type XArray: Array
  :type YArray: Array
  :return: The r-value of the paired data set
  :rtype: Variable

.. ven:function:: Stat_RSQ(array XArray, array YArray)

  This function returns the pearson coefficient (r^2) of a paired data set

  :params XArray: The array of X data values in the paired set
  :params YArray: The array of Y data values in the paired set
  :type XArray: Array
  :type YArray: Array
  :return: The pearson coefficient of the paired data set
  :rtype: Variable

.. ven:function:: Stat_Slope(array XArray, array YArray)

  This function returns the slope of the best fit line of a paired data set

  :params XArray: The array of X data values in the paired set
  :params YArray: The array of Y data values in the paired set
  :type XArray: Array
  :type YArray: Array
  :return: The slope of the best fit line
  :rtype: Variable

.. ven:function:: Stat_Intercept(array XArray, array YArray)

  This function returns the intercept of the best fit line of a paired data set

  :params XArray: The array of X data values in the paired set
  :params YArray: The array of Y data values in the paired set
  :type XArray: Array
  :type YArray: Array
  :return: The intercept of the line of best fit
  :rtype: Variable

.. ven:function:: Stat_Min(array DataArray)

  This function returns the lowest value of a dataset

  :params DataArray: The array for the minimum to be searched in
  :type DataArray: Array
  :return: The lowest value of the dataset
  :rtype: Variable

.. ven:functions:: Stat_Max(array DataArray)

  This function returns the hgihest value of a dataset

  :params DataArray: The array for the minimum to be searched in
  :type DataArray: Array
  :return: The lowest value of the dataset
  :rtype: Variable
