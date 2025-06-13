# 🧪 Postman Collection Runner with GitHub Actions

This repository automatically runs a [Postman](https://www.postman.com/) collection every night using **GitHub Actions**, generates a beautiful HTML report using [`htmlextra`](https://www.npmjs.com/package/newman-reporter-htmlextra), and publishes it via **GitHub Pages**.

---

## 🔄 What it does

- Runs the Postman collection daily at 03:00 AM UTC.
- Fetches the collection from a **Postman API URL**.
- Generates a detailed test report in HTML format.
- Publishes the report to GitHub Pages for public access.

---

## 🖥️ Live Report

👉 [View Latest Report](https://MonicaPerdomoSantana.github.io/trello-api-automation/report.html)

---

## 🚀 How to set it up

1. **Fork or clone** this repo.
2. **Add your `POSTMAN_API_KEY`** as a secret in GitHub:
   - Go to **Settings > Secrets and variables > Actions**
   - Create a new secret:
     ```
     Name: POSTMAN_API_KEY
     Value: your_postman_key
     ```
3. Edit `.github/workflows/postman-report.yml` and replace the collection URL:
   ```yaml
   https://api.postman.com/collections/YOUR_COLLECTION_ID
   ```
4. **Enable GitHub Pages**:
   - Go to **Settings > Pages**
   - Choose `GitHub Actions` as source

---

## 🛠 Tech Stack

- **Newman** – CLI runner for Postman
- **htmlextra** – Custom HTML reporter
- **GitHub Actions** – For automation
- **GitHub Pages** – To host the report

---

## 📅 Cron Schedule

This job runs every day at **03:00 UTC**:

```yaml
on:
  schedule:
    - cron: "0 3 * * *"
```

You can adjust this in `.github/workflows/postman-report.yml`.

---

## 👩‍💻 Author

Made with ❤️ by **Mónica Perdomo Santana**  
[GitHub](https://github.com/MonicaPerdomoSantana) · [Portfolio](https://mps-portfolio.netlify.com)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
