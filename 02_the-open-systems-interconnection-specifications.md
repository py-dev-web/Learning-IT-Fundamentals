# The Open Systems Interconnection Specifications

## 🌐 Internetworking Models

### 📦 The Layered Approach
- A **reference model** is a conceptual blueprint for how communication should occur.
- It divides communication tasks into **logical layers**, similar to departments in a company.
- Each layer handles specific responsibilities and relies on other layers to perform their tasks.
- Developers can focus on building protocols for a **single layer** without worrying about others — this is called **binding**.

### ✅ Advantages of Reference Models
- Simplifies **network design and troubleshooting**.
- Enables **multi-vendor interoperability** through standard components.
- Promotes **industry standardization**.
- Allows diverse hardware and software to **communicate smoothly**.
- Isolates changes within layers, easing **application development**.

---

## 🧱 The OSI Reference Model
The **OSI (Open Systems Interconnection)** model helps systems of different types (Windows, Linux, Mac) communicate. It provides a 7-layer framework:

1. **Application (Layer 7)** – User interface & application services  
2. **Presentation (Layer 6)** – Data formatting, encryption, compression  
3. **Session (Layer 5)** – Session setup and control  
4. **Transport (Layer 4)** – End-to-end connections and reliability  
5. **Network (Layer 3)** – Logical addressing & routing  
6. **Data Link (Layer 2)** – Framing and MAC addressing  
7. **Physical (Layer 1)** – Transmission of raw bits over media

#### 🔁 Mnemonic:
**A**ll **P**eople **S**eem **T**o **N**eed **D**ata **P**rocessing.(top to bottom)  


### 🔼 Upper Layers (7–5)
- **Application** – Provides user interface  
- **Presentation** – Formats and encrypts data  
- **Session** – Manages sessions between applications  

### 🔽 Lower Layers (4–1)
- **Transport** – Ensures reliable/unreliable delivery  
- **Network** – Provides logical addressing for routing  
- **Data Link** – Combines bits into frames, error detection  
- **Physical** – Moves bits, defines voltage, cables, pinouts

---

### 🧑‍💻 Layer 7 – Application Layer

The **Application Layer** is the **topmost layer** of the OSI model and enables direct **user interaction with network services**.

#### 🧠 Key Responsibilities:
- Provides access to **network services** via applications.
- Identifies and establishes **communication partners**.
- Ensures **sufficient system resources** are available.
- Manages **data integrity** and **error recovery** procedures.

#### 🔁 Typical Operations:
- Viewing a website in a browser (**HTTP**).
- Sending/receiving emails (**SMTP, POP3, IMAP**).
- Downloading files (**FTP, TFTP**).
- Accessing web domains (**DNS**).

#### 🛠️ Common Protocols:
- **HTTP/HTTPS** – Web browsing
- **FTP/TFTP** – File transfers
- **SMTP/IMAP/POP3** – Email services
- **DNS** – Domain name resolution

#### 🖥️ Real-World Examples:
- Using **Google Chrome** to visit a website.
- Sending an email via **Microsoft Outlook**.
- Uploading files to a cloud service like **Dropbox**.
- Accessing a document from **Google Drive**.

---

### 🖼️ Layer 6 – Presentation Layer

The **Presentation Layer** is responsible for **translating, encrypting, and formatting** data for the Application Layer.

#### 🧠 Key Responsibilities:
- **Data translation** (e.g., EBCDIC ↔ ASCII).
- **Data formatting** into standard structures.
- **Encryption/Decryption** for secure communication.
- **Compression/Decompression** to reduce data size.

#### 🔁 Typical Operations:
- Converting character encoding (e.g., Unicode).
- Securing HTTPS data with SSL/TLS.
- Streaming multimedia with compression.
- Displaying images in standard formats.

#### 🛠️ Common Protocols/Formats:
- **SSL/TLS** – Secure sessions
- **JPEG, MPEG, GIF** – Media formats
- **ASCII, EBCDIC** – Text encoding

#### 🖥️ Real-World Examples:
- Viewing a **YouTube** video (compression & streaming).
- Accessing a **secure website** via HTTPS (TLS encryption).
- Opening a **.jpg or .png** file in an image viewer.
- Running a video conference with **Zoom** (format + encryption).

---

### 💬 Layer 5 – Session Layer

