# 🚨 SMS Scam Prevention - Remote Pattern Updates

**Author:** Rajveer Khanvilkar  
**App:** SMS Scam Prevention  
**Purpose:** Protecting users from SMS scams with real-time pattern updates

---

## **Overview**
This repository contains scam detection patterns that are automatically downloaded by the SMS Scam Prevention Android app. Users get instant protection from new scams without needing app updates!

---

## **Files**

### **1. url-scam-patterns.json**
**Purpose:** Detects scam URLs/links in SMS messages

**Used for:**
- Link/URL analysis
- Domain checking
- Path pattern matching
- Phishing link detection

**Categories:**
- Guaranteed scams (free-money, instant-loan)
- Digital arrest scams
- UPI/Banking scams
- Government impersonation
- Crypto/Investment scams
- Delivery/Prize scams
- Job scams
- SIM/Telecom scams
- WhatsApp/Meta scams
- APK download scams
- QR code scams
- OTP/Session scams

**Example:**
```
SMS: "You won! Click: bit.ly/prize123"
URL: bit.ly/prize123 → Redirects to → scam-lottery.xyz
Detection: "lottery", "prize" keywords → BLOCKED ❌
```

---

### **2. sms-text-patterns.json**
**Purpose:** Detects scam content in SMS message text

**Used for:**
- Message content analysis
- Keyword detection
- Psychological tactic detection
- Sender verification

**Categories:**
- Emergency keywords (urgent, expire, suspend)
- Fear tactics (account blocked, card suspended)
- Prize/Lottery scams (KBC, winner, prize)
- Money offers (free money, instant loan)
- Government impersonation (income tax, aadhaar)
- Banking keywords (OTP, CVV, PIN)
- Action required (click here, verify now)
- Job/Work scams (work from home, data entry)
- Investment scams (guaranteed returns, crypto)
- Delivery scams (parcel, courier)
- Digital arrest (cyber police, FIR)
- SIM/Telecom (sim blocked, number suspended)
- WhatsApp/Meta (account suspended, blue tick)
- Curiosity tactics (secret admirer, shocking news)

**Example:**
```
SMS: "Your account is suspended. Click to verify immediately!"
Detection: "suspended" + "verify" + "immediately" → DANGEROUS ❌
```

---

## **How It Works**

### **For Users:**
```
1. Install app from Play Store
2. App downloads latest patterns (once)
3. Protected from all scams ✅
4. Patterns update automatically (daily)
5. No app update needed!
```

### **For You (Admin):**
```
1. New scam discovered
2. Edit JSON file on GitHub
3. Commit changes
4. Users protected within 24 hours ✅
```

---

## **Update Workflow**

### **Example: New scam appears**
```
News: "New scam using 'pm-kisan-refund'"

Your action:
1. Open sms-text-patterns.json
2. Add "pm-kisan-refund" to govt_impersonation array
3. Commit changes
4. Done! (30 seconds)

Result:
- File updated instantly ✅
- All users download update within 24 hours ✅
- Everyone protected ✅
```

---

## **File Structure**

```json
{
  "version": "2025.12.29.001",
  "last_updated": "2025-12-29T19:16:00+05:30",
  "min_app_version": "1.0",
  "type": "url_patterns",
  
  "category_name": [
    "keyword-1",
    "keyword-2",
    "keyword-3"
  ]
}
```

---

## **Version Control**

**Format:** `YYYY.MM.DD.XXX`
- `YYYY` = Year
- `MM` = Month
- `DD` = Day
- `XXX` = Build number (001, 002, etc.)

**Example:** `2025.12.29.001`

---

## **Adding New Patterns**

### **Step 1: Identify scam type**
```
Is it a URL/link scam? → Edit url-scam-patterns.json
Is it SMS text scam? → Edit sms-text-patterns.json
```

### **Step 2: Choose category**
```
URL patterns:
- guaranteed_scams
- digital_arrest
- upi_scams
- banking_scams
- etc.

SMS patterns:
- emergency_keywords
- fear_tactics
- prize_lottery
- money_offers
- etc.
```

### **Step 3: Add keyword**
```json
"category_name": [
  "existing-keyword-1",
  "existing-keyword-2",
  "new-keyword-here"  ← Add here
]
```

### **Step 4: Update version**
```json
"version": "2025.12.29.002",  ← Increment
"last_updated": "2025-12-29T20:00:00+05:30"  ← Update timestamp
```

### **Step 5: Commit**
```
Commit message: "Added pm-kisan-refund to govt_impersonation"
```

---

## **Testing**

### **Before committing:**
1. Validate JSON syntax (use jsonlint.com)
2. Check for duplicates
3. Verify category is correct
4. Update version number

### **After committing:**
1. Check file is accessible
2. Wait 24 hours
3. Verify users are protected

---

## **URLs for App**

```
URL Patterns:
https://raw.githubusercontent.com/YOUR-USERNAME/sms-scam-patterns/main/url-scam-patterns.json

SMS Patterns:
https://raw.githubusercontent.com/YOUR-USERNAME/sms-scam-patterns/main/sms-text-patterns.json
```

---

## **Statistics**

**Current patterns:**
- URL patterns: 200+ keywords
- SMS patterns: 150+ keywords
- Total: 350+ scam indicators

**Update frequency:** Daily (automatic)
**Download size:** ~10 KB (tiny!)
**Users protected:** All app users

---

## **Changelog**

### **2025.12.29.001**
- Initial release
- Added all 2025 scam categories
- Separated URL and SMS patterns

---

## **Support**

**Developer:** Rajveer Khanvilkar  
**App:** SMS Scam Prevention  
**Issues:** Report new scams or false positives  
**Updates:** Check version number in JSON files  

---

**Protecting users from SMS scams, one pattern at a time!** 🛡️  
**Made with ❤️ by Rajveer Khanvilkar**
