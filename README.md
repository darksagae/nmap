# nmap
**Nmap** (Network Mapper) is a powerful open-source tool used for network discovery and security auditing. It is included in Kali Linux and is widely used by security professionals to scan networks, identify active devices, and discover open ports and services.

### Installation

Nmap is pre-installed on Kali Linux. If you need to install it, you can use:

```bash
sudo apt-get install nmap
```

### Basic Usage

The basic syntax for using Nmap is:

```bash
nmap [options] <target>
```

Here, `<target>` can be an IP address, hostname, or network range.

### Common Options and Examples

1. **Basic Scan**:
   To perform a simple scan on a single IP address:

   ```bash
   nmap 192.168.1.1
   ```

   **Expected Output**:
   ```
   Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-26 12:00 UTC
   Nmap scan report for 192.168.1.1
   Host is up (0.0030s latency).
   Not shown: 996 filtered ports
   PORT     STATE SERVICE
   22/tcp open  ssh
   80/tcp open  http
   ```

2. **Scanning a Range of IP Addresses**:
   To scan a range, for example, from 192.168.1.1 to 192.168.1.254:

   ```bash
   nmap 192.168.1.1-254
   ```

   **Expected Output**:
   ```
   Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-26 12:05 UTC
   Nmap scan report for 192.168.1.1
   Host is up (0.0031s latency).
   PORT     STATE SERVICE
   22/tcp open  ssh
   80/tcp open  http

   Nmap scan report for 192.168.1.10
   Host is up (0.0040s latency).
   PORT     STATE SERVICE
   22/tcp open  ssh
   ```

3. **Service Version Detection**:
   To identify services and their versions running on open ports:

   ```bash
   nmap -sV 192.168.1.1
   ```

   **Expected Output**:
   ```
   Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-26 12:10 UTC
   Nmap scan report for 192.168.1.1
   PORT     STATE SERVICE VERSION
   22/tcp open  ssh     OpenSSH 7.6p1 Ubuntu 4 (Ubuntu Linux)
   80/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
   ```

4. **Operating System Detection**:
   To attempt to determine the operating system of the target:

   ```bash
   nmap -O 192.168.1.1
   ```

   **Expected Output**:
   ```
   Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-26 12:15 UTC
   Nmap scan report for 192.168.1.1
   Host is up (0.0030s latency).
   Not shown: 996 filtered ports
   OS details: Linux 4.15 - 5.4
   ```

5. **Aggressive Scan**:
   For a more comprehensive scan that includes OS detection, version detection, script scanning, and traceroute:

   ```bash
   nmap -A 192.168.1.1
   ```

   **Expected Output**:
   ```
   Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-26 12:20 UTC
   Nmap scan report for 192.168.1.1
   PORT     STATE SERVICE VERSION
   22/tcp open  ssh     OpenSSH 7.6p1 Ubuntu 4 (Ubuntu Linux)
   80/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
   MAC Address: 00:11:22:33:44:55 (Example Corp)
   ```

### Conclusion

Nmap is a versatile and essential tool for network scanning and security assessments. By utilizing its various options, you can gather detailed information about networks and devices, making it invaluable for penetration testers and network administrators.



                                    ALTERNATIVE
### Nmap: A Kali Linux Tool

**Nmap** (Network Mapper) is a powerful open-source tool used for network discovery and security auditing. It is commonly included in Kali Linux and is essential for penetration testing.

### Installation

Nmap is usually pre-installed on Kali Linux. If it's not, you can install it with:

```bash
sudo apt-get install nmap
```

### Basic Usage

The basic syntax for using Nmap is:

```bash
nmap [options] <target>
```

Here, `<target>` can be an IP address, hostname, or a range of IPs.

### Common Options and Examples

1. **Basic Scan**:
   To perform a basic scan on a single IP address:

   ```bash
   nmap 192.168.1.1
   ```

   **Expected Output**:
   ```
   Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-26 12:00 UTC
   Nmap scan report for 192.168.1.1
   Host is up (0.0010s latency).
   Not shown: 995 closed ports
   PORT     STATE SERVICE
   22/tcp open  ssh
   80/tcp open  http
   ```