The **Session Layer** manages and controls **dialogues (sessions)** between two communicating devices.

#### 🧠 Key Responsibilities:
- **Session establishment**, maintenance, and termination.
- **Dialog control** using:
  - Simplex: One-way only  
  - Half Duplex: Two-way, one at a time  
  - Full Duplex: Two-way, simultaneous  
- **Session recovery** after interruptions.

#### 🔁 Typical Operations:
- Managing multiple browser tabs.
- Handling VoIP and video calls.
- Resuming file transfers.
- Controlling remote sessions.

#### 🛠️ Common Protocols:
- **NetBIOS**
- **RPC (Remote Procedure Call)**
- **SQL Sessions**
- **NFS (Network File System)**

#### 🖥️ Real-World Examples:
- Running **multiple Zoom meetings** simultaneously.
- Opening several **browser tabs** in **Firefox** or **Edge**.
- Using **Remote Desktop Protocol (RDP)** to control another PC.
- Maintaining a connection in **online banking** apps.

---

### 🚚 Layer 4 – Transport Layer


The **Transport Layer** provides **end-to-end communication** and ensures **reliable or fast delivery** of data between devices.

#### 🧠 Key Responsibilities:
- **Segmentation & reassembly** of data.
- **Connection control**:
  - Connection-oriented (reliable) – e.g., **TCP**  
  - Connectionless (unreliable) – e.g., **UDP**
- **Flow control** to avoid overwhelming the receiver.
- **Error detection and correction**.

#### 🔁 Typical Operations:
- Establishing a TCP session between two hosts.
- Sending a quick DNS query over UDP.
- Retransmitting lost packets in reliable connections.

#### 🛠️ Common Protocols:

| Protocol | Type              | Description                                 |
|----------|-------------------|---------------------------------------------|
| **TCP**  | Connection-oriented | Reliable, ordered delivery (e.g., HTTP, FTP) |
| **UDP**  | Connectionless     | Fast, minimal overhead (e.g., DNS, VoIP)     |

#### 🖥️ Real-World Examples:
- Browsing a website (**TCP/HTTP**).
- Watching a live stream (**UDP/RTP**).
- Playing an online game (**UDP**).
- Downloading a file using **FTP** or **HTTP**.



#### 🔄 Connection-Oriented Communication (TCP)

In connection-oriented communication, a **virtual circuit** is established **before** any actual data is transferred. This ensures **reliable, ordered, and error-checked communication** between two hosts.

The most common protocol for connection-oriented communication is **TCP (Transmission Control Protocol)**.


##### 📦 Key Characteristics:

- 🔗 **Connection Establishment**: A session is created **before** sending data.
- ✅ **Reliability**: Ensures that all packets are received in order and without errors.
- 📤 **Acknowledgments**: Sent for received segments to confirm delivery.
- 🔁 **Flow Control**: Manages how much data is sent at a time to avoid overwhelming the receiver.
- 🚫 **Congestion Handling**: Detects and adjusts data transmission during network congestion.


##### 🔧 Three-Way Handshake: Step-by-Step

The **3-way handshake** is used by TCP to establish a reliable connection between a client and a server.

##### 📘 Steps:

```
1. Client → Server: SYN
   - Client sends a SYN (synchronize) packet to initiate a connection.

2. Server → Client: SYN-ACK
   - Server responds with SYN-ACK (synchronize-acknowledge) to acknowledge the request.

3. Client → Server: ACK
   - Client sends back an ACK, confirming the connection.
```

✅ Now the connection is established, and data transfer can begin.


##### 🔄 Visual Representation (Text Diagram)

```
CLIENT                              SERVER
  |                                   |
  | ----------- SYN ----------------> |
  |                                   |
  | <--------- SYN + ACK ------------ |
  |                                   |
  | ----------- ACK ----------------> |
  |                                   |
  |      ✅ Connection Established     |
```


##### 📉 Congestion Analogy: Traffic Jam

Imagine a **high-speed sports car** (a fast sender) trying to merge into a **narrow city street** (a slower network or server). If too many cars (packets) try to merge at once, it causes a **traffic jam** (network congestion). 

This is why TCP:
- Limits the amount of unacknowledged data in flight.
- Adjusts transmission speed dynamically using **flow and congestion control algorithms**.



#### 🚦 Flow Control: Managing Data Speed

