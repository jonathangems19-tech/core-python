# 🐍 Python Fundamentals

![Python](https://img.shields.io/badge/Python-3.10+-3572A5?style=flat&logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow?style=flat)
![Phase](https://img.shields.io/badge/Phase-1%20of%204-blue?style=flat)

> Part of my public AI/ML learning journey. This repo covers core Python from scratch — structured so that exercises show raw learning and `src/` contains clean, reusable code.

---

## 📁 Structure

```
python-fundamentals/
├── src/                        # Reusable, importable modules
│   ├── utils.py
│   └── helpers.py
├── exercises/                  # Topic-by-topic learning code
│   ├── variables_datatypes.py
│   ├── loops_conditions.py
│   ├── functions_lambdas.py
│   ├── oop_classes.py
│   ├── decorators_generators.py
│   ├── file_handling.py
│   ├── error_handling.py
│   └── regex_patterns.py
├── mini_projects/
│   ├── cli-calculator/
│   ├── student-grade-manager/  ← polished: CLI args + CSV + logging + tests
│   └── number-guessing-game/
├── tests/
│   ├── test_utils.py
│   └── test_grade_manager.py
├── scripts/
│   └── run_all_exercises.py
├── requirements.txt
└── README.md
```

---

## 📚 Topics Covered

| Topic | File | Status |
|---|---|---|
| Variables & Data Types | `exercises/variables_datatypes.py` | ✅ Done |
| Loops & Conditions | `exercises/loops_conditions.py` | ✅ Done |
| Functions & Lambdas | `exercises/functions_lambdas.py` | ✅ Done |
| OOP & Classes | `exercises/oop_classes.py` | ✅ Done |
| Decorators & Generators | `exercises/decorators_generators.py` | ✅ Done |
| File Handling | `exercises/file_handling.py` | ✅ Done |
| Error Handling | `exercises/error_handling.py` | ✅ Done |
| Regex | `exercises/regex_patterns.py` | ✅ Done |

---

## 🛠️ Mini Projects

### 1. CLI Calculator
A command-line calculator supporting basic arithmetic operations.

**Run:**
```bash
python mini_projects/cli-calculator/calculator.py
```

**Features:** addition, subtraction, multiplication, division, modulus, power

---

### 2. Student Grade Manager ⭐
The most polished project in this repo — built to practice real-world Python patterns.

**Run:**
```bash
python mini_projects/student-grade-manager/main.py --add "Alice" 88 92 76
python mini_projects/student-grade-manager/main.py --report
python mini_projects/student-grade-manager/main.py --export grades_output.csv
```

**Features:**
- Add/update/delete students via CLI arguments (`argparse`)
- Import and export data as CSV
- Logging with timestamps to `app.log`
- Grades summary: average, highest, lowest, letter grade
- Input validation with descriptive error messages

**Sample output:**
```
Name     Avg    Grade  Status
-------- ------ ------ -------
Alice    85.3   B      Pass
Bob      91.0   A      Pass
Charlie  54.2   F      Fail
```

---

### 3. Number Guessing Game
Terminal-based guessing game with difficulty levels and score tracking.

**Run:**
```bash
python mini_projects/number-guessing-game/game.py
```

---

## ⚙️ Setup

```bash
git clone https://github.com/your-username/python-fundamentals.git
cd python-fundamentals
pip install -r requirements.txt
```

---

## 🧪 Running Tests

```bash
pytest tests/
```

```
tests/test_utils.py          ..    PASSED
tests/test_grade_manager.py  ..... PASSED
```

---

## 💡 Key Concepts — Quick Reference

**Decorators**
```python
def timer(func):
    import time
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        print(f"{func.__name__} took {time.time() - start:.4f}s")
        return result
    return wrapper
```

**Generators**
```python
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        yield a
        a, b = b, a + b
```

**OOP — Dunder Methods**
```python
class Student:
    def __init__(self, name, grades):
        self.name = name
        self.grades = grades

    def __repr__(self):
        return f"Student({self.name}, avg={sum(self.grades)/len(self.grades):.1f})"

    def __lt__(self, other):
        return self.average() < other.average()
```

---

## 🔗 Part of My Learning Path

| Phase | Repo | Status |
|---|---|---|
| **1** | `python-fundamentals` ← you are here | 🟡 In Progress |
| 1 | `math-for-ml` | ⬜ Upcoming |
| 1 | `dsa-python` | ⬜ Upcoming |
| 2 | `numpy-practice`, `pandas-practice`, `eda-projects` | ⬜ Upcoming |
| 3 | `ml-algorithms-from-scratch`, `ml-projects`, `generative-ai` | ⬜ Upcoming |
| 4 | `mlops-toolkit`, `model-deployment` | ⬜ Upcoming |

Full roadmap → [`ml-portfolio`](https://github.com/your-username/ml-portfolio)

---

## 📈 Progress Log

| Date | Milestone |
|---|---|
| Week 1 | variables, loops, functions |
| Week 2 | OOP, decorators, generators |
| Week 3 | file handling, error handling, regex |
| Week 4 | mini projects + tests |

---

*Learning in public. Commits reflect real progress — each one adds a function, a test, or a working feature.*
