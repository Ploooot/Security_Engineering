#Answer, week 2
---
## Task 1A, Browsers and Banking Security

<b>What does the "Not Secure" warning mean in the first picture and what risks does visiting sites with the warning pose?</b>

The “Not Secure” warning means that the connection between the web browser and the site isn’t crypted so it might be not secure. Most of the time, it’s because the website doesn’t use HTTPS protocol.
By visiting not secure website, you take the risk to let someone intercept data between the website and you navigator. 

<b>Why does the second site show up as "trusted" to the browser?</b>

It means that the connection is crypted so the website is more or less safe.

<b>What other ways are there to detect a phishing/scam site? Are there any tools available online?</b>

We can look at the domain extension, if it is suspicious we should avoid to stay on this website. We can also use some tools as Google Safe Browsing. This kind of extension can warn us is we are visiting a website suspicious. 
The best thing is still to not go on a website coming from a link which we can not trust for sure.

<b>What is typosquatting and how does it relate to the pictures?</b>

Typosquatting is a cyberattack which consist of changing a small thing in a URL so the user thinks he is on the website he wants to but he is actually on a false one. If we look at the picture, we can see that the Not Secure website has a ‘k’ at the end of URL which is not suppose to be there and which indicate that it is not the true website. 

<b>What is UDRP and how does it help with combatting typosquatting?</b>

UDRP is a process which help legits domain owners to take legal action against fake owner website such as the one created with typosquatting. 

<b>If you were to own the domain ouspg.org and would be running your crypto banking application at bank.ouspg.org, what domains could you monitor for warning signs of possible phishing attempts against your customers?</b>

It would be good to look for website using a Cyrillic "а" instead of a Latin "a." We could also check for the domain extension because a user could trust a website with .net or .com as extension.

## Task 2: Cards and Payments

<b>Questions: Payments
Why do modern payment cards use a chip and not a magnetic stripe?</b>

Chip and PIN technology makes it much harder for fraudsters to use a found card, inasmuch as if someone steals a card, they are unable to make fraudulent purchases unless they know the PIN. Before that, someone could just steel a card and use it right after in an ATM to get money from the victim.

<b>What are EMV Certificates and why are they relevant for payment protection?</b>

EMV Certificate Authority is the only one which can create a key to associate to a card. When someone wants to use his card, the terminal will first check is the key has been given to someone/ if it exists. If so, it will then ask the bank to get the money. But if one of the steps aren’t check, the person won’t be able to use the card preventing creation of fake card all around the world.  

<b>What attacks exist against payment cards?
Card-not-present?
Contactless payment?</b>

A lot of attacks exist for hackers to get payment cards information. One of the most common in Card-not-present attack is phishing. This attack consist in creation a website similar to a real one and in which, for a “good” reason, will ask you to put your bank account information in it. It usually start with an email in which someone will introduce himself as a trust person. 
One of the Contactless payment attack is called Skimming. It is an attack in which the thief use a skimming device to intercept contactless payment data during a payment. It can be used to copy data and do fraudulent transactions.

<b>Questions: MFA
How is multi-factor authentication (MFA) used in banking?</b>

There are three king of factor of authentication : something the user knows, has or is. In banking, the two first are usually the one needed to use their property. The most common example nowadays is the credit card. The user has to own the card and to enter a PIN code to use it. So it uses two different factors. This is still true for ATM but with wireless payment, it tends to no longer be true in few years.

<b>How does multi-factor authentication increase payment security?</b>

Multi-factor authentication could drastically reduce the incidence of online identity theft and other online fraud, because the victim's password would no longer be enough to give a thief permanent access to their information. 

<b>What MFA methods are you using in you daily life?</b>

To use my credit card on my phone I use the property by owning my phone and either my being or my knowledges. Most of the time I use my being because I unlock my credit card with my fingerprint, but when I can’t I use a password which I am the only one to know. 

<b>What attacks exists against different forms of 2FA?
Time-based-one-time-password (TOTP)?</b>

