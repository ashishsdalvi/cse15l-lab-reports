# Welcome to Blog Post 2: Servers and Bugs

[Blogs](https://ashishsdalvi.github.io/cse15l-lab-reports/testing)


## Part 1: StringServer

To create StringServer, I used the code in the screenshot below.
![StringServer Code](https://ashishsdalvi.github.io/cse15l-lab-reports/StringServerCode.png)

The goal of StringServer was to create a webserver where you could pass in strings during a request.
This would be done by passing in a string as a parameter when the query was s.

Here is a screenshot of when the parameter passed was 'dog'.
![StringServer Code](https://ashishsdalvi.github.io/cse15l-lab-reports/StringServer_dog.png)

In this screenshot, the methods getPath and equals methods were called to check if the url was valid.
I also used the getQuery and split methods to store the queries of a url.
For each request, I store the second parameter of the query in an ArrayList called stringList.
In this instance, dog was the parameter added to stringList.
Thus, each request changes what is stored in stringList.
Additionally, since each time the request parameters are different, the URI should change as well.



Here is a screenshot of when the parameter passed was 'god'.
![StringServer Code](https://ashishsdalvi.github.io/cse15l-lab-reports/StringServer_dog_god.png)

In this screenshot, the methods getPath and equals methods were called again to check if the url was valid.
I also used the getQuery and split methods again to store the queries of a url.

In this instance, dog was the parameter added to stringList (the ArrayList described in the previous screenshot).
Thus, the variable stringList was changed (it now contains dog and god).
Additionally, since each time the request parameters are different, the URI should change as well.


## Part 2: Fixing Bugs

Here is the method we are testing.
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[tempArr.length - i - 1]; 
    }
  }
``` 

Here is a failure inducing input in the form of a JUnit test.
```
@Test 
public void testReverseInPlace2() {
    int[] input1 = { 3, 4, 5, 6 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 6, 5, 4, 3 }, input1);
}
```

Here is an input that passes that test as a JUnit test.
```
@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}
```

Here is a screenshot of running JUnit with the following two tests.
![JUnit Testing](https://ashishsdalvi.github.io/cse15l-lab-reports/JUnit_reverseInPlaceTest.png)


As you can see, there was one failure in the JUnit output and five passing tests. The one
failure is indicated to be testReverseInPlace2 while testReverseInPlace passes (no failure).

The code below is the incorrect:
```
static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1]; 
    }
  }
```

The code below is the fixed version:
```
static void reverseInPlace(int[] arr) {
    int[] tempArr = arr.clone(); 
    for(int i = 0; i < arr.length / 2; i += 1) {
      arr[i] = tempArr[tempArr.length - i - 1];
      arr[tempArr.length - i - 1] = tempArr[i]; 
    }
  }
```

The reason why the fixed version fixes the incorrect input
is because it creates a temporary array to store all the values.
Then it sets each of the values at each index of the array to the value
of the other side.

In the broken version of the code, the later indices would take the values
of the indices in the same array (which were already switched), hence creating
the issue. So for our failure inducing input, index 2 in the array
would take the value of index 1 of the same array (whose value was 5) meaning
both indices 1 and 2 would have the value of 5. The input {3, 4, 5, 6}
was therefore {6, 5, 5, 6}. 


## Part 3
In this lab, I learned a framework for how to design tests in JUnit. I think
 the idea of trying simple inputs that increase in size and input type (strings,
 lists, etc) was useful.
