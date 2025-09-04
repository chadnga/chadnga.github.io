<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Live Monogram Previewer</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="container">
    <!-- Left: Preview Area -->
    <div class="preview-panel">
      <div id="preview-area">
        <canvas id="preview-canvas" width="512" height="512"></canvas>
      </div>
    </div>
    <!-- Right: Controls -->
    <div class="controls-panel">
      <form id="controls-form" onsubmit="return false;">
        <label>
          Name:<br>
          <input type="text" id="input-name" placeholder="Enter name..." maxlength="32">
        </label>
        <label>
          Font:
          <select id="font-select">
            <option value="serif">Serif</option>
            <option value="sans-serif">Sans Serif</option>
            <option value="monospace">Monospace</option>
            <option value="cursive">Cursive</option>
            <option value="fantasy">Fantasy</option>
          </select>
        </label>
        <label>
          Upload Font:
          <input type="file" id="font-upload" accept=".ttf,.otf,.woff,.woff2">
        </label>
        <label>
          Font Size: <input type="number" id="font-size" min="10" max="200" value="64"> px
        </label>
        <label>
          Line Height: <input type="number" id="line-height" min="1" max="3" step="0.1" value="1.1">
        </label>
        <label>
          Letter Spacing: <input type="number" id="letter-spacing" min="0" max="20" value="0"> px
        </label>
        <label>
          Text Color: <input type="color" id="color-picker" value="#111111">
        </label>
        <label>
          Alignment:
          <select id="text-align">
            <option value="center">Center</option>
            <option value="left">Left</option>
            <option value="right">Right</option>
          </select>
        </label>
        <label>
          Background Image:
          <input type="file" id="bg-upload" accept="image/*">
        </label>
        <button type="button" id="export-btn">Export PNG</button>
      </form>
    </div>
  </div>
  <script src="app.js"></script>
</body>
</html>