There are 5 kind of Time-based-one-time-password :
-	Phishing Attacks : Attackers try to trick users into entering their TOTP codes into a fraudulent website or application, thinking they are providing it to a legitimate service. Most of the time, the user get a link in an email or a message that redirect to this fake website.
-	Man-in-the-Middle Attacks : In a MitM attack, an attacker intercepts communication between the user and the login system. They capture the TOTP code entered by the user and use it to access the user's account.
-	Code Replay Attacks : If an attacker manages to intercept a TOTP code, they may attempt to reuse it within the time window before it expires. This is why TOTP codes are typically short-lived (e.g., 30 seconds).
-	Brute Force Attacks : While TOTP codes are time-based and change frequently, attackers can still attempt to guess the correct code through brute force. This is more challenging due to the short time window, but it's not impossible. This attacks are weaker against very complexe password (Lower and Uppercase, number, symbole).
-	Devices Compromise : If an attacker gains physical access to the user's device where the TOTP generator app is installed, they could potentially extract the TOTP secret key and generate codes.

<b>Text Message?</b>

We can find almost the same kind of attack with text message. Otherwise, we can add Malware which are more or less easy to put into a phone, permitting the hacker to have access to data from the mobile.


## Task 4 : Subdomain Takeover

### Task 1

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/d0540a51-16cd-4c01-b033-8c171141cf7d)

When we click on Login, function “login()” is executed.

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/4cc0775e-9a26-4751-bbd5-f767568707fb)

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/91ff17f5-913c-4f56-9b76-39b2624ebc7a)

![image](https://github.com/Ploooot/Security_Engineering/assets/121863850/f8f15669-5fe6-4c0b-b6a8-c38f37cb23c6)

This code means that it gets username and the password. Then it create a user with the name and the password. Last part is sending the user to a JSON file to see if it’s in it. If so, sendData() is executed. Else, it only change background of the field in red.

### Task 2

<b>How did you figure out the domain?</b>

The domain is written in URL tab : bank.ouspg.org. 

<b>How can you find out the hosting provider after finding out the domain?</b>

We can use the command nslookup to get information about domain’s hosting provider. In our case, the command would be bank.ouspg.org.localhost. 

## Task 4 : Non-Technical Alternative

### Write further analysis on the effects of PSD2 on payment security for Task 3 (max 250 words)

PSD2, the Payment Services Directive 2, has had a profound impact on bolstering payment security within the European Union. Here are some key effects:
-	<b>Strong Customer Authentication (SCA)</b>: PSD2 mandates SCA, a stringent authentication process that requires at least two of the following: something the user knows (like a PIN), something the user has (like a mobile device), and something the user is (like a fingerprint). This multi-factor authentication significantly enhances transaction security.
-	<b>Dynamic Linking</b>: The directive requires dynamic linking of transaction details (e.g., payment amount and recipient) to the authentication code generated during SCA. This prevents code reuse and enhances security.
-	<b>Consumer Control</b>: PSD2 empowers consumers by allowing them to grant third-party providers (TPPs) access to their account information and payment initiation with explicit consent. This control minimizes unauthorized access risks.
-	<b>Transaction Risk Analysis (TRA)</b>: Low-risk transactions can be exempted from SCA using TRA mechanisms, streamlining payments for trusted users while maintaining security.
-	<b>Stringent Customer Verification</b>: Payment service providers must implement more rigorous customer verification processes, reducing the likelihood of unauthorized access and fraudulent transactions.
-	<b>Enhanced Monitoring and Reporting</b>: Under PSD2, providers must improve their monitoring and reporting capabilities to promptly detect and report fraudulent activities.

In essence, PSD2 has significantly elevated payment security within the EU. By focusing on SCA, dynamic linking, and consumer empowerment, it has fortified payment transactions against fraud and unauthorized access, benefiting both consumers and the financial industry.

### Summarize what is subdomain takeover and what measures can an organization take to protect itself from it (max 250 words)

Subdomain takeover is a vulnerability used by hacker to get information from a user by faking a legit website. It uses a subdomain from a real and honest compagnie by adding extension on the domain. The new subdomain is control by the hacker.

To protect against this kind of attack, organizations can take multiple measures but the most common is using a Security Header. The most famous one is HTTP and is already used by most of the website.

An important thing to do is also to remove a subdomain as soon as it’s no longer used. It permits to not forget a subdomain which someone could attack when we no longer take care of. 

## Feedback

This part was intersting thanks to the docker part. Even if I don't understand all we can do with docker, it seems that it is a powerfull software which permits us to analyse and simulate online server so we can look for vulnerabilities. 
