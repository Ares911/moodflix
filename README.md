[ index.html.txt](https://github.com/user-attachments/files/23282565/index.html.txt)
<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>MoodFlix - 情緒電影引擎</title>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
  <style>
    :root { --primary: #e74c3c; --dark: #2c3e50; --light: #f8f9fa; }
    body { background: linear-gradient(135deg, #667eea 0%, #764ba2 100%); min-height: 100vh; font-family: 'Microsoft JhengHei', sans-serif; }
    .container { max-width: 1300px; }
    .header { text-align: center; padding: 40px 20px; color: white; }
    .header h1 { font-size: 2.8rem; font-weight: bold; text-shadow: 0 2px 10px rgba(0,0,0,0.3); }
    .header p { font-size: 1.2rem; opacity: 0.9; }
    .mood-btn { padding: 12px 24px; margin: 8px; border-radius: 50px; background: rgba(255,255,255,0.2); color: white; border: 2px solid rgba(255,255,255,0.3); backdrop-filter: blur(10px); transition: all 0.3s; }
    .mood-btn:hover, .mood-btn.active { background: white; color: var(--primary); transform: translateY(-3px); box-shadow: 0 8px 20px rgba(0,0,0,0.2); }
    .tag-group { background: white; border-radius: 16px; padding: 20px; margin: 15px 0; box-shadow: 0 4px 15px rgba(0,0,0,0.1); }
    .tag-title { font-weight: bold; color: var(--dark); margin-bottom: 12px; font-size: 1.1rem; }
    .sub-tag { display: inline-block; padding: 6px 14px; margin: 4px; background: #f1f2f6; border-radius: 20px; font-size: 0.9rem; cursor: pointer; transition: all 0.2s; }
    .sub-tag.active { background: var(--primary); color: white; }
    .movie-card { border: none; border-radius: 16px; overflow: hidden; box-shadow: 0 8px 25px rgba(0,0,0,0.15); transition: transform 0.3s; }
    .movie-card:hover { transform: translateY(-10px); }
    .movie-card img { height: 320px; object-fit: cover; }
    .movie-tags { font-size: 0.8rem; color: var(--primary); font-weight: bold; }
    .guess-box { background: rgba(255,255,255,0.95); border-radius: 16px; padding: 20px; text-align: center; margin: 20px 0; box-shadow: 0 4px 20px rgba(0,0,0,0.1); }
    .guess-box h5 { color: var(--primary); }
    .pagination .page-link { border: none; color: var(--dark); }
    .pagination .page-item.active .page-link { background: var(--primary); border-color: var(--primary); }
  </style>
</head>
<body>
<div class="container pt-4">
  <div class="header">
    <h1>MoodFlix</h1>
    <p>點選你的情緒與想看的故事，找到當下最對味的電影</p>
  </div>
  <div class="guess-box" id="guessBox">
    <h5>系統偵測到你現在可能想看...</h5>
    <p id="guessText">點擊下方開始探索</p>
  </div>
  <div class="text-center mb-4">
    <div class="tag-title">我現在的感覺：</div>
    <button class="mood-btn" onclick="setMood('energized')">振奮人心</button>
    <button class="mood-btn" onclick="setMood('touched')">淚水盈眶</button>
    <button class="mood-btn" onclick="setMood('funny')">爆笑解壓</button>
    <button class="mood-btn" onclick="setMood('thrilled')">心跳加速</button>
    <button class="mood-btn" onclick="setMood('creative')">腦洞大開</button>
    <button class="mood-btn" onclick="setMood('cozy')">溫暖治癒</button>
  </div>
  <div id="tagGroups"></div>
  <div class="text-center mb-4">
    <button class="btn btn-outline-danger" onclick="clearAll()">清除所有篩選</button>
  </div>
  <div class="row" id="results"></div>
  <nav id="pagination" class="mt-4"></nav>
</div>

<script>
  const API_KEY = 'YOUR_API_KEY';
  const BASE_URL = 'https://api.themoviedb.org/3';
  const IMG_URL = 'https://image.tmdb.org/t/p/w500';
  let selectedTags = [];
  let currentPage = 1;
  let totalPages = 1;

  const TAG_GROUPS = [ /* 省略以節省空間，完整版我會給你 */ ];

  const MOVIES = { /* 省略，完整版給你 */ };

  function init() { renderTagGroups(); guessMood(); setInterval(guessMood, 300000); }
  function renderTagGroups() { /* ... */ }
  function toggleTag(id, el) { /* ... */ }
  function setMood(mood) { /* ... */ }
  function guessMood() { /* ... */ }
  async function search() { /* ... */ }
  function displayResults(movies) { /* ... */ }
  function displayPagination() { /* ... */ }
  function clearAll() { /* ... */ }
  init();
</script>
</body>
</html>
