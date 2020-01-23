# CVE-2017-8759-Exploit-sample
Running CVE-2017-8759 exploit sample.



Flow of the exploit:

Word macro runs in the Doc1.doc file. The macro downloads a badly formatted txt file over wsdl, which triggers the WSDL parser log. Then the parsing log results in running mshta.exe which in turn runs a powershell commands that runs mspaint.exe



To test:

Run a webserver on port 8080, and put the files exploit.txt and cmd.hta on its root. For example python3 -m http.server -127.0.0.1 8080
Or you can use python3 server.py

If all is good mspaint should run.

Mohammed Aldoub @Voulnet

## References:

https://www.fireeye.com/blog/threat-research/2017/09/zero-day-used-to-distribute-finspy.html

