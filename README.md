# Flask CI/CD with Jenkins

## 📋 Overview
This project demonstrates a complete CI/CD pipeline using Jenkins for a Python Flask application.

## 🧱 Pipeline Stages
1. **Build:**  
   - Creates a virtual environment  
   - Installs dependencies from `requirements.txt`
2. **Test:**  
   - Runs unit tests using `pytest`
3. **Deploy:**  
   - Placeholder stage for staging deployment (customizable)
4. **Notifications:**  
   - Sends email notifications on build success or failure

## ⚙️ Jenkins Setup
- Installed Jenkins on Ubuntu
- Installed Python3 and pip
- Installed required plugins: *Pipeline*, *Git*, *Email Extension*

## 📨 Email Notification
Configured SMTP via Gmail (or wrapped mail step with try/catch if no SMTP server).

## 🚀 Trigger
- Build is triggered automatically on push to `main` branch via GitHub webhook.

## 🧪 Test
Sample test file: `tests/test_app.py`

```python
def test_addition():
    assert 1 + 1 == 2



---

## ✅ Step 4: Take Screenshots for Submission

📸 Take the following screenshots:
1. Jenkins pipeline view with **green stages**  
2. Console output showing build → test → deploy → mail  
3. GitHub repo showing `Jenkinsfile`  
4. Email (if configured)

---

## ✅ Step 5: Submit

Per instructions:
- Add your GitHub repo URL in a `.txt` or `.pdf` file
- Upload via **Vlearn**

---

## 🚀 Next Task (GitHub Actions)

Once Jenkins is done, your next task is **GitHub Actions CI/CD**.  
We can create `.github/workflows/ci.yml` with the same Build → Test → Deploy steps.

Would you like me to generate that **GitHub Actions workflow** now so you can complete both tasks together?
