## Imprint Normalization Workflow
### 1.Extract year from imprint into p year
1.Duplicate imprint
- Duplicate your original imprint column →  
    Rename original to `imprint (o)`
    Name it as `imprint (n)`
2. Remove final dot
-In imprint (n) → Edit cells → Transform:
```javascript
value.replace(/\.$/, "")
```
3.Create p year and extract numbers
-imprint (n)→ edit column → add column based on this column
-name the new column: p year
-in value box:
```javascript
forEach(value.split(/\D+/), v, if(v.length() == 4, v, null))[0]
```
4.Manually find other years
- Open **Facet → Text facet** on `p year`
- Click the **blank** facet
- Refer to `imprint (n)` and manually insert missing years
### 2.Extract location from imprint to p location
1. Remove the year from imprint (n)
-imprint (n) → Transform:
```javascript
value.replace(/[0-9]{4}/, "")
```
2. Remove empty / nuisance brackets
-imprint (n) → Transform:
```javascript
value.replace(/\[\.\]|\[\?\]|\[\]/, "").trim()
```
3. Create facet for text before colon
-imprint (n) → Facet → Custom text facet…
```javascript
if(value.contains(":"), value.split(":")[0].trim(), value)
```
4. Refining for ambiguous cities (e.g., `[london]`, `(london)` etc.)
- Go through each facet value
- Star all rows that are London
- Add new column p location (Edit column in imprint (n)→ Add column based on this column, in value write
`"london"`.Check preview to see if its starred values)
- UNSTAR ROWS using All column
5. Refinning for clear cities (e.g.: "London")
- Filter facet to "london"
- Star all rows
- In column `p location` → Transform → expression: `"london"`
- UNSTAR rows now from All column
6. Refining columns with 2 cities
- Use city 1 & city 2
