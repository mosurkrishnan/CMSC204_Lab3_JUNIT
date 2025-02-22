# CMSC204_Lab3_JUNIT
JUnit Test Classes

You will be creating a JUnit Test Class for Gradebook.java, that has been provided for you.  Upload Gradebook.java and GradeBookTest.java to the repository in GitHub you created in Lab 1 in a directory named JUnit_Lab.

Add the following two methods to the Gradebook class.  Do not modify the other methods of Gradebook.
1.	Add a getScoreSize() method to the Gradebook class which returns scoresSize;
2.	Add a toString() method to the Gradebook class that returns a string with each score in scores separated by a space.

Create the Test Class GradebookTester.
1.	Select the setUp and tearDown method.
2.	Select all of the methods of Gradebook, except for the constructor to create tests for.
3.	In the setUp method of GradebookTester, create at least two objects of Gradebook of size 5.  Call the addScore method for each of the Gradebook classes at least twice (but no more than 5 times).
4.	In the teardown method of GradebookTester, set the two objects of Gradebook to null;
5.	Create test for the methods of Gradebook:
a.	addScore
i.	Use the toString method to compare the contents of what is in the scores array vs. what is expected to be in the scores array
assertTrue( . . .)
ii.	Compare the scoreSize to the expected number of scores entered.
assertEquals(. . .)
b.	 sum
i.	Compare what is returned by sum() to the expected sum of the scores entered.
c.	 minimum
i.	Compare what is returned by minimum() to the expected minimum of the scores entered.
d.	 finalScore
i.	Compare what is returned by finalScore() to the expected finalscore of the scores entered.
The finalScore is the sum of the scores, with the lowest score dropped if there are at least two scores, or 0 if there are no scores.
Example:

Add a private member of GradeBookTest:
	GradeBook g1;

In setup:
g1 = new GradeBook(5);
g1.addScore(50);
g1.addScore(75);

In teardown:
	g1 = null;

in testSum():
assertEquals(125, g1.sum(), .0001);

in testMinimum():
	assertEquals(50, g1.minimum(), .001);

in addScoreTest();
	assertTrue(g1.toString().equals(“50.0 75.0 ”);

