# KeyStoned
Key Systems administrator privilege escalation

![alt text](https://github.com/billchaison/KeyStoned/blob/master/ks.png)

The Key Systems network-attached electronic safe allows an administrative user to open the safe and release keys through the web interface.  The device also emits logs containing the web session ID when an administrator successfully logs in.  By monitoring these logs you can manipulate the GET request and gain administrative access.

When you access the landing page of the Key Systems box you are met with a login prompt.

![alt text](https://github.com/billchaison/KeyStoned/blob/master/ks1.png)

Clicking on any of the menu items reveals your current unauthenticated session ID.

![alt text](https://github.com/billchaison/KeyStoned/blob/master/ks2.png)

Using netcat, connect to the Key Systems box on TCP port 1010 and wait for successful administrator access to be logged.  Note the session ID (sid) in the output.  (in this example the sid is 1699452270)

![alt text](https://github.com/billchaison/KeyStoned/blob/master/ks3.png)

Copy this session ID into your browser and resend the request to gain administrative access.

![alt text](https://github.com/billchaison/KeyStoned/blob/master/ks4.png)<br />
![alt text](https://github.com/billchaison/KeyStoned/blob/master/ks5.png)
