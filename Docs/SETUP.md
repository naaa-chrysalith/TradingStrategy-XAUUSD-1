# Local Setup & Installation Guide

---

## ✅ Prerequisites

Before you begin, make sure you have:

1. **Git installed**
   - Windows: https://git-scm.com/download/win
   - Mac: `brew install git`
   - Linux: `sudo apt install git`

2. **MetaTrader 5 installed**
   - Download: https://www.metatrader5.com/

3. **Text Editor** (any of these):
   - Visual Studio Code (recommended): https://code.visualstudio.com/
   - Notepad++: https://notepad-plus-plus.org/
   - Sublime Text: https://www.sublimetext.com/

4. **GitHub account**
   - Already have: naaa-chrysalith ✅

---

## Step 1: Clone Repository to Local Machine

### Windows (PowerShell)

```powershell
# Navigate to your Documents or Projects folder
cd Documents

# Clone the repository
git clone https://github.com/naaa-chrysalith/TradingStrategy-Personal.git

# Go into the folder
cd TradingStrategy-Personal

# Verify (list contents)
ls
```

### Mac/Linux (Terminal)

```bash
# Navigate to your Documents or Projects folder
cd ~/Documents

# Clone the repository
git clone https://github.com/naaa-chrysalith/TradingStrategy-Personal.git

# Go into the folder
cd TradingStrategy-Personal

# Verify (list contents)
ls
```

---

## Step 2: Setup MetaTrader 5 Integration

### Find MT5 Experts Folder

Your MT5 folder location:

**Windows**:
C:\Users[YourUsername]\AppData\Roaming\MetaTrader 5\MQL5\Experts\

**Mac**:
~/Library/Application Support/MetaTrader 5/MQL5/Experts/

**Linux**:
~/.local/share/MetaTrader 5/MQL5/Experts/

### Create Folder Structure in MT5

Create folders matching your repo structure inside the `Experts` folder:
Experts/
├── XAUUSD-DayTrading/
│   ├── 01-SimpleScalper/
│   ├── 02-VolumeVolatility/
│   └── 03-PriceAction/
└── Development/

### Link Strategies to MT5

When you create a strategy (.mq5 file) in your repo folder:

**Option 1: Copy File**
```bash
# Copy your strategy file to MT5 Experts folder
# From: TradingStrategy-Personal/MQL5 - Active Trading/XAUUSD-DayTrading/01-SimpleScalper/
# To: MetaTrader 5/MQL5/Experts/XAUUSD-DayTrading/01-SimpleScalper/
```

**Option 2: Create Symbolic Link** (Advanced)

Windows PowerShell (Run as Admin):
```powershell
New-Item -ItemType SymbolicLink `
  -Path "C:\Users\[YourUsername]\AppData\Roaming\MetaTrader 5\MQL5\Experts\repo-strategies" `
  -Target "C:\Users\YourUsername\Documents\TradingStrategy-Personal\MQL5 - Active Trading"
```

---

## Step 3: Configure Git

### Set Your Name & Email (First Time Only)

```bash
git config --global user.name "naaa-chrysalith"
git config --global user.email "your.email@example.com"

# Verify
git config --global --list
```

### Create SSH Key (Optional but Recommended)

For secure pushes to GitHub without entering password each time:

```bash
# Generate SSH key
ssh-keygen -t ed25519 -C "your.email@example.com"

# Press Enter 3 times (no passphrase for simplicity)

# Copy the key
# Windows PowerShell: 
Get-Content ~/.ssh/id_ed25519.pub | Set-Clipboard

# Mac/Linux:
cat ~/.ssh/id_ed25519.pub | pbcopy (Mac)
cat ~/.ssh/id_ed25519.pub | xclip -selection clipboard (Linux)

# Go to GitHub Settings > SSH and GPG keys
# Click "New SSH Key" and paste
```

---

## Step 4: Create Your First Files

### Create a Simple Test EA File

**File**: `MQL5 - Active Trading/XAUUSD-DayTrading/01-SimpleScalper/SimpleScalper.mq5`

```cpp
//+------------------------------------------------------------------+
//|                                           SimpleScalper.mq5      |
//|                          Personal Trading Strategy - Fardayanaach |
//|                                                                   |
//+------------------------------------------------------------------+
#property copyright "naaa-chrysalith"
#property link      "https://github.com/naaa-chrysalith"
#property version   "1.00"
#property strict

//--- Input parameters
input double riskPercent = 0.20;  // 20% risk per trade
input int stoplossPoints = 250;   // Stop loss in points

//+------------------------------------------------------------------+
//| Expert initialization function                                   |
//+------------------------------------------------------------------+
int OnInit() {
  return(INIT_SUCCEEDED);
}

//+------------------------------------------------------------------+
//| Expert deinitialization function                                 |
//+------------------------------------------------------------------+
void OnDeinit(const int reason) {
}

//+------------------------------------------------------------------+
//| Expert tick function                                             |
//+------------------------------------------------------------------+
void OnTick() {
  // Strategy logic to be implemented
}
//+------------------------------------------------------------------+
```

### Add to Git & Commit

```bash
# Check status
git status

# Add the file
git add "MQL5 - Active Trading/XAUUSD-DayTrading/01-SimpleScalper/SimpleScalper.mq5"

# Commit
git commit -m "Add SimpleScalper EA template"

# Push to GitHub
git push origin main
```

---

## Step 5: Testing Your Setup

### Verify Repository Structure

```bash
# List all files and folders
# Windows:
tree /F

# Mac/Linux:
find . -type f | grep -v ".git" | head -20
```

### Verify Git Connection

```bash
# Check if connected to GitHub
git remote -v

# Should show:
# origin  https://github.com/naaa-chrysalith/TradingStrategy-Personal.git (fetch)
# origin  https://github.com/naaa-chrysalith/TradingStrategy-Personal.git (push)
```

### Test in MetaTrader

1. Open MetaTrader 5
2. Go to File > Open Data Folder
3. Navigate to MQL5 > Experts
4. You should see your XAUUSD-DayTrading folder
5. Right-click on SimpleScalper.mq5 > Compile
6. Check for any errors in the Toolbox panel

---

## Troubleshooting

### "Git is not recognized"
- Git not installed. Download from https://git-scm.com/

### "Cannot find MetaTrader folder"
- Check the exact path for your OS above
- Use `Find` (Mac) or `Search` (Windows) to locate it

### "SSH connection failed"
- Use HTTPS instead: `git remote set-url origin https://github.com/naaa-chrysalith/TradingStrategy-Personal.git`
- Or re-setup SSH keys following Step 3

### "Cannot compile MQL5"
- Missing includes? Check MQL5 documentation
- Make sure file is in correct Experts folder

---

## Next Steps

1. ✅ Clone repository ← You are here
2. ⏳ Add your first strategy
3. ⏳ Test in MT5
4. ⏳ Backtest
5. ⏳ Push results to GitHub

---

**Last Updated**: 2026-05-10  
**Trainer**: naaa-chrysalith