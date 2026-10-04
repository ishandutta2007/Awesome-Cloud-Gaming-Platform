# Awesome-Cloud-Gaming-Platform

$ErrorActionPreference = 'Stop'

# --- Guards ---
if (-not $env:GITHUB_TOKEN) {
    Write-Error "Error: set GITHUB_TOKEN in environment first"
    Start-Sleep -Seconds 30
    exit 1
}
$GITHUB_TOKEN = $env:GITHUB_TOKEN

if (-not $env:loops_path) {
    Write-Error "Error: set loops_path in environment first"
    Start-Sleep -Seconds 30
    exit 1
}
$loops_path = $env:loops_path

# --- Repo config ---
$repo_name = 'Awesome-Cloud-Gaming-Platform'
$repo_desc = 'Top Cloud Gaming Platform (Opensource) 🌟 Star if you like it! 🌟'

# --- Create repo ---
create-github-repo $repo_name -d $repo_desc --token $GITHUB_TOKEN

# --- Local init ---
mkdir $repo_name
cd $repo_name
"# $repo_name`n" | Out-File -Encoding utf8 README.md

git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin "https://github.com/ishandutta2007/$repo_name.git"
git pull origin main --allow-unrelated-histories
git push -u origin main

# --- Topics ---
gh repo edit ishandutta2007/$repo_name --add-topic curated-list,awesome-list

# --- Tabs & protection (custom scripts) ---
github-tabs Discussions --token $GITHUB_TOKEN
github-tabs Sponsorships --token $GITHUB_TOKEN
github-protect --token $GITHUB_TOKEN

# --- Copy boilerplate from sibling repo ---
Copy-Item ..\Awesome-BERT\.gitignore . -ErrorAction SilentlyContinue
Copy-Item ..\Awesome-BERT\LICENSE    . -ErrorAction SilentlyContinue

git add .
git commit -m "add .gitignore and LICENSE"
git pull
git push

# --- Cleanup stray backup files ---
if (Get-ChildItem -Filter *.bak -ErrorAction SilentlyContinue) {
    git rm --cached *.bak
    git commit -m "remove stray .bak files"
    git push
}

# --- Generate README via LLM ---
$repo_name = if ([string]::IsNullOrEmpty($repo_name)) { (Get-Item .).Name } else { $repo_name }
$real_repo_name = $repo_name -replace '^Awesome-', ''

# Append directive BEFORE invoking the CLI
Add-Content -Path "$loops_path\sheet_outputs\$real_repo_name.txt" `
            -Value "You must give the entire response in English language"

# Pick ONE generator:
chatgpt-cli "$loops_path\sheet_outputs\$real_repo_name.txt" -o "README.md" -w 600
# grok-cli  "$loops_path\sheet_outputs\$real_repo_name.txt" -o "README.md" -w 600

git add README.md
git commit -m "generate README"
git push

gh browse
