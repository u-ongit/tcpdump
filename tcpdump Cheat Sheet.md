## Tcpdump Cheat Sheet

Tcpdump is a robust command-line packet analyzer. This cheat sheet provides a handy reference for frequently used commands and options. Feel free to bookmark this or even contribute with your own findings!

### **Basic Commands**

**1. Capture packets from a specific interface:**
```bash
sudo tcpdump -i eth0
```

**2. Capture a limited number of packets:**
```bash
sudo tcpdump -c 10
```

**3. Display available interfaces:**
```bash
sudo tcpdump -D
```

**4. Write captured packets to a file:**
```bash
sudo tcpdump -w output.pcap
```

**5. Read packets from a file:**
```bash
sudo tcpdump -r output.pcap
```

### **Filtering Options**

**6. Filter by source or destination IP:**
```bash
sudo tcpdump src 192.168.1.100
sudo tcpdump dst 192.168.1.101
```

**7. Filter by port:**
```bash
sudo tcpdump port 80
```

**8. Filter by protocol:**
```bash
sudo tcpdump icmp
```

**9. Combine multiple conditions:**
```bash
sudo tcpdump src 192.168.1.100 and port 80
```

### **Output Customization**

**10. Display packet contents in ASCII:**
```bash
sudo tcpdump -A
```

**11. Display packet contents in HEX and ASCII:**
```bash
sudo tcpdump -XX
```

**12. Increase verbosity:**
```bash
sudo tcpdump -v
sudo tcpdump -vv
sudo tcpdump -vvv
```

### **Advanced Usage**

**13. Filter by packet length:**
```bash
sudo tcpdump len < 60
```

**14. Capture packets without DNS resolution:**
```bash
sudo tcpdump -n
```

**15. Filter TCP traffic by flags (e.g., SYN, FIN):**
```bash
sudo tcpdump 'tcp[13] & 2 != 0'  # SYN
sudo tcpdump 'tcp[13] & 1 != 0'  # FIN
```

### **Miscellaneous**

**16. Display tcpdump version:**
```bash
tcpdump -version
```

**17. View detailed help:**
```bash
tcpdump -h
```

---

This cheat sheet is designed to get you up and running with tcpdump quickly. 

Feel free to contribute to this cheat sheet with additional commands or corrections. Pull requests and issues are always welcome!

**Note**: Always ensure you have the right permissions to capture network traffic and be mindful of privacy and legal concerns when using and sharing packet captures.
