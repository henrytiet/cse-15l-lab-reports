# Week 3 Lab Report
## Part 1
### String Server Code
![Screenshot 2023-01-30 160603](https://user-images.githubusercontent.com/97487846/215624807-70e16cec-95b9-4e0c-b4a0-ff2cc4ac2d2b.png)


### Testing
![Screenshot 2023-01-30 155614](https://user-images.githubusercontent.com/97487846/215624009-14a92d07-1716-481f-a440-da6c91624a60.png)
Methods Called
- handleRequest
- println
- getQuery
- split
- equals
- format


Arguments Passed
-  URI url
- "Path: " + <path>
- split
- "="
- "s"
- "%s", listOut
  
Values that have changed from this request
- the url changed, with a new path that includes /add-message?s=hello
- the path passed as parameters[1] is also different
- listOut also updates with a new history output


![Screenshot 2023-01-30 155647](https://user-images.githubusercontent.com/97487846/215624831-234880eb-a985-45a2-97ba-99fc75e346d2.png)
Methods Called
- handleRequest
- println
- getQuery
- split
- equals
- format

Arguments Passed
-  URI url
- "Path: " + <path>
- split
- "="
- "s"
- "%s", listOut
  
Values that have changed from this request
- the url changed, with a new path that includes /add-message?s=hello
- the path passed as parameters[1] is also different
- listOut also updates with a new history output
  
## Part 2
  
### Failure Inducing Input
```
int[] input2={1, 2, 3};
ArrayExamples.reverseInPlace(input2);
assertArrayEquals(new int[]{3, 2, 1}, input2);
```
	
### Non Failing Input
```
int[] input1 = { 3 };
ArrayExamples.reverseInPlace(input1);
assertArrayEquals(new int[]{ 3 }, input1);
```

### Symptoms From Inputs
![symptom](https://user-images.githubusercontent.com/97487846/215632492-1062ae17-df8d-41bf-b996-2b2c49a9bf0d.png)

### Bug Before
```
  static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }
```
																	
### Bug After
```
static void reverseInPlace(int[] arr) {
    int[] tempArray= new int[arr.length];
    for(int i=0; i<tempArray.length; i++) {
      tempArray[i]=arr[i];
    }
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = tempArray[tempArray.length - i - 1];
    }
  }
```
The issue was that the method would overwrite itself when reversing. When the iterator reaches the middle of the array, it starts to mirror the new first half, and the original first half is nowhere to be found.
																	

## Part 3
In week 2, I learned how to run local servers. It felt really cool to be able to create something that I could see outside of the terminal outputs. Although Server.java was provided, I got to understand more about how URL's are passed and interpreted by the server.
