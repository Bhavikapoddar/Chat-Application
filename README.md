/* General Body and Centering */
body.login-body {
    background: #4A90E2; /* Solid color fallback */
    background: linear-gradient(135deg, #4A90E2 0%, #50E3C2 100%);
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    margin: 0;
    color: #333;
    
    /* Centering using table layout (compatible with older browsers) */
    height: 100vh;
    width: 100%;
    display: table;
}

.page-wrapper {
    display: table-cell;
    vertical-align: middle;
}

/* Form Container */
.form-container {
    background-color: #ffffff;
    padding: 40px;
    border-radius: 10px;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
    max-width: 400px;
    width: 90%;
    box-sizing: border-box;
    margin: 0 auto;
}

/* Form Title */
.form-container h2 {
    text-align: center;
    color: #4A90E2;
    margin-bottom: 30px;
    font-weight: 700;
}

/* Form Group and Label */
.form-group {
    margin-bottom: 20px;
}

.form-group label {
    display: block;
    margin-bottom: 8px;
    color: #555;
    font-weight: 600;
    font-size: 0.95em;
}

/* Input Fields */
.form-control {
    width: 100%;
    padding: 12px 15px;
    border: 1px solid #ddd;
    border-radius: 5px;
    box-sizing: border-box;
    font-size: 1em;
    transition: all 0.3s ease;
}

.form-control:focus {
    outline: none;
    border-color: #4A90E2;
    box-shadow: 0 0 8px rgba(74, 144, 226, 0.2);
}

/* Submit Button */
.btn-primary {
    width: 100%;
    padding: 12px 15px;
    background-color: #4A90E2;
    color: white;
    border: none;
    border-radius: 5px;
    font-size: 1.1em;
    font-weight: 600;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

.btn-primary:hover {
    background-color: #3A78BF;
}

/* Links and Messages */
.text-center {
    margin-top: 25px;
    text-align: center;
}

.text-center p {
    margin: 0;
    color: #666;
}

.text-center a {
    color: #4A90E2;
    text-decoration: none;
    font-weight: 600;
    transition: color 0.3s ease;
}

.text-center a:hover {
    color: #3A78BF;
    text-decoration: underline;
}

.text-danger {
    color: #dc3545;
    margin-top: 15px;
    text-align: center;
    font-size: 0.9em;
}

.text-success {
    color: #28a745;
    margin-top: 15px;
    text-align: center;
    font-size: 0.9em;
}