2. **Scanning a Range of IP Addresses**:
   To scan a range of IP addresses:

   ```bash
   nmap 192.168.1.1-254
   ```

   **Expected Output**:
   ```
   Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-26 12:00 UTC
   Nmap scan report for 192.168.1.1
   Host is up (0.0020s latency).
   PORT     STATE SERVICE
   22/tcp open  ssh
   80/tcp open  http

   Nmap scan report for 192.168.1.10
   Host is up (0.0025s latency).
   PORT     STATE SERVICE
   443/tcp open  https
   ```

3. **Service Version Detection**:
   To detect service versions running on open ports:

   ```bash
   nmap -sV 192.168.1.1
   ```

   **Expected Output**:
   ```
   PORT     STATE SERVICE VERSION
   22/tcp open  ssh     OpenSSH 7.9
   80/tcp open  http    Apache 2.4.38 (Debian)
   ```

4. **Operating System Detection**:
   To attempt to determine the operating system of a target:

   ```bash
   nmap -O 192.168.1.1
   ```

   **Expected Output**:
   ```
   Device type: general purpose
   Running: Linux 3.10 - 4.9
   OS details: Linux 3.10 - 4.9
   ```

5. **Aggressive Scan**:
   For a more detailed scan that includes OS detection, version detection, script scanning, and traceroute:

   ```bash
   nmap -A 192.168.1.1
   ```

   **Expected Output**:
   ```
   Starting Nmap 7.80 ( https://nmap.org ) at 2023-02-26 12:00 UTC
   Nmap scan report for 192.168.1.1
   Host is up (0.0010s latency).
   Not shown: 995 closed ports
   PORT     STATE SERVICE VERSION
   22/tcp open  ssh     OpenSSH 7.9
   80/tcp open  http    Apache 2.4.38 (Debian)
   OS details: Linux 3.10 - 4.9
   ```

### Conclusion

Nmap is a versatile and essential tool for network scanning and security assessment. Its various options allow users to customize scans to gather detailed information about networked devices. Always ensure you have permission to scan networks or devices to avoid legal issues.




                                      ALTERNATIVE
Nmap is a powerful network scanning and discovery tool included in Kali Linux. Here's an overview of how it's used, along with examples and output:

**What is Nmap?**
Nmap (Network Mapper) is a free and open-source utility for network exploration and security auditing. It's used to discover hosts and services on a computer network, create a map of the network, and gather information about the targets, including open ports, operating systems, and versions of services.

**Basic Usage:**
The basic syntax for using Nmap is:
```
nmap <target>
```
Here, `<target>` can be an IP address, a hostname, or a network range.

**Examples:**

1. **Basic Scan:**
To perform a basic scan on a single IP address:
```
nmap 192.168.1.1
```
This will scan the target host and provide information about open ports, services, and operating system.

2. **Scan a Range of IP Addresses:**
To scan a range of IP addresses, for example, 192.168.1.1 to 192.168.1.254:
```
nmap 192.168.1.1-254
```
This will scan all IP addresses in the specified range and provide a comprehensive report.

3. **OS Detection:**
To detect the operating system of a target host:
```
nmap -O 192.168.1.1
```
This will provide information about the operating system, including version and architecture.

4. **Port Scanning:**
To scan for open ports on a target host:
```
nmap -p 1-100 192.168.1.1
```
This will scan the first 100 ports on the target host and report any open ports.

**Output:**
The output of Nmap will vary depending on the target system's configuration and the options used. Here's an example output:
```
Nmap scan report for 192.168.1.1
Host is up (0.00035s latency).
Not shown: 998 closed ports
PORT      STATE SERVICE
22/tcp    open  ssh
80/tcp    open  http
111/tcp   open  rpcbind
139/tcp   open  netbios-ssn
445/tcp   open  microsoft-ds

OS detection:
  OS: Linux 3.10 - 3.14
  Device type: general purpose
  Running: Linux 3.X|4.X
```
This output provides information about open ports, operating system, and device type.

