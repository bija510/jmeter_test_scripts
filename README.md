# Apache JMeter Setup and Installation

## Installation Steps
1. Download JMeter from the official website: [JMeter Download](https://jmeter.apache.org/download_jmeter.cgi)
2. Navigate to `Binaries` and download `Apache-jmeter-5.6.3.zip sha512pgp`
3. Extract the downloaded ZIP file to a preferred location
4. Open the extracted folder: `apache-jmeter-5.6.3\bin\`
5. Locate `ApacheJMeter.jar`, right-click, and send a shortcut to the desktop

---

## How to Record a Test Case in JMeter

### JMeter Settings
1. Open JMeter
2. Navigate to **Test Plan** → Right-click → **Add** → **Non-Test Elements** → **HTTPS Test Script Recorder**
3. Set **Target Controller** to: `Test Plan > HTTP(S) Test Script Recorder`
4. Under **Request Filtering**, click **Add Suggested Excludes**

---

## Firefox Browser Configuration

1. Launch **Firefox Browser**
2. Navigate to **Burger Menu** → **Settings** → **General** → Scroll to **Network Settings** → Click **Settings**
3. Configure the proxy settings:
   - Select **Manual Proxy Configuration**
   - **HTTP Proxy:** `127.0.0.1`
   - **Port:** `8888`
   - Enable **Also use this proxy for HTTPS**
   - **HTTPS Proxy:** `127.0.0.1`
   - **SOCKS Host:** `127.0.0.1`
4. When JMeter starts browser recording, this configuration allows it to work; otherwise, it will show an error: `The proxy server is refusing connection`


### Important:
- Start the browser recording in JMeter; otherwise, it will show an error: *"The proxy server is refusing connection"*

---

## Certificate Configuration for Recording

1. HTTPS websites require a certificate for trusted recording
2. Click on the **JMeter Start Record** (Green Triangle) → JMeter will generate a certificate (`ApacheJMeterTemporaryRootCA.crt`)
3. The certificate will be valid for 7 days and is stored in the `bin` folder
4. To import the certificate in Firefox:
   - Open **Firefox Settings** → Search for **Certificate** → Click **View Certificates**
   - Navigate to **Authorities** → Click **Import**
   - Select the generated certificate from `bin` (`ApacheJMeterTemporaryRootCA.crt`)

---

## Recording the First Test Case

1. Click **Record** in JMeter and keep the **Recorder Transaction Control** on the side
2. Open **Firefox** and navigate to [BlazeDemo](https://www.blazedemo.com) (a dummy website for testing)
3. Perform a few interactions (clicks, navigation, etc.)
4. JMeter will capture unnecessary requests; remove unwanted ones

---

## Recording in Chrome with BlazeMeter Extension

BlazeMeter allows recording without proxy settings in Firefox.

### Steps:
1. Download the BlazeMeter extension for Chrome:
   [BlazeMeter Chrome Extension](https://chromewebstore.google.com/detail/blazemeter-the-continuous/mbopgmdnpcbohhpnfglgohlbhfongabi)
2. Use the extension to record browser interactions

---

### ✅ All settings are now configured for JMeter Recording!
