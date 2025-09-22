# Code_Alpha Cybersecurity Internship Project
## Secure Coding Audit/Review

---

## 📌Task/Assignment Details
- Select a programming language and application to audit.
- Perform a code review to identify security vulnerabilities.
- Use tools like static analyzers or manual inspection methods.
- Provide recommendations and best practices for secure coding.
- Document findings and suggest remediation steps for safer code.

---

## 📌Proceedures
- Install virtual environment(venv) module in terminal
  ```
  pkg install python-venv
  ```
- Create and activate virtual environment (this is necessary to segment the program dependencies from the generally installed python dependencies)
  ```
  python -m venv .venv
  source .venv/bin/activate
  ```
- Install dependencies used in the program to be audited
   ```
   pip install -r requirements.txt
   # make sure the project dependecies are in a requirements.txt file
   ```
  
- Install audit tools
  ```
  pip install pip-audit safety bandit
  ```
- First run dependency audit
  ```
  safety check -r requirements.txt
  ```
- Run static code analysis
  ```
  bandit -r
  ```
- Save results (for report) in a readable format preferrably .json format
  ```
  pip-audit -r requirements.txt -f json -o audit-report.json
  safety check -r requirements.txt --json > safety-report.json
  bandit -r . -f json -o bandit-report.json
  ```
  
