# New Device/SSL Inspection

SSL inspection is a "man-in-the-middle" (MitM) attack, where a network device intercepts and decrypts your encrypted internet traffic. It’s bad for your privacy but there is no way to bypass it unless you use a vpn. The follwoing guide will only show you how to install a ssl certificate to ingore and bypass the annoying "Your connection is not secure." warning

- How it works:
    - **Intercept Traffic:** The network device steps in between your computer and the website you’re visiting.
    - **Decrypt Data:** It decrypts (or unlocks) the encrypted data to look for anything harmful or suspicious.
    - **Inspect Data:** The device checks the decrypted data for security threats or policy violations.
    - **Re-encrypt and Forward:** After inspection, the device re-encrypts (or locks) the data and sends it to the website, and vice versa.
- **Why a Certificate is Needed:**
    
    When SSL inspection is enabled, the network device essentially acts as a "man-in-the-middle" between the user's device and the website. Without proper handling, this can trigger security warnings on the user's device, such as "Your connection is not secure." This happens because the browser detects that the certificate presented by the network device is not the original certificate from the website.
    
    To avoid these warnings, the network device generates its own SSL/TLS certificate and presents it to the user's device.
    

<aside>
❗ If you have a new device and you want to connect to the school network follow this guide.

</aside>

<aside>
❗ Before you start make sure to delete all exististing certificates as they might be expired and could cause conflict.

</aside>

Here is the lastest certificate:

[files.catbox.moe](https://files.catbox.moe/r1wphc.crt)

# **Windows**

1. Download the lastest certificate from your school
2. **Open the Certificate:**
    - Double-click the certificate file to open it.
3. **Install the Certificate:**
    - Click on the "Install Certificate" button.
    - Choose to install the certificate for the "Current User"
4. **Choose Store Location:**
    - Select "Place all certificates in the following store."
    - Click "Browse" and choose "Trusted Root Certification Authorities."
    - Click "Next" and then "Finish."
5. **Enable the Certificate:**
    - Search for “Manager user certificates” in taskbar
    - In the Certificate Manager, navigate to "Trusted Root Certification” - “Certificates”
    - Double-click on the certificate (ca.securus-software.com)
    - Click on the details tab and edit properties
    - Choose enable all purposes for this certificate and apply
6. Restart your browser and clear cache 
    
    
    # iOS
    
    1. Download the latest certificate from your school
    2. **Install the Certificate:**
        - iOS will prompt you to install a new profile.
        - Go to Settings and tap on "Profile Downloaded".
        - Tap "Install" in the top corner.
        - If prompted, enter your device passcode.
    3. **Trust the Certificate:**
        - Go to "Settings" > "General" > "About" > "Certificate Trust Settings".
        - Toggle the switch next to the certificate to enable full trust for the root certificate.

# macOS

1. Download the latest certificate from your school
2. **Install the Certificate:**
    - Open the Certificate:
    - Double-click the certificate file. It should open in the Keychain Access application.
    - Add the Certificate to Keychain:
    - In Keychain Access, you will be asked where to add the certificate.
    - Select "System" and "login" keychain NOT ICLOUD
    - Click "Add."
    - Open the certificate again
    - Double-click the certificate file. It should open in the Keychain Access application.
    - Add the Certificate to Keychain:
    - In Keychain Access, you will be asked where to add the certificate.
    - Select "login" keychain NOT ICLOUD
    - Click "Add."
3. Set Certificate Trust Settings:
    - In Keychain Access, find the installed certificate under the "Certificates" category.  (ca.securus-software.com)
    - Double-click the certificate.
    - Expand the "Trust" section.
    - Set "When using this certificate" to "Always Trust."
    - Close the window, and you'll be prompted to enter your administrator password to apply the changes.
    - This must be done for both certificate installed at “System” and “login”
4. Restart the Browser:
    - Restart your browser to apply the changes.

<aside>
❗ If your internet stops working, forget the wifi and reconnect
If you are getting a https error (your connection is not private), delete the old ssl certificate and reinstall the latest [ssl certificate issued by your school](https://files.catbox.moe/r1wphc.crt)

</aside>