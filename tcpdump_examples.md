## Tcpdump Demos & Use-Cases

Welcome to the Tcpdump Demos & Use-Cases section! Here, you'll find a collection of real-world scenarios where `tcpdump` proves to be an indispensable tool for network analysis. Each demo includes a brief description, steps to execute, and expected outcomes. For some demos, we also provide annotated `.pcap` files for a hands-on experience.

### 1. Basic Traffic Capture

**Scenario**: You want to monitor all incoming and outgoing traffic on your machine for a brief period.

**Steps**:
```bash
sudo tcpdump -i any -c 50 -w basic_traffic.pcap
```

**Outcome**: This command captures 50 packets from any interface and saves them to `basic_traffic.pcap`.

---

### 2. Filtering Traffic by Protocol

**Scenario**: You suspect there's unnecessary ICMP (ping) traffic in your network and want to inspect it.

**Steps**:
```bash
sudo tcpdump -i any -c 30 icmp -w icmp_traffic.pcap
```

**Outcome**: Captures the first 30 ICMP packets and saves them to `icmp_traffic.pcap`.

---

### 3. Monitoring a Specific Port

**Scenario**: You've just deployed a new web service and want to monitor all traffic hitting port 8080.

**Steps**:
```bash
sudo tcpdump -i any port 8080 -c 100 -w port8080_traffic.pcap
```

**Outcome**: Captures 100 packets interacting with port 8080 and saves them to `port8080_traffic.pcap`.

---

### 4. Capturing DNS Queries

**Scenario**: Your DNS seems to be acting up, and you'd like to see if the requests are even leaving your machine.

**Steps**:
```bash
sudo tcpdump -i any -c 50 udp port 53 -w dns_queries.pcap
```

**Outcome**: Captures 50 packets of DNS queries (typically on UDP port 53) and saves them to `dns_queries.pcap`.

---

### 5. Traffic Between Specific Hosts

**Scenario**: You want to analyze the traffic between your machine and a specific IP address, say `192.168.1.105`.

**Steps**:
```bash
sudo tcpdump -i any -c 75 host 192.168.1.105 -w host_traffic.pcap
```

**Outcome**: Captures 75 packets to or from the IP address `192.168.1.105` and saves them to `host_traffic.pcap`.



**Note**: Ensure you have the right permissions to capture network traffic in your environment. Always respect privacy and legal guidelines when handling and sharing `.pcap` files.
