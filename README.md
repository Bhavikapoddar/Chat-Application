hiiii
.... 

... 
body {
    font-family: Arial, sans-serif;
    background-color: #f0f2f5;
    margin: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

.form-container {
    background-color: #fff;
    padding: 30px 40px;
    border-radius: 8px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
    width: 100%;
    max-width: 420px;
    box-sizing: border-box;
    text-align: center;
}

h2 {
    color: #333;
    margin-bottom: 25px;
    font-weight: 600;
}

.form-group {
    margin-bottom: 20px;
    text-align: left;
}

.form-group label {
    display: block;
    margin-bottom: 5px;
    color: #555;
    font-weight: bold;
}

.form-control {
    width: 100%;
    padding: 12px;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
    font-size: 16px;
    transition: border-color 0.3s;
}

.form-control:focus {
    border-color: #007bff;
    outline: none;
}

.btn-primary {
    width: 100%;
    padding: 12px;
    background-color: #007bff;
    color: #fff;
    border: none;
    border-radius: 4px;
    font-size: 18px;
    cursor: pointer;
    transition: background-color 0.3s;
}

.btn-primary:hover {
    background-color: #0056b3;
}

.text-center {
    margin-top: 15px;
}

.text-center a {
    color: #007bff;
    text-decoration: none;
}

.text-center a:hover {
    text-decoration: underline;
}

.text-danger {
    color: #dc3545;
    margin-top: 15px;
}

.text-success {
    color: #28a745;
    margin-top: 15px;
}
..... 
.... 
. 
.. 

.. 
@{
    ViewBag.Title = "Log in";
    Layout = null;
}

<head>
    <title>@ViewBag.Title</title>
    <link href="~/Content/login.css" rel="stylesheet" />
</head>

<body>
    <div class="form-container">
        <h2>Login</h2>
        @using (Html.BeginForm("Login", "User", FormMethod.Post))
        {
            <div class="form-group">
                <label for="Username">Username</label>
                <input type="text" name="Username" id="Username" class="form-control" required />
            </div>
            <div class="form-group">
                <label for="Password">Password</label>
                <input type="password" name="Password" id="Password" class="form-control" required />
            </div>
            <input type="submit" value="Login" class="btn-primary" />
        }

        @if (ViewBag.Error != null)
        {
            <p class="text-danger">@ViewBag.Error</p>
        }

        <div class="text-center">
            <p>Don't have an account? @Html.ActionLink("Register here", "Register", "User")</p>
        </div>
    </div>
</body>
..... 

.... 
.... 

.. @model Airline_Managementnew.Models.User

@{
    ViewBag.Title = "Register";
    Layout = null;
}

<head>
    <title>@ViewBag.Title</title>
    <link href="~/Content/login.css" rel="stylesheet" />
</head>

<body>
    <div class="form-container">
        <h2>Register</h2>
        @using (Html.BeginForm("Register", "User", FormMethod.Post))
        {
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
            
            <input type="submit" value="Register" class="btn-primary" />
        }

        @if (ViewBag.Message != null)
        {
            <p class="text-success">@ViewBag.Message</p>
        }

        <div class="text-center">
            <p>Already have an account? @Html.ActionLink("Login here", "Login", "User")</p>
        </div>
    </div>
</body>
..... 


