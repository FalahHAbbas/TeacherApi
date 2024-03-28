### registration flow
#### 1. Register as a teacher

![img.png](img.png)


```angular2html
POST /api/v1/users
```

##### Request

```json
{
  "phone": "07801234567",
  "otpMethod": "SMS"
}
```
##### Response

```json
{
  "firstName": null,
  "lastName": null,
  "id": "5f1c88ff-0de7-4fb6-8e00-7355cfb83373",
  "username": null,
  "email": null,
  "phone": "07801234567",
  "roles": [],
  "token": null
}
```

#### 2. Verify phone number
![img_1.png](img_1.png)
```angular2html
POST /api/v1/users/otp/verify
```

##### Request

```json
{
  "phone": "07801234567",
  "otp": "123456"
}
```

##### Response

```json
{
  "firstName": null,
  "lastName": null,
  "id": "5f1c88ff-0de7-4fb6-8e00-7355cfb83373",
  "username": null,
  "email": null,
  "phone": "07801234567",
  "roles": [],
  "token": "eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzUxMiJ9.eyJpc3MiOiJzZWN1cmUtYXBpIiwiYXVkIjoic2VjdXJlLWFwcCIsInVzZXIiOnsiZmlyc3ROYW1lIjpudWxsLCJsYXN0TmFtZSI6bnVsbCwiaWQiOiI1ZjFjODhmZi0wZGU3LTRmYjYtOGUwMC03MzU1Y2ZiODMzNzMiLCJ1c2VybmFtZSI6bnVsbCwiZW1haWwiOm51bGwsInBob25lIjoic3RyaW5nMTIiLCJyb2xlcyI6W10sInRva2VuIjpudWxsfSwiZXhwIjoxNzE0MTY1MjAwLCJyb2wiOltdfQ.ijSeTKOycSWcvCogLC1Jjxq27fUmPse61o0UXgcQi5XayA96F3lCEwmGG8JMkTXRILxWSMXZQVqGlVsAb_QJqw"
}
```

#### 3. Create a teacher profile
![img_2.png](img_2.png)
![img_3.png](img_3.png)
![img_4.png](img_4.png)
![img_5.png](img_5.png)
![img_6.png](img_6.png)
![img_7.png](img_7.png)

```angular2html
POST /api/v1/teachers
```

##### Request

```json
{
  "firstName": "Falah",
  "lastName": "Abbas",
  "gender": "MALE",
  "birthdate": "1993-09-29",
  "governorate": "Baghdad",
  "schoolName": "Aschool",
  "educationalLevel": "Diploma",
  "schoolStages": [
    "PRIMARY_STAGE_5"
  ],
  "cv": "0121fc1a-206b-40f7-a188-6085107fbd9b.png",
  "photo": "ff21fc1a-2012-40f7-a188-6085107f1dad.png",
  "experienceYears": "OneToThree",
  "university": "University of Baghdad",
  "major": "Computer Science",
  "subjects": [
    "PRIMARY_ARABIC_LANGUAGE"
  ],
  "assistant": false
}
```

##### Response

```json
{
  "id": "fa2f2bfb-9c81-4e63-8d57-726c9d18d8d0",
  "firstName": "string",
  "lastName": "string",
  "birthdate": "2024-03-28",
  "phone": "aaa",
  "governorate": "Baghdad",
  "gender": "MALE",
  "schoolName": "string",
  "cv": "",
  "photo": "",
  "subjects": [
    "PRIMARY_ARABIC_LANGUAGE"
  ],
  "schoolStages": [
    "PRIMARY_STAGE_5"
  ]
}
``` 