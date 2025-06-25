# 🛠️ GitHub Actions Pipeline

This project demonstrates a basic GitHub Actions workflow that sets up a **Node.js environment** and prints a simple message.

---

## 📁 Folder Structure

```plaintext
github-actions-pipeline/
└── .github/
    └── workflows/
        └── node-greet.yml
```

---

## ⚙️ What It Does

- Triggers on **push** to the `main` branch
- Sets up **Node.js** using `actions/setup-node`
- Prints:

```
Hello from @23241a6749
```

---

## 🧪 Workflow Steps

```yaml
name: Node.js Greeting

on:
  push:
    branches:
      - main

jobs:
  greet:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Set up Node.js
        uses: actions/setup-node@v4
        with:
          node-version: '18'

      - name: Say Hello
        run: echo "Hello from @23241a6749"
```

---

## 🧠 How I Built It

- Created the `.github/workflows/` folder manually (Windows doesn’t support `mkdir -p` or `touch`)
- Added a YAML workflow file
- Used GitHub-provided actions to:
  - Checkout code
  - Set up Node.js
  - Print a message in the logs
- Committed and pushed the changes to trigger the workflow

---

## ✅ Example Output

Viewable under the **Actions tab** in your GitHub repo:

```
Hello from @23241a6749
```

---

## ⚠️ Notes

- This is a minimal CI pipeline useful for learning GitHub Actions
- You can change the Node.js version if needed
- Workflow names and triggers can be easily customized

---

## 🙋 Author

**GitHub:** [23241a6749](https://github.com/23241a6749)

---

## 📝 License

Free to use for educational or demo purposes.
