// app.js
require("dotenv").config();
const express = require("express");
const bodyParser = require("body-parser");
const cors = require("cors");
const db = require("./db");

const app = express();

app.use(bodyParser.json());
app.use(cors());
app.use(express.static("public")); // serve HTML files

// --------------------- Register User ---------------------
app.post("/register", (req, res) => {
    const { name, email, password, phone } = req.body;

    const sql = "INSERT INTO users (name, email, password, phone) VALUES (?, ?, ?, ?)";
    db.query(sql, [name, email, password, phone], (err, result) => {
        if (err) return res.json({ status: "error", error: err });
        res.json({ status: "success", message: "User registered" });
    });
});

// --------------------- Login ---------------------
app.post("/login", (req, res) => {
    console.log('log1', req.body)
    const { email, password } = req.body;

    const sql = "SELECT * FROM users WHERE email = ? AND password = ?";
    db.query(sql, [email, password], (err, results) => {
        console.log('log1', results )
        if (err) return res.json({ status: "error", error: err });

        if (results.length > 0) {
            res.json({ status: "success", user: results[0] });
        } else {
            res.json({ status: "failed", message: "Invalid credentials" });
        }
    });
});

// --------------------- Add Complaint ---------------------
app.post("/complaint", (req, res) => {
    const { student_id, title, description } = req.body;

    const sql = "INSERT INTO complaints (student_id, title, description, status) VALUES (?, ?, ?, 'Open')";
    db.query(sql, [student_id, title, description], (err, result) => {
        if (err) return res.json({ status: "error", error: err });
        res.json({ status: "success", message: "Complaint submitted" });
    });
});

// --------------------- Get Complaints for a User ---------------------
app.get("/complaints/:id", (req, res) => {
    const id = req.params.id;

    const sql = "SELECT * FROM complaints WHERE student_id = ?";
    db.query(sql, [id], (err, results) => {
        if (err) return res.json({ status: "error", error: err });
        res.json(results);
    });
});

// --------------------- Start Server ---------------------
const PORT = process.env.PORT;
app.listen(PORT, () => {
    console.log(`🚀 Server running on port ${PORT}`);
});
