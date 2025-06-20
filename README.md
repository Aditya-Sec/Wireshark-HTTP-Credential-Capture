# Wireshark-HTTP-Credential-Capture
Capture login credentials from an HTTP website using Wireshark packet analyzer.

# 🔍 Wireshark HTTP Credential Capture

This project demonstrates how to use the Wireshark packet analyzer to capture login credentials transmitted over HTTP. It showcases the vulnerability of unencrypted communication and highlights the need for HTTPS in secure data transmission.

---

## 🎯 Objective

Study and use Wireshark to monitor HTTP traffic and extract login credentials from a non-HTTPS web application.

- **Target Website**: [http://testphp.vulnweb.com](http://testphp.vulnweb.com)

---

## 🧰 Tools Used

- **Wireshark**
- **Browser**: Firefox/Chrome
- **OS**: Kali Linux / Windows / Linux (any system with Wireshark)

---

## 🛠️ Methodology

1. Open Wireshark and start packet capture on the active network interface.
2. Visit `http://testphp.vulnweb.com/login.php`.
3. Enter dummy login credentials and submit the form.
4. In Wireshark, apply the filter: `http.request`.
5. Locate the POST request with form data.
6. View the packet details and extract `username` and `password` from the payload.

---

## 📸 Screenshots

> Add these images in a folder called `images/` in your repo and link them.

- **Login Form on Target Site**  
  ![login-form](images/login-form.png)

- **Captured Packet with Credentials**  
  ![wireshark-packet](images/wireshark-packet.png)

---

## 📦 Sample Output

Captured HTTP POST request with plain-text credentials:

POST /userinfo.php HTTP/1.1
Host: testphp.vulnweb.com
username=admin&password=123456


---

## 🎓 Learning Outcome

- Understood how packet sniffing works over unencrypted channels.
- Gained hands-on experience with Wireshark filters.
- Learned about HTTP protocol vulnerability.
- Recognized the importance of secure (HTTPS) communication.

---

## ⚠️ Disclaimer

> This project was conducted only on **legal and intentionally vulnerable** websites for **educational purposes**. Do **not** perform such activities on unauthorized systems.

## 🔗 References

- [Wireshark User Guide](https://www.wireshark.org/docs/wsug_html_chunked/)
- [Acunetix Test Site](http://testphp.vulnweb.com)


