# Python Backend
## Homework #1: Network Basics and Python Backend

### Task
Implement the "Mathematical API" from the example directly through the ASGI-compatible function. In particular 

- requests for which there are no handlers (wrong method, wrong path) should return error 404 Not Found
- the GET /factorial (n!)
  - request is returned to the request body in json format of the form {"result": 123}
  - the query parameter of the request should have the parameter n: int
  - if there is no parameter, or it is not a number - return 422 Unprocessable Entity
  - if the parameter is not a valid number (less than 0) - return 400 Bad
- Request GET /fibonacci request (the nth fibonacci number)
  - it is returned to the request body in json format of the form {"result": 123}
  - in the path parameter of the request (fibonacci/{n}) there must be a parameter n: int
  - if there is no parameter, or it is not a number - return 422 Unprocessable Entity
  - if the parameter is not a valid number (less than 0) - return 400 Bad
- Request the GET /mean request (the average of the array)
  - is returned to the request body in json format of the form {"result": 123}
  - in the request body there is not an empty array of floats (for example [1, 2.3, 3.6])
  - the body is not an array of floats - we return 422 Unprocessable Entity
  - if the array is empty - we return 400 Bad Request
 
### My resources 
- Mac on m1, 2020
- Monterey 12.6.7
- Python 3.10.11
  
### How to run
- Clone the repo
```
git clone https://github.com/Laitielly/python_backend_itmo.git
```
- Go to hw1 folder
```
cd python_backend_itmo/hw1
```
- Set the environment with requirements.txt
```
pip install -r requirements.txt
```
- Run an app on localhost with port 8000
```
uvicorn app:app --host 127.0.0.1 --port 8000
```
- Open new terminal window and run test
```
pytest test_homework_1.py 
```

After running the tests, I get the following result:
```
============================= test session starts ==============================
platform darwin -- Python 3.10.11, pytest-8.3.3, pluggy-1.5.0
rootdir: /Users/annasidorova/python_backend_itmo/hw1
plugins: anyio-4.4.0
collected 22 items                                                             

test_homework_1.py ......................                                [100%]

============================== 22 passed in 0.10s ==============================
```
