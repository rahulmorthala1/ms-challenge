# ms3-challenge-api
This is to create a range for the two input parameters submitted and replace values mentioned in te problem statement

 # Problem Statement:

A client has requested a web application that calls an API-enabled backend utilizing an algorithm.  The backend algorithm takes in 2 integers representing a range, and converts each number in the range. Multiples of 7 convert to “MS3”, multiples of 3 convert to “ME”, and multiples of both 7 and 3 convert to “MS3 and ME”.  The algorithm should be created in the most optimized way possible. The input range has a limit from a minimum of 1 to a maximum of 200. Ideally, users should be able to query inputs HTTP API calls.  Responses should be in the form of JSON,


# Software requirements to run the code.
  1) MuleSoft anypoint studio 3.9 runtime
  2) postman client to test the api
  
# Special Instructions:
  
After you export the project into Anypoint studio. open ms3-challenge-api.xml. Right click and run the project. Deployment should be successful.

Enter the below uri into postman

localhost:8081/api/ms3-challange

method allowed: GET

Click on params button in postman add two keys/query parameters int1 and int2. please enter integer values for int1 and int2.

After entering the query params URI should look like eg: localhost:8081/api/ms3-challange?int1=1&int2=10

# Unit test: 

numbers divisible by 3 should be coverted to ME. numbers divisible by 7 should be coverted to MS3. numbers divisible by 3 and 7 should be coverted to MS3 and ME.

Case 1) localhost:8081/api/ms3-challange?int1=1&int2=10

request parameters

int1 = 1
int2 = 10

reponse example: 

[
    "1 : 1",
    "2 : 2",
    "3 : ME",
    "4 : 4",
    "5 : 5",
    "6 : ME",
    "7 : MS3",
    "8 : 8",
    "9 : ME",
    "10 : 10"
]

Case 2) localhost:8081/api/ms3-challange?int1=200&int2=180

request parameters

int1 = 200
int2 = 180

response:

[
    "180 : ME",
    "181 : 181",
    "182 : MS3",
    "183 : ME",
    "184 : 184",
    "185 : 185",
    "186 : ME",
    "187 : 187",
    "188 : 188",
    "189 : MS3 and ME",
    "190 : 190",
    "191 : 191",
    "192 : ME",
    "193 : 193",
    "194 : 194",
    "195 : ME",
    "196 : MS3",
    "197 : 197",
    "198 : ME",
    "199 : 199",
    "200 : 200"
]


Case 3) localhost:8081/api/ms3-challange?int1=190&int2=210

request parameters

int1 = 200
int2 = 210

{
	"message" : "Array out of range. Please Enter any number from 1 to 200"
}

In the problem statement range limit is from 1 to 200

# Error scenario

Case 4) localhost:8081/api/ms3-challange?int1=200

only one input parameter is entered 

int1 = 200

{
    "message": "Bad request. Please check the query paramters you entered or Enter two input query parameters."
}







