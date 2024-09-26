<!DOCTYPE html>
<html>
<head>
  <title>User Data Generator</title>
</head>
<body>
  <h1>User Data Generator</h1>
  <form>
    <label for="numUsers">Number of users:</label>
    <input type="number" id="numUsers" name="numUsers" value="10">
    <button type="submit">Generate Data</button>
  </form>

  <a href="/download-csv" download="users.csv">Download CSV</a>

  <script>
    const form = document.querySelector('form');
    form.addEventListener('submit', (e) => {
      e.preventDefault();
      const numUsers = document.querySelector('#numUsers').value;
      fetch(/generate-data?numUsers=${numUsers})
        .then((res) => res.text())
        .then((message) => console.log(message));
    });
  </script>
</body>
</html>
<!---
dcube10/dcube10 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