Flow control allows the **receiver** to **govern the pace** at which the **sender** transmits data to **avoid buffer overflow** and **data loss**.

##### 🧠 Why It’s Needed

If the sender is too fast and the receiver can't keep up:
- The receiver stores extra data in a **buffer** (temporary memory).
- If the buffer **overflows**, new data is **discarded**.

##### 🧊 The Stoplight Analogy

> Flow control works like a traffic light at a narrow bridge:

| State        | Meaning                          |
|--------------|----------------------------------|
| 🔴 Not Ready | Receiver buffer full, pause data |
| 🟢 Ready     | Buffer cleared, resume sending   |


##### 🧪 What Happens Internally?

```
SENDER                                RECEIVER
  |                                       |
  | ------- Segment 1 ------------------>|
  | ------- Segment 2 ------------------>|
  |                                       |
  | <--- Buffer Full! "Not Ready" -------|
  | ------ (Sender pauses transmission)  |
  |                                       |
  | <--- Buffer Cleared! "Ready" --------|
  | ------- Segment 3 ------------------>|
```


##### 🔁 Reliable Communication Process

Connection-oriented transmission ensures:

1. 📬 **Acknowledgment of received segments**
2. 🔁 **Retransmission** of unacknowledged segments
3. 🔢 **Sequencing** to preserve order
4. 🧠 **Flow control** to avoid congestion and data loss


##### 🚨 Example: When Things Go Wrong

Imagine a high-speed server sending massive data to a slower client:

- ✅ Small bursts: Handled by buffer.
- 🚨 Continuous flood: Buffer overflows.
- ❌ Receiver discards excess packets.
- 🚦 Transport issues a “not ready” signal.
- ✅ After processing, receiver sends a “ready” signal.

##### 🧾 Summary Table: Connection-Oriented Service Traits

| Trait                 | Description                                    |
|-----------------------|------------------------------------------------|
| 🔁 Virtual Circuit     | Established before data transmission           |
| 🔢 Sequencing          | Maintains correct segment order                |
| ✅ Acknowledgments     | Confirms receipt of data                       |
| 🚦 Flow Control        | Prevents buffer overflows and congestion       |



> **Flow control** ensures that the communication remains smooth, reliable, and congestion-free — a core part of what makes TCP and other connection-oriented protocols dependable.





#### 🪟 Windowing

**Windowing** is a fundamental mechanism in the Transport Layer—especially within **TCP/IP**—that ensures **efficient and controlled data transmission** between devices.

##### 🎯 What Is Windowing?

> **Windowing** defines how much data (in bytes) a sender can transmit before needing an acknowledgment from the receiver.

Without windowing, the sender would have to:
- 🕐 Wait after each segment
- ⌛ Experience reduced efficiency

But with windowing:
- 📦 Multiple segments can be sent in a row
- 🔁 Acknowledgments can be processed in bulk
- ⚡ Throughput is improved!


##### 📏 How Window Size Works

The **window size** determines how many **bytes** (or segments, conceptually) can be sent **before requiring an acknowledgment**.

| Window Size | Behavior                                                                 |
|-------------|--------------------------------------------------------------------------|
| 1           | Sends 1 segment → waits for ACK → sends next segment                     |
| 3           | Sends 3 segments → waits for ACK → sends next 3 segments                 |
| Dynamic     | Window size can adjust based on network conditions (used in TCP today)   |

> 📌 **Note**: TCP measures the window in **bytes**, not packets or segments.


##### 🧠 Visual Example

###### 🔹 Window Size = 1

```
SENDER                           RECEIVER
[Segment 1] ----->               [ACK 1] <-----
[Segment 2] ----->               [ACK 2] <-----
```

###### 🔸 Window Size = 3

```
SENDER                           RECEIVER
[Seg 1][Seg 2][Seg 3] ----->     [ACK 3] <-----
[Seg 4][Seg 5][Seg 6] ----->     [ACK 6] <-----
```

Each acknowledgment can confirm multiple segments depending on how much was sent and received successfully.


##### 🧰 Windowing in Real TCP

TCP uses **byte-level sliding windows**. Here's what that means:

- Each ACK shifts the window forward (like sliding a ruler along a line).
- It helps TCP adapt to varying speeds and congestion conditions dynamically.
- If data loss occurs, TCP can **shrink** the window and **retransmit** only the missing bytes.

