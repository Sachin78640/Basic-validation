<!DOCTYPE html>
<html>
<head>
  <title>Form with Basic Validation</title>
</head>
<body>
  <h1>Registration Form</h1>
  <form id="registrationForm" onsubmit="validateForm(event)">
    <label for="name">Name:</label>
    <input type="text" id="name" required><br>

    <label for="email">Email:</label>
    <input type="email" id="email" required><br>

    <label for="phone">Phone Number:</label>
    <input type="tel" id="phone" required><br>

    <label for="password">Password:</label>
    <input type="password" id="password" required><br>

    <label for="age">Age:</label>
    <input type="number" id="age" required><br>

    <label for="gender">Gender:</label>
    <select id="gender" required>
      <option value="">Select gender</option>
      <option value="male">Male</option>
      <option value="female">Female</option>
      <option value="other">Other</option>
    </select><br>

    <label for="date">Date:</label>
    <input type="date" id="date" required><br>

    <label for="color">Favorite Color:</label>
    <input type="color" id="color" required><br>

    <input type="submit" value="Submit">
  </form>

  <script>
    function validateForm(event) {
      event.preventDefault(); // Prevent form submission

      // Get form field values
      var name = document.getElementById('name').value;
      var email = document.getElementById('email').value;
      var phone = document.getElementById('phone').value;
      var password = document.getElementById('password').value;
      var age = document.getElementById('age').value;
      var gender = document.getElementById('gender').value;
      var date = document.getElementById('date').value;
      var color = document.getElementById('color').value;

      // Perform validation
      if (!name || !email || !phone || !password || !age || !gender || !date || !color) {
        alert("Please fill out all fields");
        return;
      }

      // Additional validation logic can be added here

      // Submit the form if all validation passes
      document.getElementById('registrationForm').submit();
    }
  </script>
</body>
</html>
