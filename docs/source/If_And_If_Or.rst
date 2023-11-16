If_And_If_Or
===================================

https://github.com/theonetruenerd/VenusPackages/blob/main/If_And_If_Or.pkg

The if_and_if_or library adds two functions:

- :ven:func:`if_and`
- :ven:func:`if_or`

.. ven:function:: if_and(variable iVar1, variable iVar2, variable iVar3, variable iVar4)
	
	This function checks variable iVar1 against iVar2 and iVar3 against iVar4; if both statements are true then the function returns a 1, otherwise it returns a 0

	:params iVar1: Variable to be checked against iVar2
	:params iVar2: Variable to be checked against iVar1
	:params iVar3: Variable to be checked against iVar4
	:params iVar4: Variable to be checked against iVar3
	:type iVar1: Variable
	:type iVar2: Variable
	:type iVar3: Variable
	:type iVar4: Variable
	:return: 1 if both true, 0 otherwise
	:rtype: Variable

.. ven:function:: if_or(variable iVar1, variable iVar2, variable iVar3, variable iVar4)

	This function checks variable iVar1 against iVar2 and iVar3 against iVar4; if at least one of the statements is true then the function will return a 1, otherwise it will return a 0

	:params iVar1: Variable to be checked against iVar2
	:params iVar2: Variable to be checked against iVar1
	:params iVar3: Variable to be checked against iVar4
	:params iVar4: Variable to be checked against iVar3
	:type iVar1: Variable
	:type iVar2: Variable
	:type iVar3: Variable
	:type iVar4: Variable
	:return: 1 if at least one is true, 0 if false
	:rtype: Variable
