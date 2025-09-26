# League Dashboard Update Instructions

This repository contains two main dashboard files:

## 1. Store League Table Dashboard (`index.html`)
**Live URL**: https://gadgetmanuk.github.io/League/

### How to Update:
1. **Access Admin Mode**:
   - Add `?admin=1` to the URL
   - Example: `https://gadgetmanuk.github.io/League/?admin=1`

2. **Upload New Data**:
   - Click "Upload Data" in admin panel
   - Select your CSV file
   - Format required:
     ```csv
     Store,Participation %,Area Code
     STORE NAME,16.7,A033
     ```

3. **Export Current Data**:
   - Click "Export Current Data" to download JSON backup
   - Save this file for future reference

## 2. Incentive Rankings Dashboard (`incentive_rankings_filtered.html`)
**Live URL**: https://gadgetmanuk.github.io/League/incentive_rankings_filtered.html

### How to Update:
1. **Access Admin Mode**:
   - Add `?admin=1` to the URL
   - Example: `https://gadgetmanuk.github.io/League/incentive_rankings_filtered.html?admin=1`
   - Or triple-click the "v2.0" text on the page

2. **Upload New Data**:
   - Click "Upload Data" in admin panel
   - Support for both JSON and CSV formats
   - JSON Format Example:
     ```json
     {
       "STORE NAME": {
         "am": "Area Manager Name",
         "points": {
           "Incentive1": 100,
           "Incentive2": 150
         },
         "originalRank": 1,
         "originalMovement": 0
       }
     }
     ```

3. **Export/Backup Data**:
   - Click "Export Current Data" to download current data as JSON
   - File will be named `incentive_data_YYYY-MM-DD.json`

## Making Permanent Updates

### Option 1: Direct GitHub Update
1. Navigate to repository: https://github.com/GadgetManUk/League
2. Click on the file you want to update
3. Click the edit (pencil) icon
4. Update the data in the file
5. Commit changes with a description

### Option 2: Local Update and Push
1. Clone the repository (if not already done):
   ```bash
   git clone https://github.com/GadgetManUk/League.git
   cd League
   ```

2. Make your updates:
   ```bash
   # Edit either file:
   # - index.html
   # - incentive_rankings_filtered.html
   ```

3. Push your changes:
   ```bash
   git add .
   git commit -m "Update dashboard data"
   git push origin main
   ```

## Admin Features Available

Both dashboards include these admin features when `?admin=1` is added:
- 📤 Upload new data (JSON/CSV)
- 📊 Export current data
- 🗑️ Clear all data
- 🔄 Refresh data
- ✏️ Edit mode
- 🔒 Hide Admin Panel option

## Important Notes

1. **Browser Storage**:
   - Changes made through the admin panel are temporary
   - They only persist in your browser's localStorage
   - For permanent changes, update the file and push to GitHub

2. **GitHub Pages Updates**:
   - After pushing changes, it may take a few minutes for GitHub Pages to update
   - You can force a refresh in your browser with Ctrl+F5 (Windows) or Cmd+Shift+R (Mac)

3. **Backup Recommendation**:
   - Always export current data before making major changes
   - Keep backup JSON files for recovery if needed

4. **URL Parameters**:
   - Use `?admin=1` (with equals sign)
   - NOT `?admin-1` (with hyphen)

## Getting Help

If you need assistance:
1. Check this README
2. Export current data before making changes
3. Keep backups of your data files
4. Test changes locally before pushing to GitHub