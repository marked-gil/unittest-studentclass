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
