# 🛡️ XSS Filter Bypass Lab with Burp Suite

## 📌 Description

This project simulates a real-world bug bounty scenario where we bypass input filters to trigger **Cross-Site Scripting (XSS)** and use **Burp Suite** to intercept, modify, and resend requests.

---

## 🔧 Tools Used

- 🧰 **Burp Suite Community Edition**
- 🕸️ DVWA (Damn Vulnerable Web App)
- 💻 Kali Linux
- 🌐 Firefox or Chromium

---

## 🧪 Steps Performed

1. **Setup DVWA** on localhost using XAMPP or Docker.
2. **Launched Burp Suite** and configured browser proxy.
3. Intercepted the **reflected XSS request**.
4. Observed **input filtering** like `<script>` being blocked.
5. Tested **filter bypass techniques**:
   - Using `img` tag with `onerror`
   - URL-encoding the payload
   - Breaking out of input sanitization with:
     - Pipes `|`
     - Semicolons `;`
     - Logical AND `&&`
6. Successfully triggered JavaScript alert box.
7. Documented the working payload and the context.

---

## 🔥 Working Payload Example

```html
<img src=x onerror=alert('XSS')>