##### 🚥 Windowing vs Flow Control

While related, they are not the same:

| Concept        | Role                                                                 |
|----------------|----------------------------------------------------------------------|
| **Flow Control** | Prevents the sender from overwhelming the receiver                 |
| **Windowing**    | Specifies how many bytes/segments can be sent before needing an ACK |


🧠 **Key Insight**:  
> **Larger windows = more throughput**, but **riskier** if there's packet loss.  
> **Smaller windows = safer**, but **slower**.





#### 📬 Acknowledgments in Reliable Data Delivery (TCP)

In reliable network communication, **acknowledgments** play a vital role in ensuring that data is:

✅ Received  
✅ In order  
✅ Not duplicated  
✅ Not lost

This is managed through a process called **Positive Acknowledgment with Retransmission (PAR)**.


##### 🔁 How Acknowledgments Work

When a sender transmits a data segment, it:

1. ✅ Records that it sent it.
2. 🕐 Starts a timer.
3. 📥 Waits for an **ACK (acknowledgment)** from the receiver.
4. 🔁 If the timer expires without receiving an ACK, it **retransmits** the segment.


##### 📦 Window Size & Acknowledgment Flow

Let's compare a **window size of 1** vs **window size of 3**.

###### 🪟 Window Size: 1 (Stop-and-Wait)
```
Sender:   Send 1     ⏳ Wait for ACK 1     Send 2     ⏳ Wait for ACK 2
Receiver:       Receive 1 → ACK 1       Receive 2 → ACK 2
```

###### 🪟 Window Size: 3 (Sliding Window)
```
Sender:   Send 1  Send 2  Send 3    ⏳ Wait for ACK 3
Receiver:      Receive 1, 2, 3 → ACK 3
```

> 📘 In TCP, ACKs typically acknowledge **the next byte expected**, not just the last one received.


##### 🧪 Example: Acknowledgment and Retransmission

Imagine segments 1–6 being sent:

```
1️⃣ Send 1, 2, 3  ➡️  Receiver gets them
✅ ACK 4 (next expected segment)

2️⃣ Send 4, 5, 6  ➡️  Segment 5 gets lost
❌ Receiver gets 4 and 6, but not 5
🔁 ACK 5  (asks for 5 again)
3️⃣ Resend 5 ➡️ ACK 7
```

> 🧠 **ACKs indicate the next expected segment**. If one is missing, the receiver keeps acknowledging the last correct segment it got.


##### 🛡️ Why This Matters

This process ensures:

- **Reliability**: Missing segments get retransmitted.
- **Ordering**: Segments are reassembled correctly.
- **No Duplicates**: Each ACK is specific and precise.
- **Congestion Control**: Timers and ACKs help detect problems in transmission.


##### 🎯 TCP vs UDP (Reliable vs Unreliable)

| Feature                     | TCP (Connection-Oriented) | UDP (Connectionless)     |
|----------------------------|----------------------------|---------------------------|
| Acknowledgments            | ✅ Yes                     | ❌ No                      |
| Retransmissions            | ✅ Yes                     | ❌ No                      |
| Data ordering              | ✅ Maintains order         | ❌ Not guaranteed          |
| Overhead                   | ⚠️ Higher                  | ✅ Lower                   |
| Use case                   | Web, Email, File Transfer  | Streaming, VoIP, Gaming   |

> 🧠 If you're using TCP, you're using virtual circuits and reliable delivery.  
> If you're using UDP, you're sending data without guarantees—fast, but risky.


✅ **Acknowledgments ensure reliable data transport** through:
- Positive confirmation of receipt
- Retransmission on loss
- Sequence tracking
- Timer-based error recovery

📌 **In TCP**, if you don’t hear back in time → **resend the data**.  
📌 **In UDP**, there’s **no listening for a reply**—just fire and forget.


---

### 🌐 Layer 3 – Network Layer

The **Network Layer** is responsible for **routing data** between devices across **multiple networks**. It handles **logical addressing**, **packet forwarding**, and **path determination**.

#### 🧠 Key Responsibilities:
- Assigns and manages **logical addresses** (e.g., IP).
- Tracks **device locations** on the network.
- Determines the **best path** for data delivery.
- Provides **packet forwarding and routing** services.
- Handles **packet fragmentation and reassembly** when needed.

