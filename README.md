nn
. 

@{
    ViewBag.Title = "Log in";
    Layout = null;
}

<head>
    <title>@ViewBag.Title</title>
    <link href="~/Content/login-register.css" rel="stylesheet" />
</head>

<body class="login-body">
    <div class="page-wrapper">
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
    </div>
</body>
..... 
... 
@model Airline_Managementnew.Models.User

@{
    ViewBag.Title = "Register";
    Layout = null;
}

<head>
    <title>@ViewBag.Title</title>
    <link href="~/Content/login-register.css" rel="stylesheet" />
</head>

<body class="login-body">
    <div class="page-wrapper">
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
    </div>
</body>

