# Bookmarklets

## Google Sheets

### HTML view

```js
javascript:(function(){var m=window.location.href.match(/\/d\/([a-zA-Z0-9-_]+)/);if(m){window.location.href='https://docs.google.com/spreadsheets/d/'+m[1]+'/htmlview';}})();
```

### Save as .csv

```js
javascript:(function(){var m=window.location.href.match(/\/d\/([a-zA-Z0-9-_]+)/);if(m){window.location.href='https://docs.google.com/spreadsheets/d/'+m[1]+'/gviz/tq?tqx=out:csv&sheet=Sheet1';}})();
```

- For spreadsheets with multiple sheets: replace `Sheet1` with the name of sheet you're targeting.
