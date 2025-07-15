# Timestamp Microservice

A simple API microservice built with Node.js and Express. It converts date strings or Unix timestamps into a JSON object. The example homepage is styled with Tailwind CSS.

This project is a solution to the "Timestamp Microservice" challenge from [freeCodeCamp](https://www.freecodecamp.org/learn/back-end-development-and-apis/back-end-development-and-apis-projects/timestamp-microservice).

---

## ✨ Tech Stack

-   **Backend:** [Node.js](https://nodejs.org/), [Express.js](https://expressjs.com/)
-   **Language:** [JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
-   **Styling:** [Tailwind CSS](https://tailwindcss.com/)

---

## 🚀 How It Works

The microservice has one main endpoint that handles date conversions.

### Endpoint: `/api/:date?`

-   The `:date` parameter is optional.
-   If the `:date` parameter is a **valid date string** (e.g., `"2015-12-25"`), the API will return the Unix timestamp and the date in UTC format.
-   If the `:date` parameter is a **Unix timestamp** in milliseconds (e.g., `1451001600000`), the API will return the same timestamp and the corresponding date in UTC format.
-   If the `:date` parameter is **omitted**, the API will return the current date and time.

---

### 📝 Usage Example

-   **For a specific date:**
    `[PROJECT_URL]/api/2015-12-25`

-   **For a Unix timestamp:**
    `[PROJECT_URL]/api/1451001600000`

-   **For the current date:**
    `[PROJECT_URL]/api/`

---

### 📤 Output Example

-   **Successful Output:**

    ```json
    { "unix": 1451001600000, "utc": "Fri, 25 Dec 2015 00:00:00 GMT" }
    ```

-   **If the input date is invalid, the output will be:**
    ```json
    { "error": "Invalid Date" }
    ```

---

## 💻 Local Development

1.  **Clone the repository:**

    ```bash
    git clone <YOUR_REPOSITORY_URL>
    cd <REPOSITORY_NAME>
    ```

2.  **Install dependencies:**
    This will install both production (`express`, `cors`, etc.) and development (`tailwindcss`) dependencies.

    ```bash
    npm install
    ```

3.  **Run the development environment:**
    For an optimal development experience, you should run two commands in **separate terminals**:

    -   **Terminal 1: Start the Tailwind CSS watcher:**
        This command watches your template files (like `index.html`) for changes and automatically rebuilds the `public/style.css` file.

        ```bash
        npm run watch:css
        ```

    -   **Terminal 2: Start the Node.js server:**
        This starts the Express server with `--watch`, so it automatically restarts when you save changes to backend files (like `index.js`).
        ```bash
        npm run dev
        ```

    The server will then be running on `http://localhost:3000`.

---
