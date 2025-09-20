<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name = "viewport" content ="width = device-width, initial-scale=1.0">
    <title>simple registration form</title>
</head>
<body>
    <div>
        <h2> Contact Form </h2>
        <label for = "name">Name:</label>
        <input type ="text" id="name" name ="name">
    </div>
    <br>
    <div>
        <label for = "email">Email:</label>
        <input type ="email" id="email" name ="email">
    </div>
    <br>
    <div>
        <label for ="phone">Phone Number:</label>
        <input type ="tel" id = "phone" name = "phone" placeholder = "numeric" required aria-required = "true" aria-describedby ="phone-error" onkeypress ="restrictAlphabets(event)">
        <span id="phone-error" role="alert" style="display: none;">numbers only.</span>
    </div>
    <script>
        function restrictAlphabets(event) {
            const key = event.key;
            if(!/[0.9]/.test(key) && key !== "Backspace" && key !=="ArrowLeft" && key!=="ArrowRight") {
                event.preventDefault();
            }
        }
    </script>
</body>
</html>
