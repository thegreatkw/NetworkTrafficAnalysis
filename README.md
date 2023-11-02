<h1>Network Traffic Analysis Project</h1></br>

<h2>Description</h2>

• Examinied network traffic to characterize common ports and protocols utilized, establish a baseline for a given environment, monitor and respond to threats, and ensure the greatest possible insight into an organization's network.</br>

<h2>Utilities</h2>

• Wireshark</br>
• tcpdump</br>

<h2>Steps</h2>

<i>• <b>1.</b> Reviewed everyday use cases of network traffic analysis and common traffic analysis tools:</i></br>

![image](https://github.com/thegreatkw/NetworkTrafficAnalysis/assets/128569887/bef836d1-5f41-4bf0-a0b4-4b9938b4ed7f)
![image](https://github.com/thegreatkw/NetworkTrafficAnalysis/assets/128569887/641523c5-2b19-4772-a7a9-8c6d7cb007f2)

<i>• <b>2.</b> Became familiar with network traffic analysis workflow:</i></br>
<i></br>
  <b>Ingest Traffic</b></br>
  Once we have decided on our placement, begin capturing traffic. Utilize capture filters if we already have an idea of what we are looking for.
  
  <b>Reduce Noise by Filtering</b></br>
  Capturing traffic of a link, especially one in a production environment, can be extremely noisy. Once we complete the initial capture, an attempt to filter out unnecessary traffic from our view can make analysis easier. (Broadcast and Multicast traffic, for example.)
  
  <b>Analyze and Explore</b></br>
  Now is the time to start carving out data pertinent to the issue we are chasing down. Look at specific hosts, protocols, even things as specific as flags set in the TCP header. The following questions will help us:
  
      Is the traffic encrypted or plain text? Should it be?
      
      Can we see users attempting to access resources to which they should not have access?
      
      Are different hosts talking to each other that typically do not?
  
  <b>Detect the Root Issue</b></br>
  
      Are we seeing any errors? Is a device not responding that should be?
      
      Use our analysis to decide if what we see is benign or potentially malicious.
      
      Other tools like IDS and IPS can come in handy at this point. They can run heuristics and signatures against the traffic to determine if anything within is potentially malicious.
      
  </i></br>

![image](https://github.com/thegreatkw/NetworkTrafficAnalysis/assets/128569887/33a36578-bec4-43d2-9c05-b2072e9e9ff4)

</br>
<i>• <b>3.</b> Learned tcpdump fundamentals and practiced with filters.</i></br></br>


![image](https://github.com/thegreatkw/NetworkTrafficAnalysis/assets/128569887/b874eb04-3480-4767-93c8-1f43e3183bd7)
![image](https://github.com/thegreatkw/NetworkTrafficAnalysis/assets/128569887/935f75d6-c4a4-456f-aca4-361a254368a9)
![image](https://github.com/thegreatkw/NetworkTrafficAnalysis/assets/128569887/d00421a9-7817-4a00-877d-2584f5779943)

<i>• <b>4.</b> Examined Wireshark output and dissected the GUI view.</i></br>

![image](https://github.com/thegreatkw/NetworkTrafficAnalysis/assets/128569887/69389f53-d75b-4823-bccb-ef00f6436701)

<i>
<b>Three Main Panes:</b> (See Figure above)</br>
</br>
Packet List: Orange</br></br>

In this window, we see a summary line of each packet that includes the fields listed below by default. We can add or remove columns to change what information is presented.
Number- Order the packet arrived in Wireshark
Time- Unix time format
Source- Source IP
Destination- Destination IP
Protocol- The protocol used (TCP, UDP, DNS, ECT.)
Information- Information about the packet. This field can vary based on the type of protocol used within. It will show, for example, what type of query It is for a DNS packet.

Packet Details: Blue</br>

The Packet Details window allows us to drill down into the packet to inspect the protocols with greater detail. It will break it down into chunks that we would expect following the typical OSI Model reference. the packet is dissected into different encapsulation layers for inspection.
Keep in mind, Wireshark will show this encapsulation in reverse order with lower layer encapsulation at the top of the window and higher levels at the bottom.

Packet Bytes: Green</br>

The Packet Bytes window allows us to look at the packet contents in ASCII or hex output. As we select a field from the windows above, it will be highlighted in the Packet Bytes window and show us where that bit or byte falls within the overall packet.
This is a great way to validate that what we see in the Details pane is accurate and the interpretation Wireshark made matches the packet output.
Each line in the output contains the data offset, sixteen hexadecimal bytes, and sixteen ASCII bytes. Non-printable bytes are replaced with a period in the ASCII format.
</i>











