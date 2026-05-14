# Gemini Data Assistant — Excel Add-in Setup Guide

## Aapko kya milega is add-in mein:
- ✅ Sheet scan karna (rows, columns, empty cells count)
- ✅ Duplicate rows hatana
- ✅ Spaces trim karna
- ✅ Text UPPERCASE / lowercase karna
- ✅ Empty cells yellow highlight karna
- ✅ Formatting clear karna
- ✅ Gemini AI se Hinglish mein sawaal poochna

---

## Step 1 — Files Host Karein (Free)

Sabse aasaan tarika: **GitHub Pages** (bilkul free)

1. GitHub account banayein: https://github.com
2. Naya repository banayein — naam: `gemini-excel-addin`
3. `taskpane.html` upload karein
4. Settings → Pages → Source: main branch select karein
5. Aapka URL milega: `https://YOUR-USERNAME.github.io/gemini-excel-addin/`

---

## Step 2 — manifest.xml Update Karein

`manifest.xml` file mein **"YOUR-HOSTING-URL"** ki jagah apna GitHub Pages URL daalen:

```
https://YOUR-USERNAME.github.io/gemini-excel-addin/taskpane.html
```

Yeh 4 jagah replace karna hai:
- `SourceLocation DefaultValue`
- `Commands.Url`
- `Taskpane.Url`
- Teenon `bt:Image` URLs (yeh optional hain, default icon use hoga)

Updated manifest.xml bhi GitHub pe upload karein.

---

## Step 3 — Excel mein Add-in Install Karein

### Windows Excel mein:
1. Excel kholen
2. **File → Options → Trust Center → Trust Center Settings**
3. **Trusted Add-in Catalogs** → naya catalog add karein
4. Ya seedha: **Insert → Get Add-ins → My Add-ins → Upload My Add-in**
5. `manifest.xml` file select karein
6. **Upload** click karein

### Mac Excel mein:
1. Excel kholen
2. **Insert → Add-ins → My Add-ins**
3. **Upload My Add-in** click karein
4. `manifest.xml` select karein

### Excel Online (browser) mein:
1. Excel Online kholen
2. **Insert → Add-ins → Upload My Add-in**
3. `manifest.xml` upload karein

---

## Step 4 — Add-in Use Karein

1. Excel mein **Home tab** mein "Gemini Assistant" button dikhega
2. Click karein — right side mein panel khulega
3. Apni **Gemini API key** daalen aur Save karein
4. **"Sheet scan karein"** button dabayein
5. Tools use karein ya AI se sawaal poochein!

---

## Gemini API Key Kahan Se Milegi? (Free!)

1. https://aistudio.google.com jayen
2. Google account se login karein
3. **"Get API Key"** click karein
4. **"Create API Key"** karein
5. Key copy karein aur add-in mein paste karein

> Free tier mein per day kaafi requests milti hain — personal use ke liye bilkul sufficient hai.

---

## Zaroori Note

- API key aapke browser mein locally save hoti hai (secure)
- Internet connection chahiye Gemini AI ke liye
- Excel 2016 ya usse naya version chahiye

---

## Problem Aaye Toh?

| Problem | Solution |
|---|---|
| "CORS error" aaye | GitHub Pages se host karo, local file se nahi |
| Add-in nahi dikh raha | Excel restart karo |
| API error aaye | API key dobara check karo |
| Sheet scan nahi ho rahi | Sheet mein kuch data hona chahiye |
