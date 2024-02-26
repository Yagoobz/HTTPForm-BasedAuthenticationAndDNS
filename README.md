<h2>HTTP Form-Based Authentication and DNS</h2>

<h3>Objectives</h3>
- Develop and implement a Wireshark capture filter to target HTTP traffic on port 80.
<br />
- Analyze differences in HTTP traffic encodings to assess authentication security.
<br />
- Evaluate the encryption status of DNS traffic captured on port 53 for potential vulnerabilities.
<br />
- Explore strategies to mitigate risks associated with unencrypted DNS traffic and enhance overall network security.

<h3>Step 1: Configuring Wireshark Capture Filter and Generating HTTP Traffic</h3>
I configured Wireshark to capture traffic specifically from HTTP by setting the capture filter to port 80. Next, I navigated to an insecure HTTP website named 'testing-ground' and proceeded to input a username and password in order to generate traffic.
<br />
<img src="https://github.com/Yagoobz/HTTPForm-BasedAuthenticationAndDNS/assets/145611184/c6fe3d57-440b-40eb-968b-8ebe9e04bcab" height="30%" width="70%" alt="Disk Sanitization Steps"/>

<h3>Step 2: Observing Differences in HTTP Traffic Encodings</h3>
Unlike the last http traffic I captured in Wireshark from the previous lab that was displayed in the Hypertext Transfer Protocol, this time it is showing up in the HTML Form URL Encoded in clear text form. Form-based authentication lacks obfuscation, making it less secure than basic authentication. However, it was designed with HTTPS in mind, negating the need for additional encoding or obfuscation. Nonetheless, it's crucial not to input sensitive data on non-HTTPS websites, as everything is transmitted in clear text, exposing it to potential snoopers.
<br />
<img src="https://github.com/Yagoobz/HTTPForm-BasedAuthenticationAndDNS/assets/145611184/cb5281e3-fcd5-42a7-9e12-dae7333114e4" height="30%" width="70%" alt="Disk Sanitization Steps"/>

<h3>Step 3: Capturing DNS Traffic and Analyzing Encryption</h3>
Now, I'm focusing on capturing DNS traffic. I configured Wireshark's capture filter to port 53 and proceeded to open the Windows Command Prompt. From there, I pinged a website. Upon analysis, it became evident that the DNS traffic is unencrypted, as I could clearly observe the application data and identify the server the virtual machine I'm using needs to resolve the IP for. Had the traffic been encrypted, such detailed information would not have been visible.
<br />
<img src="https://github.com/Yagoobz/HTTPForm-BasedAuthenticationAndDNS/assets/145611184/b674cb19-8470-4066-a6ad-bdd0a216edb1" height="30%" width="70%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/Yagoobz/HTTPForm-BasedAuthenticationAndDNS/assets/145611184/2c81f5c3-5eda-42a0-a2db-68c553913dd5" height="30%" width="70%" alt="Disk Sanitization Steps"/>
