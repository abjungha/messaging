# messaging Api

This is an application with a need to build its own social network, "Friends Management" is a common requirement which usually starts off simple but can grow in complexity depending on the application's use case.
Usually, the application compraised of features like "Friend", "Unfriend", "Block", "Receive Updates" etc.

## Technology Choice

### Spring Boot
1. Spring Boot allows easy setup of standalone Spring-based applications. 
2. Ideal for spinning up microservices and easy to deploy. 
3. Makes data access less of a pain. 

## List of REST Endpoints and Explanation

1.  Establish Friendship between two persons
    * Path : `/createFriendConnection`
    * Input :
    ```
    {
		"friends":[
			"abc@gmail.com",
			"pqr@gmail.com"
		]
    }
    ```
    * Output :
    ```
    {
		"success": true
	}
	```

2. Returns a list of friends of a person.
   * Path : `/getFriendsList`
   * Input :
   ```
   {
		"email":"abc@example.com"
   }
   ```
   * Sample Output :
   ```
   {
		"success": true,
		"friends":[
			"pqr@gmail.com",
			"lmn@gmail.com",			
		],
		"count":2
	}
	```
	  

# Mock Database
Mock database is created in MockRepository.java with below data.

Friend 1: andy@example.com
	Friendlist: pqr@cap.com,
		    lmn@cap.com 	

Friend 2:  pqr@cap.com 
	Friendlist: abc@cap.com,
		    lmn@cap.com	 


# Testing

ControllerTest.java includes below test cases-
1. testFriendConnection
2. testGetFriendsList
