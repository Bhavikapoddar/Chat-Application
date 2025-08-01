hiiiii
.... 
... 
/* General Body Styles */
body {
    font-family: Arial, sans-serif;
    background-color: #f0f2f5;
    margin: 0;
}

/* Form Container - Replaced flexbox with traditional centering */
.form-container {
    background-color: #fff;
    padding: 30px;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    width: 100%;
    max-width: 400px;
    box-sizing: border-box;

    /* Centering using margin: auto */
    margin: 50px auto; /* Adjust top margin as needed */
}

/* Form Header */
h2 {
    text-align: center;
    margin-bottom: 20px;
    color: #333;
}

/* Form Elements */
.form-group {
    margin-bottom: 15px;
}

label {
    display: block;
    font-weight: bold;
    margin-bottom: 5px;
    color: #555;
}

input[type="text"],
input[type="password"],
input[type="email"] {
    width: 100%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
    font-size: 16px;
}

input[type="text"]:focus,
input[type="password"]:focus,
input[type="email"]:focus {
    border-color: #007bff;
    outline: none;
    box-shadow: 0 0 5px rgba(0, 123, 255, 0.5);
}

/* Submit Button */
input[type="submit"] {
    width: 100%;
    padding: 12px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 4px;
    font-size: 16px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

input[type="submit"]:hover {
    background-color: #0056b3;
}

/* Error and Message Styles */
.error-message, .success-message {
    text-align: center;
    margin-top: 15px;
}

.error-message {
    color: #dc3545;
}

.success-message {
    color: #28a745;
}

/* Specific styling for the body of login/register pages */
body.login-body {
    display: table; /* Acts as a container for centering */
    width: 100%;
    height: 100vh; /* Make it fill the viewport height */
}

body.login-body .form-container {
    display: table-cell;
    vertical-align: middle;
    margin: 0 auto; /* Center the form horizontally */
}
....... 
.. 
.. 
@{
    ViewBag.Title = "Log in";
    Layout = null;
}

<head>
    <title>@ViewBag.Title</title>
    @Styles.Render("~/Content/css")
    <link href="~/Content/style.css" rel="stylesheet" />
</head>

<body class="login-body">
    <div class="form-container">
        <h2>Login</h2>
        @using (Html.BeginForm("Login", "User", FormMethod.Post))
        {
            @* ... form groups here ... *@
            <div class="form-group">
                <label for="Username">Username</label>
                <input type="text" name="Username" id="Username" required />
            </div>
            <div class="form-group">
                <label for="Password">Password</label>
                <input type="password" name="Password" id="Password" required />
            </div>
            <input type="submit" value="Login" />
        }

        @if (ViewBag.Error != null)
        {
            <p class="error-message">@ViewBag.Error</p>
        }
    </div>
</body>
...... 
..... 
@model Airline_Managementnew.Models.User
@{
    ViewBag.Title = "Register";
    Layout = null;
}

<head>
    <title>@ViewBag.Title</title>
    @Styles.Render("~/Content/css")
    <link href="~/Content/style.css" rel="stylesheet" />
</head>

<body class="login-body">
    <div class="form-container">
        <h2>Register</h2>
        @using (Html.BeginForm("Register", "User", FormMethod.Post))
        {
            @* ... form groups here ... *@
            <div class="form-group">
                @Html.LabelFor(m => m.Username)
                @Html.TextBoxFor(m => m.Username, new { @class = "form-control", required = "required" })
            </div>

            <div class="form-group">
                @Html.LabelFor(m => m.Email)
                @Html.TextBoxFor(m => m.Email, new { @class = "form-control", required = "required" })
            </div>

            <div class="form-group">
                @Html.LabelFor(m => m.Password)
                @Html.TextBoxFor(m => m.Password, new { @class = "form-control", required = "required", type = "password" })
            </div>
            
            <input type="submit" value="Register" />
        }

        @if (ViewBag.Message != null)
        {
            <p class="success-message">@ViewBag.Message</p>
        }
    </div>
</body>
..... 
.......... 
..... 