#### 🔁 Typical Operations:
- Receiving a packet and checking the **destination IP**.
- Looking up the **routing table** for the best path.
- Sending the packet out via the appropriate **exit interface**.
- Dropping packets if no route is found.

#### 🛠️ Common Protocols:

| Type               | Protocols                                         |
|--------------------|--------------------------------------------------|
| **Routed Protocols**  | IP, IPv6 (used to transport user data)             |
| **Routing Protocols** | RIP, RIPv2, OSPF, EIGRP (used to exchange route info) |

#### 📘 Routing Table Components:
- **Network Address**: Destination network or subnet.
- **Interface**: Outbound port for sending the packet.
- **Metric**: Cost of the path (e.g., hop count, delay, bandwidth).
- **Next Hop**: IP of the next router to forward the packet to.

#### 📌 Additional Functions:
- **Breaks up broadcast and collision domains**.
- **Does not forward broadcast or multicast traffic** by default.
- **Supports Access Control Lists (ACLs)** for packet filtering and security.
- **Connects VLANs** and handles **inter-VLAN routing**.
- Can provide **QoS (Quality of Service)**.

#### 🖥️ Real-World Examples:
- A router sending data from **192.168.1.10** to **8.8.8.8** across the internet.
- Routing VoIP calls through optimized **low-latency paths**.
- Using **ACLs** on a Cisco router to block specific IP traffic.
- Connecting **multiple subnets** in a corporate LAN.
- Running **OSPF** to dynamically update routing tables in a large network.

---

### 🧷 Layer 2 – Data Link Layer

The **Data Link Layer** is responsible for **node-to-node communication** within the same physical network. It ensures **reliable transmission** of data across a physical link by handling **framing, MAC addressing, and error detection**.

#### 🧠 Key Responsibilities:
- **Framing**: Converts data into **frames** for transmission.
- **MAC Addressing**: Uses **hardware (MAC) addresses** to identify devices on a local network.
- **Error Detection**: Detects errors in frames (e.g., using CRC).
- **Flow Control**: Manages data rate to prevent overwhelming the receiving device.
- **Media Access Control**: Determines **when and how** devices access the shared physical medium.

#### 🧩 Sublayers:
| Sublayer | Description |
|----------|-------------|
| **MAC (Media Access Control)** | Controls access to the physical medium. Defines MAC addressing, frame delimiting, and collision handling. |
| **LLC (Logical Link Control)** | Identifies Network layer protocols and encapsulates them. Provides flow control and error notification. |

#### 📌 Functions & Concepts:
- Encapsulates packets from Layer 3 into **frames**.
- Adds **source and destination MAC addresses**.
- Manages **logical topologies** (signal paths on a physical medium).
- Handles **frame synchronization** and **order**.
- Translates Network layer packets for physical transmission.

#### 🛠️ Common Protocols and Standards:
| Protocol / Standard | Description |
|---------------------|-------------|
| **Ethernet (IEEE 802.3)** | Most widely used LAN standard. |
| **Wi-Fi (IEEE 802.11)** | Wireless LAN standard. |
| **PPP (Point-to-Point Protocol)** | Used for direct connections between two nodes. |
| **HDLC** | High-level protocol used on WAN links. |
| **Frame Relay / ATM** | Used in legacy WAN environments. |

#### 🖥️ Real-World Examples:
- A switch forwarding data based on **MAC addresses**.
- A laptop connected to Wi-Fi using **802.11** frame structure.
- Ethernet NIC sending data with a **destination MAC**.
- Frame Check Sequence (FCS) detecting frame errors at the receiver.
- Flow control preventing overflow of buffers in video conferencing.

🎯 **Goal**:  
Provide **reliable and efficient data transfer** across the physical link, ensuring correct delivery between devices on the same LAN segment.

---

### ⚙️ Layer 1 – Physical Layer

The **Physical Layer** is the **foundation of the OSI model**, responsible for **transmitting raw bits** (1s and 0s) over a physical medium between devices. It defines the **electrical, mechanical, and procedural specifications** for activating and deactivating physical links.

#### 🧠 Key Responsibilities:
- **Bit Transmission**: Sends and receives raw binary data (bits).
- **Media Signaling**: Converts digital bits into **electrical, optical, or radio** signals.
- **Interface Standards**: Defines **hardware connectors** and interface types.
- **Topology Definition**: Specifies **physical layouts** like star, bus, ring, or mesh.
- **Synchronization**: Handles **timing of signal transmission and reception**.

