### -Lowercase the column name
### remove , . ; at end of string (do for both title (n) and metadata using transform)
```javascript
`value.replace(/[,;.]$/, "").trim()`
```