Remember to use Nmap responsibly and ethically, as it can be used to gather sensitive information about target systems. Always ensure you have permission to scan a target network or IP address.



                                    ALTERNATIVE
Certainly, I'd be happy to provide information about the Nmap tool in Kali Linux.

Nmap (Network Mapper) is a powerful open-source tool used for network discovery and security auditing. It's one of the most widely used security tools in the Kali Linux distribution.

**Basic Usage**
The basic syntax for using Nmap is:

```
nmap [Scan Type] [Options] [Target]
```

Here, `[Scan Type]` specifies the type of scan to perform, `[Options]` allows you to customize the scan, and `[Target]` is the IP address, hostname, or network range you want to scan.

**Examples and Expected Output**

1. **Basic TCP Scan**:
   To perform a basic TCP port scan on a single IP address:

   ```
   nmap 192.168.1.100
   ```

   **Expected Output:**
   ```
   Starting Nmap scan on 192.168.1.100
   Nmap scan report for 192.168.1.100
   Port     State Service
   22/tcp   open  ssh
   80/tcp   open  http
   443/tcp  open  https
   ```

   This output shows that the host at 192.168.1.100 has three open ports: 22 (SSH), 80 (HTTP), and 443 (HTTPS).

2. **Scan a Range of IP Addresses**:
   To scan a range of IP addresses, for example, 192.168.1.1 to 192.168.1.254:

   ```
   nmap 192.168.1.1-254
   ```

   **Expected Output:**
   ```
   Starting Nmap scan on 192.168.1.1-254
   Nmap scan report for 192.168.1.5
   Port     State Service
   22/tcp   open  ssh
   80/tcp   open  http
   Nmap scan report for 192.168.1.10
   Port     State Service
   135/tcp  open  msrpc
   139/tcp  open  netbios-ssn
   ```

   This will scan the entire 192.168.1.0/24 network range and report on the open ports for each discovered host.

3. **SYN Stealth Scan**:
   To perform a stealthy SYN scan, which is less likely to be detected by firewalls:

   ```
   nmap -sS 192.168.1.100
   ```

   **Expected Output:**
   ```
   Starting Nmap SYN Stealth Scan on 192.168.1.100
   Nmap scan report for 192.168.1.100
   Port     State Service
   22/tcp   open  ssh
   80/tcp   open  http
   ```

   The `-sS` option tells Nmap to use the SYN scan technique, which is more stealthy than a regular TCP connect scan.

4. **OS Detection**:
   To try to determine the operating system of a target host:

   ```
   nmap -O 192.168.1.100
   ```

   **Expected Output:**
   ```
   Starting Nmap OS detection on 192.168.1.100
   Nmap scan report for 192.168.1.100
   OS: Linux 3.2 - 4.9
   ```

   The `-O` option enables Nmap's OS detection feature, which tries to identify the operating system of the target based on various fingerprinting techniques.

Nmap is a versatile and powerful tool that can be used for a wide range of network reconnaissance and security testing tasks. The examples provided here demonstrate some of the basic usage scenarios, but Nmap offers many more advanced features and options to explore.




                                      ALTERNATIVE
Nmap (Network Mapper) is a versatile and widely used network scanning tool in Kali Linux. It's used for discovering hosts and services on a computer network by sending packets and analyzing the responses. Nmap can determine various characteristics of a network, such as what hosts are available, what services they offer, what operating systems they run, what type of packet filters/firewalls are in use, and many other details.

### Basic Usage

The basic syntax for using Nmap is:

```bash
nmap [scan type(s)] [options] {target specification}
```

Here, the target specification can be a single IP address, hostname, network, or a list of targets.

### Common Options and Examples

