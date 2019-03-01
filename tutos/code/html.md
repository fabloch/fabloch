
[CSS: 2 colonnes](https://www.w3schools.com/howto/howto_css_two_columns.asp)

En CSS:
```
.column {
  float: left;
  width: 50%;
}


/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}
```

En HTML:
```
<div class="row">
  <div class="column"></div>
  <div class="column"></div>
</div>

```

Une css simple pour une belle préseentation
https://medium.com/mtholla/build-a-responsive-modern-dashboard-layout-with-css-grid-and-flexbox-bd343776a97e
