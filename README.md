# REAL WORLD TESTS


## Lifecycle of a test

### Two (2) methods to run at the beginning and end of each test method:
1. `setUp()` - can be used to create temporary files and folders or set up  
a database connection during tests
2. `tearDown()` - would be used to remove temporary files or folders or close a connection to a database
[These methods are defined using **camelCase** (or else, they won’t run at all)]

### Two (2) methods to run before and after of all tests run:
1. `setUpClass()`
2. `tearDownClass()`


## Mocking  
--> allows us to test functionality  that could fail due to factors beyond our control    
(We’ll create a new method which will make a request to a fictional external API to retrieve a student’s course schedule. We’ll then write a test to mock this request to make sure our method behaves as expected when the request is successful and when it fails.)
1. Import the `requests` module in our student.py file - so we can use it to make a request to our fictional API service.
2. We can now check if the request was successful using `response.ok` and return the response content itself using `response.text`.     
    (As we can’t control  whether an external API is available or not, it would be impossible for us to test both cases for our method. This is of course where mocking comes into play as it will allow us to mock the  request being both successful and unsuccessful.)
3. import a method from `unittest.mock` called “`patch`” in our test_student.py file.   
    * The patch method we’ve imported can be used as a decorator or a context manager. We’ll use a context manager for our test method.     
    * Note that we’re importing the `student class` at the top of the file and that’s why we use `student.requests.get` to access it.

