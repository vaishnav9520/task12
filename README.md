



### Task Overview: Create a Registration Page

#### Step 1: Create `index.html`
1. **Open VSCodium** and create a new file named `index.html`.
2. **Add HTML structure**:
   - Title: "Register"
   - Create a form with fields: 
     - First Name
     - Last Name
     - Email ID
     - Phone Number
     - Password
     - Confirm Password
   - Include a Submit button.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Register</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <h1>Register</h1>
    <form action="submit.html" method="get" onsubmit="return checkPasswords()">
        <label for="firstName">First Name:</label>
        <input type="text" id="firstName" name="firstName" required><br><br>
        
        <label for="lastName">Last Name:</label>
        <input type="text" id="lastName" name="lastName" required><br><br>
        
        <label for="email">Email ID:</label>
        <input type="email" id="email" name="email" required><br><br>
        
        <label for="phone">Phone Number:</label>
        <input type="tel" id="phone" name="phone" required><br><br>
        
        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required><br><br>
        
        <label for="confirmPassword">Password (Confirm):</label>
        <input type="password" id="confirmPassword" name="confirmPassword" required><br><br>
        
        <input type="submit" value="Submit">
    </form>

    <script src="script.js"></script>
</body>
</html>
```

#### Step 2: Create `submit.html`
1. Create a file named `submit.html`.
2. Add the message indicating successful registration.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration Complete</title>
</head>
<body>
    <h1>You've been registered. Please check your email for details.</h1>
</body>
</html>
```

#### Step 3: Run with Live Server
- Install the **Live Server** extension in VSCodium.
- Right-click on `index.html` and select "Open with Live Server".

#### Step 4: Add Basic CSS
1. Create `style.css`.
2. Add styles to improve the appearance of the form.

```css
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 20px;
    background-color: #f4f4f4;
}

h1 {
    color: #333;
}

form {
    background: #fff;
    padding: 20px;
    border-radius: 5px;
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

label {
    display: block;
    margin-bottom: 5px;
}

input[type="text"],
input[type="email"],
input[type="tel"],
input[type="password"] {
    width: 100%;
    padding: 10px;
    margin-bottom: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
}

input[type="submit"] {
    background-color: #28a745;
    color: white;
    border: none;
    border-radius: 4px;
    padding: 10px 15px;
    cursor: pointer;
}

input[type="submit"]:hover {
    background-color: #218838;
}
```

3. Link `style.css` in the `<head>` of `index.html`.

#### Step 5: Add JavaScript for Password Matching
1. Create `script.js`.
2. Add a function to check if passwords match.

```javascript
function checkPasswords() {
    const password = document.getElementById('password').value;
    const confirmPassword = document.getElementById('confirmPassword').value;

    if (password !== confirmPassword) {
        alert("Passwords do not match!");
        return false; // Prevent form submission
    }
    return true; // Allow form submission
}
```

3. Link `script.js` just before the closing `</body>` tag in `index.html`.

### Final Structure
- Ensure your directory has:
  - `index.html`
  - `submit.html`
  - `style.css`
  - `script.js`

### Testing
- Open your page in a browser using Live Server.
- Test the form submission and CSS styling.