#### 🧩 Concepts and Interfaces:
- **DTE (Data Terminal Equipment)** ↔ **DCE (Data Communication Equipment)**  
  ➤ Example: A computer (DTE) connected to a modem or CSU/DSU (DCE).
- **State Transitions**: Changes in signal levels to represent binary values.
- **Encoding Schemes**: Defines how bits are translated into media signals.

#### 📌 Common Standards and Technologies:
| Standard / Technology | Description |
|------------------------|-------------|
| **RJ45, USB, DB9**     | Physical interface connectors |
| **Ethernet (IEEE 802.3)** | Defines wiring, speeds, and signals for LANs |
| **Fiber Optic**        | Uses light for high-speed transmission |
| **DSL, ISDN**          | Used in legacy telephone-based data services |
| **Wi-Fi (IEEE 802.11)**| Wireless physical media standard |
| **Bluetooth, Zigbee**  | Short-range wireless protocols |

#### 🖥️ Real-World Examples:
- An **Ethernet cable** connecting a PC to a switch.
- **Fiber optic cable** transmitting internet signals across long distances.
- **Wi-Fi radio signals** traveling from your router to your phone.
- A technician using a **multimeter** to test electrical signals in copper cables.
- A network interface card (NIC) **blinking LEDs** indicating link and activity.

🎯 **Goal**:  
Enable **physical transmission of binary data** between devices using appropriate signals, media, and interfaces.

---




## 📦 Introduction to Encapsulation in the OSI Model

When data travels from one device to another across a network, it doesn't go as-is — it's **wrapped layer by layer** in what's called **encapsulation**.

🔄 This process adds **Protocol Data Units (PDUs)** at each OSI layer, so devices on each end can understand and interpret the information correctly.


### 📐 What Is Encapsulation?

🧱 **Encapsulation** is the process of:
> Wrapping user data with necessary protocol information **at each layer of the OSI model** so it can be transmitted and understood across a network.

At each layer:
- Data is packaged in a **PDU** (Protocol Data Unit)
- Headers (and sometimes trailers) are added
- Only the **peer layer** on the receiving side understands and interprets this data

### 🔄 Encapsulation Steps (Sender Side)

Here’s how encapsulation works step-by-step as data travels down the OSI layers:

| OSI Layer         | Action                                                                 | PDU Name  | Header Added         |
|------------------|------------------------------------------------------------------------|-----------|-----------------------|
| 🧑‍💻 Application   | User data is generated                                                 | Data      | ❌                    |
| 🎨 Presentation   | Data is formatted (e.g., encryption, compression)                      | Data      | ❌                    |
| 🗂️ Session        | Establishes session and synchronization                                | Data      | ❌                    |
| 🚚 Transport       | Breaks data into segments; adds sequencing and reliability (TCP)       | Segment   | **TCP/UDP Header**    |
| 🌐 Network         | Adds IP addressing and routes data                                     | Packet    | **IP Header**         |
| 📡 Data Link       | Prepares data for local delivery; adds MAC addressing + error checking| Frame     | **MAC + LLC Headers** |
| ⚡ Physical        | Converts frames into binary (bits) and sends via media                 | Bits      | ❌ (Electrical signal) |

---

### 🖼️ Visual Diagram

```
Application Data
   ↓
[ Transport Layer ]
   ➤ TCP Header + Data = Segment
   ↓
[ Network Layer ]
   ➤ IP Header + Segment = Packet
   ↓
[ Data Link Layer ]
   ➤ MAC/LLC Header + Packet + Trailer (FCS) = Frame
   ↓
[ Physical Layer ]
   ➤ Frame → 01010101010101... = Bits
```

🧾 **Final Transmission**:  
🔹 Bits (like `010101011010...`) are sent over the physical medium (cables, wireless, fiber, etc.)



### 🧪 Example

Let’s say a user sends a message "Hello":

1. **Application Layer**: Data = `"Hello"`
2. **Transport Layer**: Adds TCP Header → `Segment`
3. **Network Layer**: Adds IP Header → `Packet`
4. **Data Link Layer**: Adds MAC Header + Trailer (FCS) → `Frame`
5. **Physical Layer**: Converts `Frame` into Bits → sent via cable/wireless

---

