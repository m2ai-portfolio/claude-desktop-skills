# Quick Start Guide: Upload & Use Your Skills

## How to Upload Skills to Claude

### Step 1: Access Skills
1. Go to claude.ai
2. Open your project (or create one)
3. Click on "Skills" in the left sidebar
4. Click "Upload skill" or "Add custom skill"

### Step 2: Upload .skill Files
1. Select the .skill file from `/mnt/user-data/outputs/`
2. Upload (it's a ZIP file with .skill extension)
3. Claude will automatically extract and validate
4. The skill becomes available immediately in that project

### Step 3: Test Each Skill
Try these test prompts:

#### Resume Bullet Generator
```
"I need help turning my work experience into resume bullets. 
I'm a data analyst in healthcare, mid-level. 

My responsibilities included:
- Managing patient databases
- Creating reports
- Training new staff

Can you create professional resume bullets?"
```

#### Instagram Caption Generator
```
"Create an Instagram caption for a carousel post about 
meal prep tips. I'm a fitness coach targeting busy 
professionals. Tone should be motivational but practical."
```

#### Meeting Summary Generator
```
"Here's the transcript from our product planning meeting:

[paste a sample meeting transcript]

Can you create a summary with action items and owners?"
```

## How Skills Get Triggered

Claude's skill system uses **description matching**:

- User says: "help me write a cover letter"
- Claude sees: cover-letter-personalizer description mentions "cover letters for job applications"
- Skill triggers automatically!

**You don't need to mention the skill name.** Just describe what you need naturally.

## Skill Organization Tips

### Create Separate Projects by Suite

**Project: M2AI Career Tools**
- Upload: resume-bullet-generator.skill
- Upload: cover-letter-personalizer.skill
- Upload: job-description-generator.skill
- Upload: email-tone-converter.skill

**Project: M2AI Creator Tools**
- Upload: instagram-caption-generator.skill
- Upload: youtube-script-outliner.skill
- Upload: tweet-thread-generator.skill

**Project: M2AI Growth Tools**
- Upload: meeting-summary-generator.skill
- Upload: cold-email-personalizer.skill

**Benefit:** Cleaner skill selection, easier to share specific project links

### Or: Create One Master Project

**Project: M2AI Skills Suite**
- Upload all 9 skills
- Let Claude auto-select the right one

**Benefit:** One-stop-shop for all use cases

## Sharing Skills with Users

### Option 1: Project Invites
1. Create project with uploaded skills
2. Invite users to project
3. They get access to all skills in that project

### Option 2: Distribute .skill Files
1. Share .skill files directly
2. Users upload to their own accounts
3. They "own" the skill (can modify if needed)

### Option 3: Claude Skill Marketplace (Future)
When public marketplace launches, you can:
- Publish skills publicly
- Get discovery through Claude's interface
- Build reputation as skill creator

## Monitoring Usage

### What to Track
- Which skills get used most?
- What types of requests trigger each skill?
- Where do users get stuck?
- What improvements are requested?

### Feedback Loop
1. User uses skill
2. User provides feedback (manual or survey)
3. Update SKILL.md with improvements
4. Re-package and re-upload
5. Announce update to users

## Upgrading Skills

### When to Update
- User finds edge case you didn't handle
- Better examples discovered
- New industry-specific needs
- Quality improvements

### How to Update
1. Edit the source SKILL.md in `/home/claude/[skill-name]/`
2. Re-run package script:
   ```bash
   python /mnt/skills/examples/skill-creator/scripts/package_skill.py \
     /home/claude/[skill-name] /home/claude
   ```
3. Upload new .skill file (overwrites old version)
4. Users get updated version automatically

## Combining Skills with Other Tools

Skills work alongside:
- **Web search:** Research before personalizing
- **Analysis:** Process data before summarizing
- **Other skills:** Chain multiple skills together

**Example workflow:**
1. User: "Find job postings for data analyst roles in Austin"
2. Claude uses web search
3. User: "Write a cover letter for the first one"
4. Claude uses cover-letter-personalizer skill
5. User: "Make the tone more casual"
6. Claude uses email-tone-converter skill

## Common Issues & Solutions

### Issue: Skill not triggering
**Solution:** Make your request more specific to the skill's description
- Instead of: "help with writing"
- Try: "help me write resume bullets for my data analyst experience"

### Issue: Wrong skill triggered
**Solution:** Create more specific projects or rephrase request

### Issue: Output not matching expectations
**Solution:** Provide more input details (the skills ask for specific info)

### Issue: Skill seems slow
**Solution:** Skills with complex guidelines take longer - this is normal

## Integration with n8n (Advanced)

These skills can be called from n8n workflows:

1. **Via Claude API:**
   - n8n → Claude API node
   - Include skill in project context
   - Pass structured input
   - Receive structured output

2. **Webhook Trigger:**
   - User submits form (Typeform, Airtable)
   - n8n catches webhook
   - Calls Claude with skill
   - Returns result via email/Slack

3. **Scheduled Jobs:**
   - Daily summary of meetings (via meeting-summary skill)
   - Weekly job description generation
   - Automated social media caption generation

**Example: Auto-summarize Zoom meetings**
```
Trigger: Zoom recording completed
→ n8n gets transcript
→ Calls Claude with meeting-summary-generator
→ Posts summary to Slack
→ Creates tasks in Asana
```

## Best Practices

### For Skill Users
1. Provide complete context upfront
2. Use natural language (don't try to "game" the skill)
3. Iterate if first output isn't perfect
4. Save examples of great outputs

### For Skill Creators (You)
1. Keep SKILL.md under 500 lines
2. Use before/after examples liberally
3. Handle edge cases explicitly
4. Update based on user feedback
5. Version your skills (in description or filename)

## Marketing Your Skills

### Free Distribution
- Share on X/LinkedIn with examples
- Create video tutorials showing usage
- Write blog posts: "How I built X skill"
- GitHub repo with all .skill files

### Lead Capture
- Landing page: Download skill in exchange for email
- Email nurture: Free skill → paid automation
- Consultation offer: "Need this automated? Book a call"

### Paid Distribution
- Sell access to premium skills
- Offer "skill + implementation" packages
- White-label skills for agencies

## Next Steps

1. **Test all 9 skills** with real use cases
2. **Document any issues** or improvement ideas
3. **Share with beta users** (5-10 people)
4. **Collect feedback** and iterate
5. **Launch publicly** with marketing content

Ready to deploy! 🚀
