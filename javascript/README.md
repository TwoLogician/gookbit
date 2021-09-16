*Locale Date*
```javascript
let date = new Date(2020, 1, 29)

date.toLocaleDateString("th-TH", {
    year: "numeric",
    month: "long",
    day: "numeric"
})

// 29 กุมภาพันธ์ 2563
```