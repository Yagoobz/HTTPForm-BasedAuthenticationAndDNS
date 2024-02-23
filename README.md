<h2>Exercise 3: HTTP Form-Based Authentication and DNS</h2>

<h3>Objectives</h3>
- ...
<br />
- ...
<br />
- ...
<br />
- ...

<h3>Step 1: Configuring Wireshark Capture Filter and Generating HTTP Traffic</h3>
I configured Wireshark to capture traffic specifically from HTTP by setting the capture filter to port 80. Next, I navigated to an insecure HTTP website named 'testing-ground' and proceeded to input a username and password in order to generate traffic.
<br />
<img src="https://github.com/Yagoobz/HTTPForm-BasedAuthenticationAndDNS/assets/145611184/c6fe3d57-440b-40eb-968b-8ebe9e04bcab" height="30%" width="70%" alt="Disk Sanitization Steps"/>

<h3>Step 2: Observing Differences in HTTP Traffic Encodings</h3>
Unlike the last http traffic I captured in Wireshark from the previous lab that was displayed in the Hypertext Transfer Protocol, this time it is showing up in the HTML Form URL Encoded in clear text form. Form-based authentication lacks obfuscation, making it less secure than basic authentication. However, it was designed with HTTPS in mind, negating the need for additional encoding or obfuscation. Nonetheless, it's crucial not to input sensitive data on non-HTTPS websites, as everything is transmitted in clear text, exposing it to potential snoopers.
<br />
<img src="https://github.com/Yagoobz/HTTPForm-BasedAuthenticationAndDNS/assets/145611184/cb5281e3-fcd5-42a7-9e12-dae7333114e4" height="30%" width="70%" alt="Disk Sanitization Steps"/>

<h3>Step 3: ...</h3>
...
<br />
<img src="..." height="30%" width="70%" alt="Disk Sanitization Steps"/>
