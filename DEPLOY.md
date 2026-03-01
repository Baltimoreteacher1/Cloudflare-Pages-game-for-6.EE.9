# Quick Start: Deploy & Share

## 30-Second Deployment to Cloudflare Pages

### Step 1: Create GitHub Repo
```bash
# Initialize repo locally
git init
git add .
git commit -m "Initial commit: Equation Quest game"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/equation-quest.git
git push -u origin main
```

### Step 2: Connect to Cloudflare
1. Go to [dash.cloudflare.com](https://dash.cloudflare.com)
2. Click **Pages** → **Create a project**
3. Select **Connect to Git**
4. Authorize GitHub & select your `equation-quest` repo
5. **Build settings:**
   - Framework preset: *None*
   - Build command: *(leave blank)*
   - Build output directory: *(leave blank)*
6. Click **Save and Deploy**

✅ **Done!** Your game is live at `equation-quest.pages.dev`

---

## Share With Students

### Option A: Direct Link (Easiest)
```
https://equation-quest.pages.dev
```
Paste in Google Classroom, email, or LMS.

### Option B: Google Classroom
1. Create assignment
2. Add "Websites" attachment
3. Paste the Cloudflare URL
4. Students click → plays in browser

### Option C: Create Custom Domain (Optional)
In Cloudflare Pages settings:
- Add custom domain (e.g., `equation-quest.bcps.edu`)
- Points to your Pages deployment

---

## Monitor Student Progress

### How to Check Individual Progress
Students' progress is saved **locally on their device**. To see:

1. **Ask student to screenshot their stats:**
   - Level Select screen shows: Score, Streak, Levels Complete, Accuracy %

2. **Or export their data:**
   - Have them open browser DevTools (F12)
   - Go to Console tab
   - Type: `copy(localStorage.getItem('equationQuestState'))`
   - Paste into a text file to see their full progress object

3. **Class-Wide View:**
   - Run a practice session
   - Take screenshots of everyone's Level Select screen before dismissal
   - Compile accuracy data in a spreadsheet

---

## Customization After Deploy

**If you edit the HTML file:**
1. Make changes to `Equation quest.html`
2. Commit & push:
   ```bash
   git add .
   git commit -m "Updated equations"
   git push
   ```
3. Cloudflare redeploys automatically (~30 seconds)
4. Students see the update next time they visit

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Game won't load | Check browser console (F12) for errors; try different browser |
| Progress not saving | Check if localStorage is enabled; not available in private/incognito mode |
| Equations seem too hard | Edit the HTML file and adjust equation values |
| Mobile layout broken | Check viewport — game is fully responsive |
| Sound not working | Check browser permissions; mute button may be enabled |

---

## File Structure (What You're Pushing)

```
equation-quest/
├── Equation quest.html    ← The game (this is all you technically need)
├── README.md              ← Documentation
├── .gitignore             ← Git ignore rules
└── DEPLOY.md              ← This file
```

---

## Next Steps (Optional Enhancements)

- [ ] Add custom equations for your specific class
- [ ] Create a teacher version that shows all student progress
- [ ] Export student data to a dashboard
- [ ] Add more levels or difficulty tiers
- [ ] Integrate with Google Forms for quicker formative assessment

---

**Questions?** Check README.md for full documentation.
