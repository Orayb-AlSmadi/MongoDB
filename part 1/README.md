## MongoDB Exercises
### Instructions 
1. Download Robo 3t and setup it on your machine.
2. Create a new connection
3. Create a new collection (students)
4. Right click on the collection.
5. Select 'insert Document'.
6. Enter image description here
7. Paste your json data
8. Click validate.
9. Click save.
10. Excute your queries on the query bar.
11. Test your queries using robo 3t


1. Insert yourself as a new  student. Example:
`{"fname" : "Ahmad","lname":"Omar","class":"A","age" :25}`

2.  Insert the following students.

`{"fname" : "Ahmad","lname":"Omar","class":"A","age" :25,"technologies":["PHP","mySql"]}`
`{"fname" : "Ammar","lname":"Saad","class":"B","age" :23,"technologies":["PHP","MongoDB"]}`
`{"fname" : "Steve","lname":"Rayan","class":"C","age" :18,"technologies":["C#","mySql"]}`
`{"fname" : "Jhon","lname":"williams","class":"A","age" :30, "technologies":["Python","MongoDB"]}`

3.  Write a MongoDB query to update the data of all students by incrementing their ages one year..
<!-- db.students.updateMany({}, {$inc:{age:1}})  -->

4. Write a MongoDB query to update all the student who has (ADAM) name and make thier classs `A` and thier technolgies `['PHP','mySql']`.
<!-- 
db.students.insertMany([
  {
    "fname": "Ala",
    "lname": "Mohammad",
    "class": "A",
    "age": 35,
    "technologies": [
      "PHP",
      "mySql"
    ]
  },
  {
    "fname": "Adam",
    "lname": "Graham",
    "class": "B",
    "age": 16,
    "technologies": [
      "javascrpt",
      "MongoDB"
    ]
  },
  {
    "fname": "Eva",
    "lname": "Mullins",
    "class": "B",
    "age": 20,
    "technologies": [
      "Python",
      "mySql"
    ]
  },
  {
    "fname": "Willie'",
    "lname": "Williamson",
    "class": "C",
    "age": 26,
    "technologies": [
      "C#",
      "Sql"
    ]
  },
  {
    "fname": "Bella",
    "lname": "Weaver",
    "class": "A",
    "age": 18,
    "technologies": [
      "VB",
      "Sql"
    ]
  },
  {
    "fname": "Nicolas",
    "lname": "Shelton",
    "class": "B",
    "age": 21,
    "technologies": [
      "PHP",
      "mariaDB"
    ]
  },
  {
    "fname": "Yasmin",
    "lname": "Rogers",
    "class": "A",
    "age": 16,
    "technologies": [
      "Javascript",
      "MongoDB"
    ]
  },
  {
    "fname": "Adele",
    "lname": "Drew",
    "class": "B",
    "age": 24,
    "technologies": [
      "PHP",
      "mySql"
    ]
  },
  {
    "fname": "Lillie",
    "lname": "Bird",
    "class": "A",
    "age": 30,
    "technologies": [
      "Ruby",
      "mySql"
    ]
  },
  {
    "fname": "Sue",
    "lname": "Mccoy",
    "class": "A",
    "age": 29,
    "technologies": [
      "GO",
      "mySql"
    ]
  },
  {
    "fname": "Amir",
    "lname": "Richards",
    "class": "B",
    "age": 28,
    "technologies": [
      "C#",
      "Oracle"
    ]
  },
  {
    "fname": "Umar",
    "lname": "Mccarthy",
    "class": "C",
    "age": 25,
    "technologies": [
      "Java",
      "mySql"
    ]
  },
  {
    "fname": "Ismail",
    "lname": "Ryan",
    "class": "A",
    "age": 36,
    "technologies": [
      "PHP",
      "mySql"
    ]
  }
])
db.getCollection('students').updateMany({"fname": "Adam"},{$set:{class: "A", technolgies: ['PHP','mySql']}})   -->

5. Write a MongoDB query to delete one student from class `A` .
<!-- db.getCollection('students').deleteOne({class: "A"})   -->
6.  Write a MongoDB query to delete All the students from class `C`.
<!-- db.getCollection('students').deleteMany({class: "C"})   -->
7. Write a MongoDB query to display all the students that thier age less than 20.
<!-- db.getCollection('students').find({age: {$lt:20}}) -->
8. Write a MongoDB query to display all the students that thier age greater than 30.
<!-- db.getCollection('students').find({age: {$gt:20}}) -->
9. Write a MongoDB query to get only the students of class `B`.
<!-- db.getCollection('students').find({class:"B"}) -->
10.  Sort the faculty details by their age (descending order) and get the details of the first five faculty members only. .
<!-- db.getCollection('students').find().sort({age:-1}) -->
