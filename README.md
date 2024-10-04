<p align="center">
  <img src="https://i.imgur.com/4ESXHWV.png" width="20%" alt="SCHOOL_SSL_INSPECTION-logo">
</p>
<p align="center">
    <h1 align="center">SCHOOL_SSL_INSPECTION</h1>
</p>
<p align="center">
	<img src="https://img.shields.io/github/license/temrage/school_ssl_inspection?style=flat&logo=opensourceinitiative&logoColor=white&color=0080ff" alt="license">
	<img src="https://img.shields.io/github/last-commit/temrage/school_ssl_inspection?style=flat&logo=git&logoColor=white&color=0080ff" alt="last-commit">
	<img src="https://img.shields.io/github/languages/top/temrage/school_ssl_inspection?style=flat&color=0080ff" alt="repo-top-language">
	<img src="https://img.shields.io/github/languages/count/temrage/school_ssl_inspection?style=flat&color=0080ff" alt="repo-language-count">
  
# 🚨 SSL Inspection Bypass Guide

SSL inspection is essentially a **"man-in-the-middle" (MitM)** attack, where a network device intercepts and decrypts your encrypted internet traffic. This process can jeopardize your privacy, and while it’s something you can't completely bypass due to its server-sided nature, this guide shows how to install an SSL certificate to **ignore** and **bypass** the persistent "Your connection is not secure" warnings.

❗ **This guide is for:**  
- New device users trying to connect to a school network.
- Anyone receiving HTTPS errors (like "Your connection is not private").
  
⚠️ **Before starting**:  
Make sure to delete all existing certificates to avoid conflicts due to expired certificates!

---

## 🔍 **How SSL Inspection Works**:

1. **Intercept Traffic**: The network device steps in between your device and the website you’re visiting.
2. **Decrypt Data**: The device decrypts the encrypted data to check for anything suspicious.
3. **Inspect Data**: The decrypted data is scanned for security threats or policy violations.
4. **Re-encrypt & Forward**: After inspection, the device re-encrypts the data and forwards it to the website, completing the loop.

---

## 🔑 **Why a Certificate is Needed**:

When SSL inspection is enabled, the network device acts as a MitM between the user and the website. This can trigger security warnings (e.g., "Your connection is not secure") because the certificate presented by the network device isn't the website's original certificate. 

To avoid these warnings, the network device generates its own SSL/TLS certificate, which you’ll need to install on your device.

📥 **Download the latest certificate here:**  
[ssl.crt](https://github.com/temrage/school_ssl_inspection/releases/download/release/ssl.crt)

---

## 🖥️ **Installation Instructions**

### **Windows**:

1. **Download** the latest certificate from your school.
2. **Open the Certificate**:
   - Double-click the certificate file to open it.
3. **Install the Certificate**:
   - Click "Install Certificate" and choose to install it for the "Current User".
4. **Choose Store Location**:
   - Select "Place all certificates in the following store".
   - Click "Browse" and choose "Trusted Root Certification Authorities".
   - Click "Next" and then "Finish".
5. **Restart your browser and clear cache**.

---

### 📱 **iOS**:

1. **Download** the latest certificate from your school.
2. **Install the Certificate**:
   - iOS will prompt you to install a new profile.
   - Go to "Settings" and tap on "Profile Downloaded".
   - Tap "Install" in the top-right corner.
   - If prompted, enter your device passcode.
3. **Trust the Certificate**:
   - Go to "Settings" > "General" > "About" > "Certificate Trust Settings".
   - Toggle the switch next to the certificate to enable full trust.

---

### 🍏 **macOS**:

1. **Download** the latest certificate from your school.
2. **Install the Certificate**:
   - Double-click the certificate file, which should open in **Keychain Access**.
3. **Add to Keychain (System)**:
   - In Keychain Access, select the "System" keychain (NOT iCloud).
   - Click "Add".
4. **Add to Keychain (Login)**:
   - Re-open the certificate and select the "login" keychain (NOT iCloud).
   - Click "Add".
5. **Set Certificate Trust Settings**:
   - In Keychain Access, find the installed certificate (e.g., `ca.securus-software.com`).
   - Double-click it and expand the "Trust" section.
   - Set "When using this certificate" to "Always Trust".
   - Enter your admin password to confirm.
   - Repeat for both "System" and "login" keychains.
6. **Restart your browser** to apply changes.

---

## ⚠️ **Troubleshooting**:

- If your internet connection stops working, **forget the Wi-Fi network** and reconnect.

---

❗ **Disclaimer**:  
DMCA requests can be sent to [temrage@cumallover.me](mailto:temrage@cumallover.me). They will be publicly posted here and **ignored** since the certificate here is a public key that anyone can access.
