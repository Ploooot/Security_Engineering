### Week 4

## Task 1 : Side-channels

<b> Brief explanation of what side-channel the attack uses and how</b>

A side-channel attack is a form of security breach that focuses on exploiting data revealed by accident  by a system's physical characteristics, such as its power usage, electromagnetic emissions, timing, or other unintended channels. These attacks use the fact that a system's physical implementation often unintentionally discloses information about the data it is handling.
The essence of side-channel attacks lies in their capacity to exploit unintentional data leaks stemming from the physical implementation of a system. To protect themselves, companies take preventive measures, including the use of constant-time algorithms, hardware safeguards, and techniques like introducing noise, all aimed at minimizing the exposure of sensitive information through side-channels.

<b> What systems does it affect?</b>

This kind of attack can affects Cryptographic Sys, Smart Cards, Embedded Sys, Hardware Security Modules, Mobile Devices, Cloud Servers, Banking Sys, Defense Sys, High-Performance Computing Sys and Automotive Electronics.

<b>What information is leaked via the side channel?</b>

Cryptographic Keys can be leaked via Power Consumption or Electromagnetic Radiation by analyzing variations in power consumption during cryptographic operations for example. You can also know keyboard input by capture and analyzing sound patterns to infer keystrokes or data input on a keyboard.

<b>Is there a documented case of it being used in a real life attack?</b>

Computer scientists have devised an attack that reliably extracts secret cryptographic keys by capturing the high-pitched sounds coming from a computer while it displays an encrypted message.
They demonstrated “the attack on various targets and by various methods, including the internal microphone of a plain mobile phone placed next to the computer and using a sensitive microphone from a distance of four meters”.

https://arstechnica.com/information-technology/2013/12/new-attack-steals-e-mail-decryption-keys-by-capturing-computer-sounds/

<b>Has it been fixed? If yes, how it was fixed?</b>

“The technique has its limitations. Most obviously, the attackers must have a smartphone, bug, or other microphone-enabled device in close proximity to a computer at the precise moment it's decrypting a message that was sent by, or otherwise known to, the attackers. Still, the technique represents a solid advance in the field of cryptanalytic side-channel attacks, which target cryptographic implementations that leak secret information through power consumption, electromagnetic emanations, timing differences, or other indirect channels.”

https://arstechnica.com/information-technology/2013/12/new-attack-steals-e-mail-decryption-keys-by-capturing-computer-sounds/

Task2: Slow Loris

<b>How does it work?</b>

The principle of the Slow Loris is to send partial HTTP requests via a script, at regular intervals, in order to keep the sockets open. Slowloris therefore initiates a GET request to the target server, there is an exchange between the two entities, as any HTTP client would do to the server, but here slowloris will ensure that the exchange never ends. Slowloris will not send the sequences expected by the server but will from time to time provide it with a bogus header which will be ignored by the server, but which will keep the TCP connection open, thus preventing the socket from being closed. The server quickly becomes saturated, resulting in denial of service. 

https://fr.wikipedia.org/wiki/Slowloris

<b> Why is it unique while compared to the other high bandwith DDoS attacks?</b>

The main difference is that  Slowloris tries to maintain its connections for as long as possible. It prevents the server from freeing up resources and serving legitimate users by keeping connections open. The longer the connections are maintained, the more effective the attack becomes.

<b> What are the effects of the attack?</b>

The first issue with this attack is that it prevent any user to connect to a server because the limit has already been reach by fake user which never disconnect with the Slow Loris attack. For all the user currently connected, they suffer huge latency because of the amount of connected devices. If the website is an online business, it can directly affect sells of the compagnies meaning a lose of money for it.

<b>How can you mitigate/prevent the effects of the attack?</b>

You can configure your web server to limit the number of concurrent connections from a single IP address. By setting a connection limit, you can reduce the impact of Slowloris attacks. You also can disconnect a user after a certain amount of time without activity for him. You can do penetration testing and security assessments of your web applications to identify and address vulnerabilities that could be exploited in Slowloris attacks.

<b>Are there any notable instances of this style of attack being performed?</b>

As Ars reported last week, memcached, a database caching system for speeding up websites and networks, lets DDoS vandals amplify their attacks by an unprecedented factor of 51,000. That means a single home computer with a 100 megabit-per-second upload capacity from its ISP is capable of bombarding a target with a once-unimaginable 5 terabits per second of traffic, at least in theory.

Following the discovery that DDoS vandals in the wild were abusing open memcached servers, researchers last week predicted a new round of record attacks. Two days later, DDoS mitigation service Akamai/Prolexic reported the 1.3Tbps attack against Github, just slightly topping previous records set in 2016.

https://arstechnica.com/information-technology/2018/03/us-service-provider-survives-the-biggest-recorded-ddos-in-history/
 
## Task 3: BurpSuite Introduction
# Subtask 1: Intercepting (0.25p)

After the connection, we can see an alert message telling us to change the password because it has been detected during a data breach.

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/b257fd4e-791b-42fd-87ee-e1d80075155b)

After few interaction with the login page, we can see them on Burp Suite : 

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/fb7121ca-c4e8-4fcf-9eb2-9d9e71a4f2ed)

Original Request : 

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/9613cbfc-cd74-4051-ae5d-a8ef235df65d)


Edited Request : 

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/b69cf892-869b-424d-9306-179dc7783f9b)


Last POST request : 
 
![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/e8ba415b-1112-44ce-b7fd-f99d25fdec6d)

Last GET request : 

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/bb6fd0d3-5582-460a-adc2-c10b57fceb0c)
 
# Subtask 2: Repeater (0.25p)

The value of the svwaSession increment itself with the time : each second, the value up by 1.

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/8196950c-2d72-4c25-a2e1-c8d4fd21d93a)

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/e777db70-3643-43f5-9159-5ab20aae90f2)

It seems that the Cookie is generated for every request. Every time the request is executed, the new cookie replace the last one giving it an ID/dvwaSession relative to the current time.

 
# Subtask 3: Intruder (0.25p)

Modification of the request with the intruder :

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/d3646cd9-62a0-4c0b-bf86-bb6275123354)

It seems that all the attempts worked. All tries ended up with a status code 200 OK meaning that the request has succeeded. (1st line of the raw)

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/49949219-6202-4b92-af43-5670e92c68c7)
 
# Subtask 4: Decoder (0.25p)

Here is the encoding of my personal data and how it comes back to the original text : 

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/5e01955a-8750-475a-b9f3-f0b425d9c5ca)

# Subtask 5: thc-hydra (1p)

New password has been found : 

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/94c51c55-2d2d-4b58-9910-e28045fa444d)

Now we try to find the time we need to find a 4 letters password.
We use this command : docker run --network="host" vanhauser/hydra -V -f -I -l admin -x 1:4:a "http-get-form://localhost/vulnerabilities/brute/:username=^USER^&password=^PASS^&Login=Login:H=Cookie:PHPSESSID=pe0ee9lggovv3d4pjp835ns174;security=low:F=Username and/or password incorrect."
The operation started at 11:27:11

![Screenshot_20231006_142729_Gallery](https://github.com/Ploooot/Security_Engineering/assets/121863850/d84cdae2-ba4b-4a0a-8fa7-cf2b7459ee9b)

It ended at 11:37:31

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/b531a486-6fee-4371-a8e1-1f3a99af8796)

This program took 10 minutes and 20 secondes and 45468 attempts to find the password.
