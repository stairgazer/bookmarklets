# Bookmarklets

## Google Sheets

### /htmlview (for quick links copying)

```js
javascript:(function(){var m=window.location.href.match(/\/d\/([a-zA-Z0-9-_]+)/);if(m){window.location.href='https://docs.google.com/spreadsheets/d/'+m[1]+'/htmlview';}})();
```

### Save as .csv

```js
javascript:(function(){var m=window.location.href.match(/\/d\/([a-zA-Z0-9-_]+)/);if(m){var g=(window.location.hash.match(/gid=(\d+)/)||[,'0'])[1];window.location.href='https://docs.google.com/spreadsheets/d/'+m[1]+'/gviz/tq?tqx=out:csv&gid='+g;}})();
```

### Copying Unlock

```js
javascript:(function(){var style=document.createElement('style');style.innerHTML='* { -webkit-user-select: text !important; -moz-user-select: text !important; -ms-user-select: text !important; user-select: text !important; pointer-events: auto !important; }';document.head.appendChild(style);document.addEventListener('contextmenu',function(e){e.stopPropagation();},true);document.addEventListener('copy',function(e){e.stopPropagation();},true);document.addEventListener('selectstart',function(e){e.stopPropagation();},true);var d=document.createElement('div');d.textContent='Copying Unlocked!';d.style.cssText='position:fixed;top:20px;right:20px;padding:12px 20px;background:#007BFF;color:#FFFFFF;border-radius:8px;font:14px sans-serif;z-index:99999;transition:opacity 0.5s';document.body.appendChild(d);setTimeout(function(){d.style.opacity='0';setTimeout(function(){d.remove()},500)},1500);})();
```

### Copy Sheet ID

```js
javascript:(function(){var m=window.location.href.match(/\/d\/([a-zA-Z0-9-_]+)/);if(m){navigator.clipboard.writeText(m[1]).then(function(){var d=document.createElement('div');d.textContent='Sheet ID copied!';d.style.cssText='position:fixed;top:20px;right:20px;padding:12px 20px;background:#007BFF;color:#FFFFFF;border-radius:8px;font:14px sans-serif;z-index:99999;transition:opacity 0.5s';document.body.appendChild(d);setTimeout(function(){d.style.opacity='0';setTimeout(function(){d.remove()},500)},1500);});}else{alert('Could not find Sheet ID.');}})();
```

### Plain HTML View

```js
javascript:(function(){var m=window.location.href.match(/\/d\/([a-zA-Z0-9-_]+)/);if(m){var g=(window.location.hash.match(/gid=(\d+)/)||[,'0'])[1];window.open('https://docs.google.com/spreadsheets/d/'+m[1]+'/gviz/tq?tqx=out:html&gid='+g);}})();
```
