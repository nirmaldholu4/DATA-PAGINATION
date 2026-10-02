# 🎓 Student Progress Tracker

A clean and simple **Academic Performance Dashboard** built with **React** and **Bootstrap**. It fetches student data from a mock REST API (JSON Server) and shows it in a responsive table with custom pagination.


## 🎥 Demo Video

[▶️ Watch the pagination Project Demo Video](https://drive.google.com/file/d/1fQ6K3koglrCEzCBmpTL7Q1b4klYgCm5Y/view?usp=sharing)

---
## 🎥 Project Screenshot

![Project Screenshot](./src/assets/Screenshot/project-screenshot.png)

---

## ✨ Features

- 📋 Student marks table (ID, Name, DSA, Maths, DBMA, Networking)
- 📄 Custom pagination with Previous / Next buttons
- 🔢 Rows per page selector (5, 10, 25, 50, 100)
- 🌐 Data fetched from a REST API using `fetch` and `useEffect`
- 🎨 Modern teal-themed UI with gradient background, rounded card and ID badges
- 📱 Responsive layout using Bootstrap's grid and `table-responsive`

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| React | UI library (hooks: `useState`, `useEffect`) |
| Vite | Build tool / dev server |
| Bootstrap 5 | Layout and base table styling |
| Custom CSS | Theme, badges, pagination styling |
| JSON Server | Mock REST API (`db.json`) |

---

## 📁 Project Structure

```
student-progress-tracker/
├── public/
├── src/
│   ├── assets/
│   │   └── screenshot/
│   │       └── project-screenshot.png   # Project preview image
│   ├── App.jsx        # Main component (table + pagination logic)
│   ├── App.css        # Custom styling
│   └── main.jsx       # Entry point (Bootstrap imports + render)
├── db.json            # Mock database (100 students)
├── package.json
└── README.md
```

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd student-progress-tracker
```

### 2. Install dependencies

```bash
npm install
npm install bootstrap
npm install -g json-server
```

### 3. Start the JSON Server (API)

```bash
json-server --watch db.json --port 3000
```

The API will be available at: `http://localhost:3000/students`

### 4. Start the React app

Open a new terminal and run:

```bash
npm run dev
```

Then open the URL shown in the terminal (usually `http://localhost:5173`).

---

## 📊 Data Format

Each student in `db.json` looks like this:

```json
{
  "id": 1,
  "name": "Aarav Desai",
  "dsa": 65,
  "maths": 98,
  "dbma": 64,
  "networking": 89
}
```

---

## 🧠 How Pagination Works

```js
let lastIndex = currentData * perpageData;
let firstIndex = lastIndex - perpageData;
let currentStudents = allData.slice(firstIndex, lastIndex);
let totalData = Math.ceil(allData.length / perpageData);
```

- `currentData` → current page number
- `perpageData` → rows shown per page
- `slice()` picks only the students for the current page
- Previous / Next buttons are disabled on the first / last page

---

## 🔮 Future Improvements

- Search and filter students by name
- Sort columns (ascending / descending)
- Show total marks, percentage and grade
- Add, edit and delete students (full CRUD)
- Charts for subject-wise performance

---

## 👨‍💻 Author

**Dholu Nirmal.**

- GitHub: [@nirmaldholu4](https://github.com/nirmaldholu4)
- LinkedIn: [dholu-nirmal](https://www.linkedin.com/in/dholu-nirmal/)
- Email: nirmaldholu4@gmail.com

Made with ❤️ using React.

---

---

## 📜 License

📄 License 👉 This project is created for educational purposes only.👈

---
