# 🛠️ Firewall Configuration Documentation

<div align="center">

[🏠 Portfolio Home](../README.md)

</div>

---

## 💻 Server Security Commands

### 1. Command Used to Allow SSH
To ensure remote administrative management remains accessible after activating the firewall, SSH traffic was explicitly allowed:
```bash
sudo ufw allow ssh