1.  **Basic Scan**:

    *   To perform a basic scan on a single IP address:

    ```bash
    nmap 192.168.1.1
    ```

    *   **Expected Output:**

    ```
    Starting Nmap 7.92 ( https://nmap.org ) at 2025-02-26 04:42 UTC
    Nmap scan report for 192.168.1.1
    Host is up (0.0013s latency).
    Not shown: 997 closed ports
    PORT    STATE SERVICE
    22/tcp  open  ssh
    80/tcp  open  http
    443/tcp open  https

    Nmap done: 1 IP address (1 host up) scanned in 0.23 seconds
    ```

    This output shows the open ports (22, 80, 443) and the services running on the target IP.

2.  **Scanning a Range of IP Addresses**:

    *   To scan a range of IP addresses, for example, 192.168.1.1 to 192.168.1.254:

    ```bash
    nmap 192.168.1.1-254
    ```

    This will scan all IP addresses in the specified range and report any open ports and services found.

3.  **Operating System Detection**:

    *   To detect the operating system of the target, use the `-O` option:

    ```bash
    nmap -O 192.168.1.1
    ```

    *   **Expected Output:**

    ```
    Starting Nmap 7.92 ( https://nmap.org ) at 2025-02-26 04:42 UTC
    Nmap scan report for 192.168.1.1
    Host is up (0.00098s latency).
    Not shown: 997 closed ports
    PORT    STATE SERVICE
    22/tcp  open  ssh
    80/tcp  open  http
    443/tcp open  https
    Device type: general purpose
    Running: Linux 3.X|4.X
    OS CPE: cpe:/o:linux:linux_kernel:3 cpe:/o:linux:linux_kernel:4
    OS details: Linux 3.10 - 4.11

    Nmap done: 1 IP address (1 host up) scanned in 5.48 seconds
    ```

    This output attempts to determine the OS running on the target (in this case, a Linux kernel version 3.10 - 4.11).

4.  **Service Version Detection**:

    *   To determine the version of services running on the target, use the `-sV` option:

    ```bash
    nmap -sV 192.168.1.1
    ```

    *   **Expected Output:**

    ```
    Starting Nmap 7.92 ( https://nmap.org ) at 2025-02-26 04:42 UTC
    Nmap scan report for 192.168.1.1
    Host is up (0.00079s latency).
    Not shown: 997 closed ports
    PORT    STATE SERVICE VERSION
    22/tcp  open  ssh     OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (protocol 2.0)
    80/tcp  open  http    Apache httpd 2.4.29 ((Ubuntu))
    443/tcp open  ssl/http Apache httpd 2.4.29 ((Ubuntu))

    Nmap done: 1 IP address (1 host up) scanned in 7.28 seconds
    ```

    This output shows the specific versions of the services running on the open ports (e.g., OpenSSH 7.6p1, Apache httpd 2.4.29).

5.  **Aggressive Scan**:

    *   To enable aggressive scanning (includes OS detection, version detection, script scanning, and traceroute), use the `-A` option:

    ```bash
    nmap -A 192.168.1.1
    ```

    This will perform a comprehensive scan, providing as much information as possible about the target.

6.  **TCP Connect Scan**:

    *   To perform a TCP connect scan, use the `-sT` option. This is a basic and reliable scan type that establishes a full TCP connection:

    ```bash
    nmap -sT 192.168.1.1
    ```

7.  **SYN Scan (Stealth Scan)**:

    *   To perform a SYN scan (also known as a half-open scan), use the `-sS` option. This is a stealthier scan that doesn't complete the TCP connection:

    ```bash
    nmap -sS 192.168.1.1
    ```

8.  **UDP Scan**:

    *   To scan for open UDP ports, use the `-sU` option:

    ```bash
    nmap -sU 192.168.1.1
    ```

9.  **Saving Results to a File**:

    *   To save the output to a file, use the `-oN` (normal output), `-oG` (grepable output), or `-oX` (XML output) options:

    ```bash
    nmap -oN output.txt 192.168.1.1
    ```

    This will save the scan results in a normal format to `output.txt`.

