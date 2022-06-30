---
tags: utility
aliases: dashboard
cssclass: 
---

# ✅Tasks
```dataviewjs
dv.taskList(dv.pages('-"Bins"').file.tasks
	.where(t=> !t.completed));
```
---

```dataviewjs
let dates = {
  today: new Date(),
  activeFile: new Date(app.workspace.getActiveFile().name.substring(0, 10)),
};

let dateToCompare = dates.today;
let openFileDateFormatted = formatDate(dates.activeFile);
let pages = dv.pages('"Journal/Daily"').where(onThisDay);
let columns = ["File"];

function render() {
  dates.activeFile = new Date(
    app.workspace.getActiveFile().name.substring(0, 10)
  );

  if (isNaN(dates.activeFile)) {
    dateToCompare = dates.today;
  } else {
    dateToCompare = dates.activeFile;
  }

  pages = dv.pages('"Journal/Daily"').where(onThisDay);

  dv.container.empty();

  dv.header(2, "On this day");
  dv.list(pages.file.link);
}

render();
app.workspace.on("file-open", function cb() {
  render();
});

function pad(n, width, z) {
  z = z || "0";
  n = n + "";
  return n.length >= width ? n : new Array(width - n.length + 1).join(z) + n;
}

function formatDataviewDate(dateObject) {
  let month = pad(dateObject.file.day.month, 2);
  let day = pad(dateObject.file.day.day, 2);

  return `-${month}-${day}`;
}

function formatDate(date) {
  let month = pad(date.getMonth() + 1, 2);
  let day = pad(date.getDate(), 2);
  return `-${month}-${day}`;
}

function onThisDay(dailyNote) {
  return formatDataviewDate(dailyNote) == formatDate(dateToCompare);
}
```
## Links
[[01 Home]]