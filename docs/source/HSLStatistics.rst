HSLStatistics - unfinished
===================================

https://github.com/theonetruenerd/VenusPackages/blob/main/HSLStatistics.pkg

The HSLStatistics library is designed to easily allow the user to perform basic statistical functions easily. It adds the following functions:

  - :py:func:`Stat_Average`
  - :py:func:`Stat_StdDeviation`
  - :py:func:`Stat_CorrelationCoefficent`
  - :py:func:`Stat_RSQ`
  - :py:func:`Stat_Slope`
  - :py:func:`Stat_Intercept`
  - :py:func:`Stat_Min`
  - :py:func:`Stat_Max`

.. py:function:: Stat_Average(array DataArray)

  This function returns the average of a data set input as an array

  :params DataArray: The input array of data from which the average is calculated
  :type DataArray: Array
  :return: The calculated average of the array
  :rtype: Variable

.. py:function:: Stat_StdDeviation(array DataArray)

  This function returns the standard deviation of a data set input as an array

  :params DataArray: The input array of data from which the standard deviation is calculated
  :type DataArray: Array
  :return: The calculated standard deviation of the array
  :rtype: Variable

.. py:function:: Stat_CorrelationCoefficient(array XArray, array YArray)

  This function returns the correlation coefficient (r-value) of a paired data set

  :params XArray: The array of X data values in the paired set
  :params YArray: The array of Y data values in the paired set
  :type XArray: Array
  :type YArray: Array
  :return: The r-value of the paired data set
  :rtype: Variable

.. py:function:: Stat_RSQ(array XArray, array YArray)

  This function returns the pearson coefficient (r^2) of a paired data set

  :params XArray: The array of X data values in the paired set
  :params YArray: The array of Y data values in the paired set
  :type XArray: Array
  :type YArray: Array
  :return: The pearson coefficient of the paired data set
  :rtype: Variable

.. py:function:: Stat_Slope(array XArray, array YArray)

  This function returns the slope of the best fit line of a paired data set

  :params XArray: The array of X data values in the paired set
  :params YArray: The array of Y data values in the paired set
  :type XArray: Array
  :type YArray: Array
  :return: The slope of the best fit line
  :rtype: Variable

.. py:function:: Stat_Intercept(array XArray, array YArray)

  This function returns the intercept of the best fit line of a paired data set

  :params XArray: The array of X data values in the paired set
  :params YArray: The array of Y data values in the paired set
  :type XArray: Array
  :type YArray: Array
  :return: The intercept of the line of best fit
  :rtype: Variable

.. py:function:: Stat_Min(array DataArray)

  This function returns the lowest value of a dataset

  :params DataArray: The array for the minimum to be searched in
  :type DataArray: Array
  :return: The lowest value of the dataset
  :rtype: Variable

.. py:functions:: Stat_Max(array DataArray)

  This function returns the hgihest value of a dataset

  :params DataArray: The array for the minimum to be searched in
  :type DataArray: Array
  :return: The lowest value of the dataset
  :rtype: Variable
