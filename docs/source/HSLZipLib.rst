HSLZipLib
================================

https://github.com/theonetruenerd/VenusPackages/blob/main/HSLZipLib.pkg

HSLZipLib is a library that allows you to create zip folders, as well as unzip and extract folders from them. It adds the following four functions:

- :ven:func:`UnpackArchive`
- :ven:func:`AddItemToArchive`
- :ven:func:`InitializeArchive`
- :ven:func:`PackArchive`

.. ven:function:: UnpackArchive(variable i_strArchiveName, variable i_strPathOutput)

  The unpack archive function unzips a zip folder and extracts the contents to the specified location.

  :params i_strArchiveName: The full name and path to the zip folder you wish to unzip, including the .zip file extension
  :params i_strPathOutput: The full name and path of the folder you would like to create when extracting the zip file, with no extension
  :type i_strArchiveName: Variable
  :type i_strPathOutput: Variable
  :return: Boolean confirming whether unzipping the archive was successful or not
  :rtype: Boolean

.. ven:function:: AddItemToArchive(variable i_strFileOrDirectoryName, variable i_strDirectoryPathInArchive)

  This function specifies a file or directory which will be added to the zip file which will be generated with the :ven:func:`PackArchive` function. 

  :params i_strFileOrDirectoryName: The path to the file or directory that you wish to include in the zip folder. File extension required for files, no extension required for folders.
  :params i_strDirectoryPathInArchive: The path to the desired location of the file within the zip folder.
  :type i_strFileOrDirectoryName: Variable
  :type i_strDirectoryPathInArchive: Variable
  :return: Boolean confirming whether adding the file or directory to the archive was successful
  :rtype: Boolean

.. ven:function:: InitializeArchive(variable i_strArchiveName)

  This function initializes whatever archive is specified. It is required to call this function for each archive you are interacting with, in advance of calling any of the otehr functions. 

  :params i_strArchiveName: The name of the desired zip file; can be a file that already exists or one that doesn't exist yet and will be created
  :type i_strArchiveName: Variable
  :return: None
  :rtype: N/A

.. ven:function:: PackArchive()

  This function zips/packs whichever archive was most recently initialized. 

  :return: Boolean confirming whether zipping the archive was successful or not
  :rtype: Boolean
