<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>WebOS</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
  <!-- 1. BOOT SCREEN (shows on page load)  -->
  <!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
  <div id="boot-screen">
    <div id="boot-logo">WebOS</div>
    <div id="boot-loader"></div>
  </div>

  <!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
  <!-- 2. DESKTOP (main OS screen)          -->
  <!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
  <div id="desktop">

    <!-- 2a. Wallpaper / Background -->
    <div id="wallpaper"></div>

    <!-- 2b. Desktop Icons -->
    <div id="desktop-icons">
      <div class="icon" data-app="browser">
        <img src="icons/browser.png" alt="Browser" />
        <span>Browser</span>
      </div>
      <div class="icon" data-app="notepad">
        <img src="icons/notepad.png" alt="Notepad" />
        <span>Notepad</span>
      </div>
      <div class="icon" data-app="calculator">
        <img src="icons/calc.png" alt="Calculator" />
        <span>Calculator</span>
      </div>
      <div class="icon" data-app="filemanager">
        <img src="icons/folder.png" alt="Files" />
        <span>Files</span>
      </div>
    </div>

    <!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
    <!-- 3. WINDOWS AREA (apps open here)    -->
    <!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
    <div id="windows-area">

      <!-- Each app = one window -->
      <div class="window" id="window-notepad">

        <!-- 3a. Title Bar -->
        <div class="title-bar">
          <span class="window-title">📝 Notepad</span>
          <div class="window-controls">
            <button class="btn-minimize">–</button>
            <button class="btn-maximize">□</button>
            <button class="btn-close">✕</button>
          </div>
        </div>

        <!-- 3b. Window Content -->
        <div class="window-content">
          <textarea placeholder="Start typing..."></textarea>
        </div>

      </div>

      <!-- Calculator Window -->
      <div class="window" id="window-calculator">
        <div class="title-bar">
          <span class="window-title">🔢 Calculator</span>
          <div class="window-controls">
            <button class="btn-minimize">–</button>
            <button class="btn-maximize">□</button>
            <button class="btn-close">✕</button>
          </div>
        </div>
        <div class="window-content">
          <input type="text" id="calc-display" readonly />
          <div id="calc-buttons">
            <!-- Buttons will go here -->
          </div>
        </div>
      </div>

    </div><!-- end windows-area -->

    <!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
    <!-- 4. TASKBAR (bottom bar)             -->
    <!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
    <div id="taskbar">

      <!-- Start / App Menu Button -->
      <button id="start-btn">⊞ Start</button>

      <!-- Running Apps shown here -->
      <div id="taskbar-apps">
        <!-- JS will add app buttons here dynamically -->
      </div>

      <!-- System Tray (right side) -->
      <div id="system-tray">
        <span id="battery">🔋 100%</span>
        <span id="wifi">📶</span>
        <span id="clock">00:00</span>
      </div>

    </div><!-- end taskbar -->

    <!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
    <!-- 5. START MENU (opens on click)      -->
    <!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
    <div id="start-menu" class="hidden">
      <input type="text" id="search-bar" placeholder="Search apps..." />
      <ul id="app-list">
        <li data-app="notepad">📝 Notepad</li>
        <li data-app="calculator">🔢 Calculator</li>
        <li data-app="browser">🌐 Browser</li>
        <li data-app="filemanager">📁 File Manager</li>
      </ul>
    </div>

    <!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
    <!-- 6. CONTEXT MENU (right-click menu)  -->
    <!-- ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ -->
    <div id="context-menu" class="hidden">
      <ul>
        <li>Change Wallpaper</li>
        <li>New Folder</li>
        <li>Refresh</li>
      </ul>
    </div>

  </div><!-- end desktop -->

  <script src="script.js"></script>
</body>
</html>
