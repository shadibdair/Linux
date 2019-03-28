# Question
## given the usrl:
## curl https://jsonplaceholder.typicode.com/posts

* print all the IDs of the user with id 10

# Answer
```
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://jsonplaceholder.typicode.com/posts | grep -A1 userId | grep -A1 10 | grep id
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 27520    0 27520    0     0  17439      0 --:--:--  0:00:01 --:--:-- 17439
    "id": 10,
    "id": 91,
    "id": 92,
    "id": 93,
    "id": 94,
    "id": 95,
    "id": 96,
    "id": 97,
    "id": 98,
    "id": 99,
    "id": 100,

```
* SAME
```
shadi@shadi-VirtualBox:~/Desktop/weekend$ curl https://jsonplaceholder.typicode.com/posts | grep -A1 userId | grep -A1 10 
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 27520    0 27520    0     0   209k      0 --:--:-- --:--:-- --:--:--  209k
    "id": 10,
--
--
    "userId": 10,
    "id": 91,
--
    "userId": 10,
    "id": 92,
--
    "userId": 10,
    "id": 93,
--
    "userId": 10,
    "id": 94,
--
    "userId": 10,
    "id": 95,
--
    "userId": 10,
    "id": 96,
--
    "userId": 10,
    "id": 97,
--
    "userId": 10,
    "id": 98,
--
    "userId": 10,
    "id": 99,
--
    "userId": 10,
    "id": 100,


```
