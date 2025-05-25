````markdown
# 📆 Date Conversion Program

This JavaScript program retrieves the current date and time, logs it, and provides functions to convert the date into two human-readable formats:

- **MM/DD/YYYY** (e.g., `9/27/2024`)
- **Month Day, Year** (e.g., `September 27, 2024`)

## ✅ Features

- Get the current system date and time.
- Format and display the date in:
  - Short format: MM/DD/YYYY
  - Long format: Month Day, Year
- Console logs the current date string.
- Locale-specific formatting using `en-US`.

---

## 🧩 User Stories Implemented

1. Create a `currentDate` variable with the current date and time.
2. Create a `currentDateFormat` string:  
   `Current Date and Time: <full date string>`.
3. Log `currentDateFormat` to the console.
4. Create a function `formatDateMMDDYYYY(date)` that:
   - Returns:  
     `Formatted Date (MM/DD/YYYY): [month]/[day]/[year]`
5. Create a function `formatDateLong(date)` that:
   - Returns:  
     `Formatted Date (Month Day, Year): [Month name] [day], [year]`
6. Ensure all formatting uses the **en-US** locale.

---

## 📜 Example Output

```bash
Current Date and Time: Fri Sep 27 2024 16:04:43 GMT+0500 (Pakistan Standard Time)
Formatted Date (MM/DD/YYYY): 9/27/2024
Formatted Date (Month Day, Year): September 27, 2024
```

---

## 📁 Code Overview

```javascript
// Get current date
const currentDate = new Date();

// Format and log the current date
const currentDateFormat = `Current Date and Time: ${currentDate.toString()}`;
console.log(currentDateFormat);

// Convert to MM/DD/YYYY format
function formatDateMMDDYYYY(date) {
  const month = date.getMonth() + 1;
  const day = date.getDate();
  const year = date.getFullYear();
  return `Formatted Date (MM/DD/YYYY): ${month}/${day}/${year}`;
}

// Convert to Month Day, Year format
function formatDateLong(date) {
  const options = { year: 'numeric', month: 'long', day: 'numeric' };
  const formatted = date.toLocaleDateString('en-US', options);
  return `Formatted Date (Month Day, Year): ${formatted}`;
}
```

---

## 🚀 How to Run

1. Copy the code into a `.js` file (e.g., `dateConverter.js`).
2. Open the file in a browser console or run it using Node.js:

```bash
node dateConverter.js
```

---

## 🛠️ Requirements

* JavaScript (ES6+)
* Optional: Node.js or any modern browser

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

```
