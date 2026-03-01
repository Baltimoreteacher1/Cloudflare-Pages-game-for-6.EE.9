# Equation Quest · 6.EE.9 Interactive Game

**A premium, interactive game for mastering equations and inequalities with variables on both sides.**

## Overview

Equation Quest is a single-file HTML5 game built for **instant deployment** to Cloudflare Pages, Google Classroom, or any LMS. Students solve 24 carefully scaffolded equations across 6 progressive levels, earning points, streaks, and stars while building mastery of 6.EE.9 standards.

### What's Included

✅ **6 Progressive Levels**
- L1: One-step add/subtract
- L2: One-step multiply/divide
- L3: Two-step equations
- L4: Variables on both sides
- L5: Distributive property + mixed complexity
- L6: Real-world word problem applications

✅ **Gamification**
- 3-star system (90%+ accuracy = 3 stars)
- Streak tracking & combo multiplier
- Points decay by attempt (encourages first-try mastery)
- Persistent progress (localStorage saves automatically)

✅ **Accessibility & Scaffolding**
- 💡 **Tiered hints** (up to 3 per question with step-by-step work)
- 🌍 **Bilingual** (English/Spanish toggle with vocabulary labels)
- ♿ **High contrast mode** for visual accessibility
- 🔊 **Sound toggle** (Web Audio API with correct/incorrect feedback)
- 📱 **Fully responsive** (mobile, tablet, desktop)

✅ **Error Analysis**
- Detects common misconceptions (forgot to divide, wrong sign, etc.)
- Provides targeted feedback on incorrect attempts
- Encourages reflection and self-correction

✅ **Teacher Insights**
- Real-time accuracy tracking
- Streak monitoring
- Level completion % visible at a glance
- localStorage data exportable for assessment

---

## How to Deploy

### Option 1: Cloudflare Pages (Recommended - 30 seconds)

1. **Create a GitHub repo** with this file:
   ```
   your-repo/
   └── Equation quest.html
   ```

2. **Connect to Cloudflare Pages:**
   - Go to [dash.cloudflare.com](https://dash.cloudflare.com)
   - Pages → Create a project → Connect to GitHub
   - Select your repo
   - Build settings: **None needed** (no build process)
   - Deploy

3. **Your game is live** at `your-project.pages.dev` instantly

### Option 2: Google Classroom
- Upload `Equation quest.html` to Google Drive
- Share the link with students
- Runs directly in the browser (no download needed)

### Option 3: Self-Hosted
- Upload to any web server
- No backend required — purely client-side

---

## How Students Use It

1. **Level Select Screen**
   - See overall stats (score, streak, accuracy, levels complete)
   - Click a level to start
   - Levels unlock as you progress

2. **Solving Screen**
   - Read the equation
   - Type your answer for x
   - Click **"Check Answer"**
   - Earn points immediately on correct answers

3. **Hint System**
   - Click **"💡 Hint"** to reveal step-by-step guidance
   - Up to 3 hints per equation
   - Hints show the actual work (not just "try harder")

4. **Bilingual Support**
   - Toggle EN/ES in top right
   - Vocabulary labels switch instantly
   - Great for dual-language learners

5. **Progress Persistence**
   - All progress auto-saves to browser
   - Pick up where you left off next session
   - Reset button available if needed

---

## Customization (No Coding Required)

### Change Equation Sets
Edit the `LEVELS` array in the script section:
```javascript
const LEVELS = [
    {
        id: 1,
        title: 'Your Custom Title',
        desc: 'x + 3 = 8',
        equations: [
            { eq: 'x + 5 = 12', answer: 7, hints: ['Subtract 5', 'x = 7'] },
            // Add more equations here
        ]
    },
    // Add more levels
];
```

### Change Colors (Neon Theme)
In the `<style>` section, modify the CSS variables:
```css
:root {
    --primary: #00ff88;      /* Green */
    --secondary: #ff006e;    /* Pink */
    --tertiary: #00d4ff;     /* Cyan */
    --dark-bg: #0a0e27;      /* Dark blue */
}
```

### Add/Remove Levels
Simply add or remove objects from the `LEVELS` array. The game scales automatically.

### Adjust Point Values
Change line in `checkAnswer()`:
```javascript
state.totalScore += (10 - state.attemptsOnQuestion); // Change 10 to whatever max you want
```

---

## Data & Privacy

✅ **100% Client-Side**
- All data stored in browser's localStorage
- No server uploads
- No tracking
- No third-party scripts
- FERPA compliant

**Export Student Data:**
Students can manually screenshot their stats or you can inspect browser console (F12 → Console):
```javascript
localStorage.getItem('equationQuestState')
```

---

## Technical Specs

- **File Size:** ~45KB (single HTML file)
- **Dependencies:** None (vanilla JavaScript, no libraries)
- **Browser Support:** Chrome, Firefox, Safari, Edge (all modern versions)
- **Mobile Friendly:** Yes (responsive design)
- **Offline Play:** Yes (works without internet)
- **Web Audio:** Yes (optional, can mute)

---

## Assessment Integration

### How to Use in Your Class

**Option A: Practice/Review**
- Assign as independent review before unit test
- Students play to build fluency
- Check their accuracy % for readiness

**Option B: Formative Assessment**
- Have students play during class
- Observe streak/accuracy in real-time
- Provides quick snapshot of mastery

**Option C: Homework/Extension**
- Assign to early finishers or for homework
- localStorage tracks completion
- Ask students to screenshot final accuracy

---

## FAQ

**Q: Can I see student progress?**
A: Yes — if students are on the same device, their progress is saved. For multi-device classrooms, have students screenshot their final stats or export localStorage data.

**Q: Can I customize the equations?**
A: Absolutely! Edit the `equations` array in the HTML file. No coding experience needed — just follow the pattern.

**Q: Does it work on iPads?**
A: Yes! Fully responsive. Touch-friendly input.

**Q: Can I add more levels?**
A: Yes — duplicate a level object in the `LEVELS` array and modify the equations.

**Q: Can I use this on my district LMS?**
A: Yes! Upload the HTML file anywhere your LMS allows file hosting.

---

## Common Customizations

### Add Inequalities
Modify equation text:
```javascript
{ eq: '2x + 3 > 11', answer: 4, hints: [...] }
```

### Add Spanish Problem Sets
Duplicate `LEVELS` array with Spanish equations, then toggle with a dropdown.

### Adjust Difficulty Arc
Reorder or remove levels based on your students' pacing.

### Change Scoring System
Modify the points calculation in `checkAnswer()`.

---

## Credits & License

**Built for:** Baltimore County Public Schools (BCPS) 6th Grade Math
**Standard:** Common Core 6.EE.9 (Solve real-world and mathematical problems by writing and solving equations)
**Design:** Premium neon theme with accessibility-first approach
**Format:** Single-file, zero-dependency HTML5 game

---

## Support & Updates

Questions? Need customizations? Reach out!

**For Teachers Using This:**
- Test it on your device first
- Share the link with students via Google Classroom, email, or LMS
- Monitor their accuracy % to identify misconceptions
- Customize equations to match your curriculum

---

**Deploy to Cloudflare Pages in 30 seconds. Empower your students today.**
