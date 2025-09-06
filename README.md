<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Two Panel Live Update Demo</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="container">
    <!-- Left: Preview Area -->
    <div class="preview-panel">
      <div id="live-preview" class="live-preview">
        <span id="preview-text">Type something →</span>
      </div>
    </div>
    <!-- Right: Controls -->
    <div class="controls-panel">
      <div class="control-group">
        <label for="input-text">Type here:</label>
        <input type="text" id="input-text" placeholder="Your text goes here">
      </div>
    </div>
  </div>
  <script>
    // Simple live update logic
    const input = document.getElementById('input-text');
    const preview = document.getElementById('preview-text');
    input.addEventListener('input', function() {
      preview.textContent = input.value || "Type something →";
    });
  </script>
</body>
</html>
body {
  margin: 0;
  font-family: system-ui, sans-serif;
  background: #f5f5f5;
}

.container {
  display: flex;
  min-height: 100vh;
}

.preview-panel, .controls-panel {
  flex: 1 1 0;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 2rem;
  box-sizing: border-box;
}

.preview-panel {
  background: #fff;
  border-right: 1px solid #e5e5e5;
}

.live-preview {
  font-size: 2rem;
  color: #333;
  min-width: 300px;
  min-height: 80px;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 2px dashed #ccc;
  background: #fdfdfd;
  border-radius: 8px;
  padding: 2rem;
  text-align: center;
}

.controls-panel {
  background: #fafafa;
  flex-direction: column;
}

.control-group {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  width: 100%;
  max-width: 300px;
}

input[type="text"] {
  font-size: 1.2rem;
  padding: 0.5rem;
  border: 1px solid #aaa;
  border-radius: 4px;
}

@media (max-width: 800px) {
  .container {
    flex-direction: column;
  }
  .preview-panel {
    border-right: none;
    border-bottom: 1px solid #e5e5e5;
  }
}
