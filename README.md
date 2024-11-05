<p align="center">
  <img src="https://i.imgur.com/UypXMEo.gif" width="20%" alt="SCHOOL_SSL_INSPECTION-logo">
</p>
<p align="center">
    <h1 align="center">SCHOOL_SSL_INSPECTION</h1>
</p>
<p align="center">
	<img src="https://img.shields.io/github/license/temrage/school_ssl_inspection?style=flat&logo=opensourceinitiative&logoColor=white&color=0080ff" alt="license">
	<img src="https://img.shields.io/github/last-commit/temrage/school_ssl_inspection?style=flat&logo=git&logoColor=white&color=0080ff" alt="last-commit">
	<img src="https://img.shields.io/github/languages/top/temrage/school_ssl_inspection?style=flat&color=0080ff" alt="repo-top-language">
	<img src="https://img.shields.io/github/languages/count/temrage/school_ssl_inspection?style=flat&color=0080ff" alt="repo-language-count">
  
# 🚨 Connecting to the School Network
The school network has SSL inspection enabled to monitor encrypted traffic and block sites. This can cause security warnings on your device, such as "Your connection is not private," because the network’s SSL certificate is not trusted by default. You cannot bypass ssl inspection when using the school network because it's server sided. (you can use a vpn tho)

❗ **This guide is for:**  
- New device users trying to connect to a school network.
- Anyone receiving HTTPS errors (like "Your connection is not private").
  
⚠️ **Before starting**:  
Make sure to delete all existing certificates to avoid conflicts due to expired certificates!

## 🔑 **Why a Certificate is Needed**:

When SSL inspection is enabled, the network device acts as a MitM between the user and the website. This can trigger security warnings (e.g., "Your connection is not secure") because the certificate presented by the network device isn't the website's original certificate. To avoid these warnings, the school has generated its own SSL/TLS certificate, which you’ll need to install on your device.

📥 **Download the latest certificate here:**  
[ssl.crt](https://github.com/temrage/school_ssl_inspection/releases/download/release/ssl.crt)
This certificate will expire on 15/4/2025, once the school releases a new one it will be updated over here.
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
5. **Set Certificate Trust Settings**:
   - In Keychain Access, find the installed certificate (e.g., `ca.securus-software.com`).
   - Double-click it and expand the "Trust" section.
   - Set "When using this certificate" to "Always Trust".
   - Enter your admin password to confirm.
6. **Restart your browser**.

---

## ⚠️ **Troubleshooting**:

- If you are still getting the error make sure the certificated you installed is trusted.
- Clear your browser cache or trying using a diffrent browser.

---

❗ **Disclaimer**:  
DMCA requests can be sent to [temrage@cumallover.me](mailto:temrage@cumallover.me). They will be publicly posted here and **ignored** since the certificate here is public which anyone can access. 
