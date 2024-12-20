# Back End Development and APIs - Learning Journey 🌐

Welcome to my **FreeCodeCamp Back End Development and APIs** course repository! This repository documents my progress, challenges, and solutions as I complete the course. 🚀

---

## 🗂️ File Structure

```plaintext
.
├── .env                      # Environment variables file
├── package.json              # Dependencies and scripts
├── server.js / myApp.js      # Main application file
├── models/
│   └── Person.js             # Mongoose schema and model for Person
├── tests/
│   └── test.js               # Automated tests for FCC challenges
├── README.md                 # This file, detailing the course journey
```

---

## 📚 Course Overview

The **Back End Development and APIs** certification covers the fundamentals of creating and managing backend services and APIs using Node.js, Express, and MongoDB.

---

## ✅ Progress Checklist

### **1. MongoDB and Mongoose**
- [x] Install and Set Up Mongoose
- [x] Create a Model
- [x] Create and Save a Record of a Model
- [x] Create Many Records with `Model.create()`
- [ ] Find Records by `name` with `Model.find()`
- [ ] Perform Classic Updates by Running Find, Edit, and Save
- [ ] Delete Many Records with `Model.remove()`
- [ ] Chain Search Query Helpers

---

## 🚀 Challenges and Solutions

Each challenge is implemented in the `server.js` file. Below are highlights of the key challenges and how I approached them:

### **Challenge: Install and Set Up Mongoose**
- **Task:** Connect to MongoDB Atlas using Mongoose.
- **Solution:**
  ```javascript
  require('dotenv').config();
  const mongoose = require('mongoose');

  mongoose.connect(process.env.MONGO_URI, {
    useNewUrlParser: true,
    useUnifiedTopology: true,
  })
  .then(() => console.log('Connected to MongoDB'))
  .catch((err) => console.error('Connection error:', err));
  ```

---

### **Challenge: Create Many Records with `Model.create()`**
- **Task:** Create multiple records in the database.
- **Solution:**
  ```javascript
  const createManyPeople = (arrayOfPeople, done) => {
    Person.create(arrayOfPeople, (err, data) => {
      if (err) return done(err);
      done(null, data);
    });
  };
  ```

---

## 🛠️ How to Run the Project

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file:
   ```plaintext
   MONGO_URI=<your-mongo-atlas-uri>
   ```

4. Start the server:
   ```bash
   node server.js
   ```

---

## 🌟 Key Learnings
- Fundamentals of CRUD operations with MongoDB and Mongoose.
- Building and testing APIs using Node.js and Express.
- Error handling and debugging backend applications.

---

## 🔗 Resources
- [FreeCodeCamp Course](https://www.freecodecamp.org/learn/back-end-development-and-apis)
- [Mongoose Documentation](https://mongoosejs.com/docs/guide.html)
- [Node.js Documentation](https://nodejs.org/en/docs/)

---

## 🎯 Next Steps
- Complete remaining challenges in the course.
- Build a full-fledged API using these concepts.
- Deploy the API on a cloud service.

---

Happy coding! 😊
```

### How to Use This `README.md`
1. Replace `<repository-url>` with your actual GitHub repository URL.
2. Replace `<repository-folder>` with your local project folder name.
3. Update progress checkboxes (`[x]`) as you complete the challenges.

This template ensures clear documentation of your journey and makes it easy for others to navigate your code. Let me know if you need help refining it further! 🚀
