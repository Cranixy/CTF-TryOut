# Shush Protocol (ICS Challenge)

**Points:** 900  
**Difficulty:** Very Easy  
**Category:** ICS Challenges  

---

## Challenge description

The crew sets their sights on an abandoned fertilizer plant, a desolate structure rumored to hold a cache of ammonium nitrate—crucial for their makeshift explosives. Navigating through the plant’s crumbling corridors, they reach the main control room where a dusty, outdated PLC still hums faintly with power.

The crew’s hackers spring into action, connecting their equipment to the network of the PLC and starting the process of extracting data. They know that finding the password the control device uses to connect to the PLC is key to gaining full access to it. The hackers deploy network enumeration tools to scan for active devices on the plant’s internal network. They meticulously sift through IP addresses, looking for clues that might reveal the password.

After several tense hours, they pinpoint the device—a ruggedized industrial computer buried under layers of dust, still linked to the PLC that performs certain diagnostic operations under a custom protocol on a specific interval. Having captured the traffic from that connection the only thing that remains is to locate the packet that contains the secret information.

File provided: `ics_shush_protocol.zip` (original) / `traffic.pcapng` (extracted)

---

## Steps I took

1. Opened the `traffic.pcapng` file in Wireshark.  
2. Pressed **Ctrl + F**, selected **String**, searched inside **Packet bytes**.  
3. Looked for the keyword `HTB`.  
4. Wireshark jumped directly to the packet where the flag was visible in the ASCII pane.

---

## Screenshot

![Wireshark view](wireshark.png)

---

## Flag
HTB{50m371m35_cu570m_p2070c01_423_n07_3n0u9h7}

