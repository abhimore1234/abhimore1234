
# 👋 Hi, I'm Abhishek More 

**Data Science & Full Stack Developer**<br><br>
🌐 Explore My Portfolio : [abhimore.netlify.app](https://abhimore.netlify.app/) <br>
A living canvas of my projects, capabilities, and innovations.

---



## 👨‍💻 About Me

I specialize in turning complex data into actionable insights. With a strong foundation in data analysis, machine learning, and statistical modeling, I help organizations unlock valuable patterns and drive informed decisions.

- **Core Skills:** Data analysis, machine learning, statistical modeling
- **Technologies:** Python, R, SQL, Apache Spark, Hadoop
- **Specializations:** Predictive analytics, deep learning, scalable data pipelines
- **Interests:** AI-driven solutions for business optimization and fraud detection
- **Continuous Learning:** Cloud-based AI, MLOps, efficient model deployment


---

## 🚀 What I Do

- Always curious, always learning—exploring the endless possibilities in data science and full stack development.
- Experiment with new tools, frameworks, and approaches to keep my skills sharp.
- Enjoy breaking down complex topics into easy-to-understand concepts.
- Believe in the power of data to make a positive impact, one project at a time.

---

## 🌱 Motto

> “Data doesn’t lie, but interpretation is everything.”

> “Continuous learning is the key to growth.”

---

## 📫 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhishek-more-363bb62b8)

---

_Simplicity is the ultimate sophistication._

## 👨‍💻 About Me

I specialize in turning complex data into actionable insights. With a strong foundation in data analysis, machine learning, and statistical modeling, I help organizations unlock valuable patterns and drive informed decisions.

- **Core Skills:** Data analysis, machine learning, statistical modeling
- **Technologies:** Python, R, SQL, Apache Spark, Hadoop
- **Specializations:** Predictive analytics, deep learning, scalable data pipelines
- **Interests:** AI-driven solutions for business optimization and fraud detection
- **Continuous Learning:** Cloud-based AI, MLOps, efficient model deployment

---

## 🚀 What I Do

- Always curious, always learning—exploring the endless possibilities in data science and full stack development.
- Experiment with new tools, frameworks, and approaches to keep my skills sharp.
- Enjoy breaking down complex topics into easy-to-understand concepts.
- Believe in the power of data to make a positive impact, one project at a time.

---

## 🌱 Motto

> “Data doesn’t lie, but interpretation is everything.”

> “Continuous learning is the key to growth.”

---

## 📫 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhishek-more-363bb62b8)

---

_Simplicity is the ultimate sophistication._ 


🧱 Step 1: Setup MongoDB Environment
✅ Requirements
- MongoDB installed locally or use MongoDB Atlas (cloud)
- MongoDB shell (mongosh) or GUI like MongoDB Compass
- A database and collection to work with

  
🏗️ Create a Database and Collection
use universityDB; // switch to or create database
db.createCollection("students"); // create collection



📝 Step 2: Create Documents (Insert)

🔹 insertOne() and insertMany()
// Insert one student
db.students.insertOne({
  name: "Abhishek",
  age: 22,
  skills: ["Python", "MongoDB", "Flask"]
});

// Insert multiple students
db.students.insertMany([
  { name: "Ravi", age: 23 },
  { name: "Sneha", age: 21 }
]);
🔹 save() Method (Legacy but useful)

// Save inserts if _id is new, updates if _id exists
db.students.save({
  _id: ObjectId("652f1a2b3c4d5e6f7g8h9i0j"),
  name: "Abhishek More",
  age: 23,
  skills: ["Python", "Flask", "MongoDB"]
});



🔍 Step 3: Read Documents (Query)
🔹 Basic Find
db.students.find(); // all documents
db.students.find({ age: { $gt: 21 } }); // age > 21

 Logical Operators
// AND
db.students.find({
  $and: [{ age: { $gt: 20 } }, { skills: "MongoDB" }]
});

// OR
db.students.find({
  $or: [{ age: { $lt: 22 } }, { name: "Sneha" }]
});

// NOT
db.students.find({
  age: { $not: { $gt: 25 } }
});



✏️ Step 4: Update Documents
🔹 updateOne() and updateMany()
// Update one
db.students.updateOne(
  { name: "Ravi" },
  { $set: { age: 24 } }
);

// Update many
db.students.updateMany(
  { age: { $lt: 22 } },
  { $set: { status: "junior" } }
);


🗑️ Step 5: Delete Documents
🔹 deleteOne() and deleteMany()
db.students.deleteOne({ name: "Sneha" }); // delete one
db.students.deleteMany({ age: { $lt: 22 } }); // delete many



🧠 Step 6: Use save() for Upsert Logic
🔹 Save = Insert or Update
db.students.save({
  _id: ObjectId("652f1a2b3c4d5e6f7g8h9i0j"),
  name: "Abhishek More",
  age: 24,
  skills: ["Python", "MongoDB", "Flask", "JavaScript"]
});











