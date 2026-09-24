# Publishing to GitHub

## Option 1 — GitHub CLI

After creating a new repository named `universal-expert-master-prompt` on GitHub:

```bash
git clone https://github.com/YOUR-USERNAME/universal-expert-master-prompt.git
cd universal-expert-master-prompt
# Copy the files from this project into the repository directory.
git add .
git commit -m "Initial release: Universal Expert Master Prompt"
git branch -M main
git push -u origin main
```

## Option 2 — Upload the ZIP

1. Create a new GitHub repository.
2. Extract `universal-expert-master-prompt.zip`.
3. Upload the repository contents to GitHub.
4. Commit the files to the `main` branch.

## Before Publishing

Replace these placeholders with your actual GitHub information:

- `your-username` in `README.md`
- `your-username` in `CITATION.cff`
- `[YOUR-LAST-NAME]` in `CITATION.cff`

You can also add a project description and GitHub topics using the metadata already prepared in `README.md`.
