# Testing

**Base test elements**

To perform base testing you may use Verify expression and Verify expression with operator elements. These elements execute given expression and throw exception in case of failure. When project starts all test elements show <img src="../../.gitbook/assets/TestNone.png" alt="" data-size="line"> icon, but after verification they change it to <img src="../../.gitbook/assets/TestSuccess.png" alt="" data-size="line"> on success or <img src="../../.gitbook/assets/TestFail.png" alt="" data-size="line"> in case of failure.

Verify output with operator is more complex element. This element executes supplied element (Get attribute for example) and verifies it's output with given expression. The most useful case for this element is UI-testing.

**Test data**

Test data source is a part of the project and specifies in process properties

![](<../../.gitbook/assets/image (71).png>)



Test data path may be absolute or relative. Test data file is an Excel document in a special format:

| Variable 1 name | Variable 2 name | Variable n name |
| --------------- | --------------- | --------------- |
| Value 1         | Value 2         | Value 3         |
| Value 1n        | Value 2n        | Value 3n        |

In order to get a value from the file you need to use Get next local test data element. This element can either set test data into a variable or map data to variables by their names.

You may create test data file manually or using current variables values by clicking Process -> Dump variables menu and setting path to test data file in a window

![](<../../.gitbook/assets/image (78).png>)



**Mocks**

Mock element has two containers: Element and Mock

![](<../../.gitbook/assets/image (87).png>)

Element container executes if the mock is turned off and Mock container executes if on. Turning the mock on and off is available through it's properties or by clicking <img src="../../.gitbook/assets/WFMock.png" alt="" data-size="line"> button in Studio menu.