### Important Notes

*   Ensure you have permission to scan a target network or IP address. Unauthorized scanning can be illegal.
*   Nmap is a powerful tool that can be used to identify potential vulnerabilities, so use it responsibly and ethically.
*   The output may vary depending on the target system's configuration and the options used.



                                              ALTERNATIVE
  Nmap (Network Mapper) is a powerful open-source tool included in Kali Linux, widely used for network discovery and security auditing. It allows users to discover hosts and services on a computer network by sending packets and analyzing the responses. Here’s how to use Nmap effectively, along with examples and expected output.

### Basic Usage

To use Nmap, you typically run it from the command line. The basic syntax is:

```bash
nmap [options] [target]
```

### Common Commands and Examples

1. **Scanning a Single Host**:
   To perform a default scan on a single IP address:
   ```bash
   nmap 192.168.1.1
   ```
   **Expected Output**:
   ```
   Starting Nmap 7.80 ( https://nmap.org ) at 2025-02-26 12:00 UTC
   Nmap scan report for 192.168.1.1
   Host is up (0.0010s latency).
   Not shown: 999 closed ports
   PORT     STATE SERVICE
   22/tcp open  ssh
   80/tcp open  http
   ```

2. **Scanning a Range of IP Addresses**:
   To scan a range of IP addresses:
   ```bash
   nmap 192.168.1.1-10
   ```
   **Expected Output**:
   ```
   Starting Nmap 7.80 ( https://nmap.org ) at 2025-02-26 12:05 UTC
   Nmap scan report for 192.168.1.1
   Host is up (0.0010s latency).
   PORT     STATE SERVICE
   22/tcp open  ssh
   80/tcp open  http

   Nmap scan report for 192.168.1.2
   Host is up (0.0010s latency).
   PORT     STATE SERVICE
   22/tcp open  ssh
   ```

3. **Aggressive Scan**:
   To perform an aggressive scan that includes OS detection, version detection, and script scanning:
   ```bash
   nmap -A 192.168.1.1
   ```
   **Expected Output**:
   ```
   Starting Nmap 7.80 ( https://nmap.org ) at 2025-02-26 12:10 UTC
   Nmap scan report for 192.168.1.1
   Host is up (0.0010s latency).
   Not shown: 999 closed ports
   PORT     STATE SERVICE VERSION
   22/tcp open  ssh     OpenSSH 7.6 (protocol 2.0)
   80/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
   ```

4. **Service Version Detection**:
   To detect versions of services running on open ports:
   ```bash
   nmap -sV 192.168.1.1
   ```
   **Expected Output**:
   ```
   Starting Nmap 7.80 ( https://nmap.org ) at 2025-02-26 12:15 UTC
   Nmap scan report for 192.168.1.1
   Host is up (0.0010s latency).
   PORT     STATE SERVICE VERSION
   22/tcp open  ssh     OpenSSH 7.6 (protocol 2.0)
   80/tcp open  http    Apache httpd 2.4.29 ((Ubuntu))
   ```

5. **Saving Scan Results**:
   To save the scan results in different formats:
   ```bash
   nmap -oA scan_results 192.168.1.1
   ```
   This command saves the output in three formats: normal, XML, and grepable.

### Conclusion

Nmap is an essential tool for network scanning and security assessments. Its versatility allows users to perform a wide range of scans, from simple host discovery to detailed service enumeration and vulnerability detection. By mastering Nmap, security professionals can gain valuable insights into network security.

---
Learn more:
1. [nmap | Kali Linux Tools](https://www.kali.org/tools/nmap/)
2. [A Guide to Using Nmap on Kali Linux | by Bukola Obialom | Medium](https://medium.com/@bukkyobialom/a-guide-to-using-nmap-on-kali-linux-c0e6894834a8)
3. [How to Use Nmap in Kali Linux](https://www.linkedin.com/pulse/how-use-nmap-kali-linux-indian-cyber-security-solutions-uq5if)
