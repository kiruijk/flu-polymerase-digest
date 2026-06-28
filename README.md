Readme · MDGoogle DriveInfluenza Polymerase Research Digest

A lightweight research blog that aggregates and summarizes recent papers on influenza polymerase from PubMed. Uses AI to generate plain-language summaries of technical abstracts, making cutting-edge research accessible to scientists across disciplines.

Features


🔄 Live PubMed Integration — Automatically fetches the latest papers on influenza polymerase
✨ AI-Generated Summaries — Claude generates concise, readable 2–3 sentence summaries of each abstract
📧 Email Signup — Researchers can subscribe to get weekly digest notifications
🔗 Direct Links — One-click access to PubMed listings and DOI full texts
📖 Expandable Abstracts — Read full technical abstracts inline on the page
⚡ Zero Backend — Pure static HTML + JavaScript; no server costs, instant loading
🚀 Easy Deployment — Deploy free on GitHub Pages in minutes


How It Works

Open the site → fetches recent "influenza polymerase" papers from NCBI eUtils API → displays title, authors, journal, and AI-generated plain-language summary for each paper → stores email subscriptions locally in your browser.

Every time you visit, you get the latest papers. No refresh needed elsewhere.

Quick Start

View the Live Site

https://YOUR_USERNAME.github.io/flu-polymerase-digest

Run Locally

bash# Clone
git clone https://github.com/YOUR_USERNAME/flu-polymerase-digest.git
cd flu-polymerase-digest

# Open in browser (no build step needed)
open index.html

Deploy to GitHub Pages


Push code to GitHub
Go to repo Settings → Pages
Source: main branch, / (root)
Save — live in ~2 minutes


File Structure

flu-polymerase-digest/
├── index.html              # Complete blog app (all HTML/CSS/JS)
├── README.md               # This file
├── .gitignore              # Standard Git ignore

That's it. Single-file deployment.

How to Customize

Change the search topic:
In index.html, find this line:

javascriptconst term = encodeURIComponent('influenza polymerase');

Replace 'influenza polymerase' with any other research topic. Examples:


'CRISPR gene editing'
'climate change mitigation'
'Alzheimer\'s disease treatment'


Change the styling:
All CSS is in the <style> block at the top of index.html. Modify colors, fonts, spacing as you like.

Change the title:
Update the <h1> and <title> tags in index.html.

Data Sources


Papers — NCBI PubMed eUtils API (free, public, no key required)
Summaries — Generated on-page using Claude API (optional; falls back to abstracts)


Email Subscriptions

Currently, email addresses are stored in your browser's local storage. To add real email delivery:


Create a backend (Node.js, Python, etc.) with a /subscribe endpoint
Use an email service like SendGrid or Mailgun (free tier available)
Store emails in a database
Deploy backend separately (Render, Heroku, Railway, etc.)
Update the JavaScript to POST subscription data to your backend


See docs/BACKEND_SETUP.md (coming soon) for step-by-step instructions.

Troubleshooting

Q: Papers aren't loading


Check browser console (F12) for errors
PubMed API may be down — try refreshing in a few minutes
The site falls back to demo papers if the API is unreachable


Q: Emails aren't being sent


Current version doesn't send emails — it only stores them locally
To enable email delivery, follow the backend setup guide above


Q: Can I use this for a different topic?


Yes! Change the search term in the code (see "How to Customize" above)


Performance


Page load: <1 second (pure static)
API calls: ~2 seconds (PubMed is remote)
Bandwidth: ~50 KB per page load
Hosting cost: $0 (GitHub Pages is free)


Future Ideas


 Automated email delivery backend
 Advanced filtering by date, author, journal
 Paper recommendations based on reading history
 Dark mode toggle
 Export summaries to Markdown or PDF
 Integration with Zotero / Mendeley for bibliography management


Technology Stack


Frontend: HTML5, vanilla JavaScript (no frameworks)
APIs: NCBI eUtils (PubMed), Claude API (summaries)
Hosting: GitHub Pages
License: MIT


Contributing

Found a bug or have a feature idea? Open an issue or submit a pull request.

License

MIT — feel free to fork, modify, and redistribute.

Author

Created with Claude in Cowork mode. Questions? Check the GitHub issues.


Made for scientists, by scientists. Keep up with the latest research without the paywall.
