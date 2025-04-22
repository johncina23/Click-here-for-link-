# Click-here-for-link-
Full video 
<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>My Shortener Links</title>
  <style>
    body { font-family: Arial, sans-serif; padding: 20px; background: #f9f9f9; }
    h1 { color: #333; }
    form { margin-bottom: 20px; }
    input, button { padding: 10px; margin: 5px 0; width: 100%; max-width: 400px; }
    ul { list-style-type: none; padding: 0; }
    li { background: #fff; margin: 10px 0; padding: 10px; border: 1px solid #ccc; border-radius: 5px; }
    a { color: #007bff; text-decoration: none; }
  </style>
</head>
<body>
  <h1>My Shortener Links</h1>
  <form id="linkForm">
    <input type="text" id="title" placeholder="Enter title" required /><br />
    <input type="url" id="url" placeholder="Enter short link (e.g. https://bit.ly/xyz)" required /><br />
    <button type="submit">Add Link</button>
  </form>
  <ul id="linkList"></ul>  <script>
    const form = document.getElementById('linkForm');
    const linkList = document.getElementById('linkList');

    form.addEventListener('submit', function (e) {
      e.preventDefault();
      const title = document.getElementById('title').value;
      const url = document.getElementById('url').value;

      const li = document.createElement('li');
      li.innerHTML = `<strong>${title}</strong><br /><a href="${url}" target="_blank">${url}</a>`;
      linkList.appendChild(li);

      form.reset();
    });
  </script></body>
</html>
