# How to Add Folders with Files to Your Repository

This guide explains how to add folders and files to your Git repository.

## Method 1: Using Git Command Line

### Step 1: Create a folder
```bash
mkdir folder-name
```

### Step 2: Add files to the folder
```bash
# Copy files into the folder
cp /path/to/file.txt folder-name/

# Or create a new file
echo "content" > folder-name/file.txt
```

### Step 3: Add the folder to Git
```bash
git add folder-name/
```

### Step 4: Commit and push
```bash
git commit -m "Add folder-name with files"
git push
```

## Method 2: Adding Empty Folders

Git doesn't track empty folders. To keep an empty folder in your repository, add a `.keep` file:

```bash
mkdir empty-folder
touch empty-folder/.keep
git add empty-folder/.keep
git commit -m "Add empty-folder placeholder"
git push
```

## Current Repository Structure

Your repository now has the following structure:

```
.
├── documents/          # Project documents and deliverables
│   ├── .keep
│   ├── TheCore4-Del1.pptx
│   ├── TheCore4-Deliverable1-Project Proposal.pdf
│   └── TheCore4-Team Deliverable 2.pdf
├── reports/            # Reports folder (placeholder for future use)
│   └── .keep
├── src/                # Source code folder (placeholder for future use)
│   └── .keep
└── website/            # Website files
    ├── *.html          # HTML pages
    ├── css/            # Stylesheets
    │   └── style.css
    ├── data/           # Data files
    │   └── catalog.csv
    ├── images/         # Images
    │   └── *.jpg
    └── js/             # JavaScript files
        └── scripts.js
```

## Tips

1. **Use meaningful folder names** - Choose names that clearly describe the contents
2. **Organize by type or function** - Group related files together
3. **Use .gitignore** - Exclude files you don't want in the repository (like build artifacts, dependencies, etc.)
4. **Add .keep files** - Use them to preserve empty folders that will be used later
5. **Commit regularly** - Make small, focused commits with clear messages

## Common Patterns

### Adding a new feature folder
```bash
mkdir feature-name
# Add your files
git add feature-name/
git commit -m "Add feature-name implementation"
git push
```

### Adding multiple folders at once
```bash
mkdir folder1 folder2 folder3
# Add files to each folder
git add folder1/ folder2/ folder3/
git commit -m "Add multiple folders"
git push
```

### Moving existing files into a folder
```bash
mkdir new-folder
mv file1.txt file2.txt new-folder/
git add -A  # Stages both deletions and additions
git commit -m "Organize files into new-folder"
git push
```

## What Was Done in This Repository

The following changes were made to organize your repository:

1. ✅ Created `documents/` folder with project deliverables
2. ✅ Created `reports/` folder with `.keep` placeholder
3. ✅ Created `src/` folder with `.keep` placeholder  
4. ✅ Organized website files into `website/` folder with subfolders:
   - `css/` - Stylesheets
   - `data/` - Data files
   - `images/` - Image assets
   - `js/` - JavaScript files
5. ✅ Created `.gitignore` to exclude unnecessary files

All files are now properly organized and committed to the repository!
