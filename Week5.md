### Task2: Slow Loris

<b>Spectre v1</b>

Spectre v1 is a type of speculative execution attack that exploits a fundamental feature of modern microprocessors to access sensitive information. It targets systems with out-of-order execution capabilities, which includes a wide range of modern CPUs.
The attack leverages the speculative execution process, where the CPU predicts and pre-executes instructions to optimize performance. Spectre v1 tricks the CPU into speculatively executing malicious code that can leak sensitive data like passwords or encryption keys. By inducing a misprediction in the CPU's branch prediction unit, an attacker can infer the contents of memory that should be inaccessible.
Mitigation for Spectre v1 involves software-level solutions as recompiling applications with specialized compiler flags or applying microcode updates provided by CPU manufacturers. These measures help to prevent speculative execution of malicious code sequences.

<b>Bounds Check Bypass (RIDL)</b>

Bounds Check Bypass is a microarchitectural data sampling attack that targets systems using Intel processors. It exploits the interaction between the CPU's microarchitectural components, such as the Load Port, Store Buffer, and Memory Ordering Buffer, to leak sensitive data.
In a RIDL attack, an attacker manipulates these components to retrieve data from memory that they shouldn't have access to. This data could include passwords or cryptographic keys. RIDL is a variant of the larger class of microarchitectural data sampling attacks, which includes MDS (Microarchitectural Data Sampling) and Fallout.
Mitigating RIDL involves a combination of microcode updates from Intel and operating system patches. These updates help prevent the unintended leakage of data through these microarchitectural components.

<b>Microarchitectural Load Port Data Sampling (MLPDS) and Branch History Injection (BHI)</b>

Microarchitectural Load Port Data Sampling (MLPDS) and Branch History Injection (BHI) are two speculative execution attacks that target similar systems as Spectre and Meltdown attacks, primarily Intel processors.
MLPDS focuses on exploiting the Load Port to sample data, similar to RIDL. BHI, on the other hand, leverages the CPU's branch prediction mechanisms to carry out speculative execution of malicious code, potentially revealing sensitive information.
Mitigation for MLPDS and BHI includes a combination of microcode updates, operating system patches, and software-specific measures. These updates and patches help to reduce the risk of speculative execution attacks and protect sensitive data.
In summary, these three attacks, Spectre v1, RIDL, MLPDS, and BHI, all exploit microarchitectural vulnerabilities in modern CPUs to access sensitive information. Each has its unique way of compromising data security, but they commonly target systems with speculative execution capabilities. Mitigation strategies primarily involve a combination of microcode updates, operating system patches, and software-level measures to minimize the risk of exploitation and protect against data leakage. 

### Task 3: BurpSuite Introduction

<b>Malware and Viruses</b>

Harm: Malware and viruses can wreak havoc on your system, causing data loss, compromising privacy, and making your computer a tool for cybercriminals.

Windows Mitigation: Windows includes security tools, Windows Defender, to detect and remove malware. Keeping your operating system updated, enabling the built-in firewall, and practicing safe online habits are essential precautions.

<b>Exploiting Software Vulnerabilities</b>

Harm: Exploiting software vulnerabilities can open the door to unauthorized access, data breaches, and system instability.

Windows Mitigation: To address this risk, regularly update Windows to patch known vulnerabilities. Windows Security Center is a built-in tool for managing security settings.

<b>Phishing and Social Engineering</b>

Harm: Phishing and social engineering attacks aim to deceive you into revealing sensitive information, potentially leading to identity theft, financial fraud, or unauthorized account access.

Windows Mitigation: Windows offers security features like Windows Defender SmartScreen to help identify and block malicious websites. Educating people about phishing is crucial in protecting against these threats.

<b>Drive-by Downloads</b>

Harm: Drive-by downloads can surreptitiously install malicious software on your computer, causing system compromise and data loss.

Windows Mitigation: Employ a secure browser with built-in security features, and configure browser settings for enhanced protection. Windows Defender can also help prevent drive-by downloads.

<b>Zero-Day Exploits</b>

Harm: Zero-day exploits target undiscovered vulnerabilities in your OS or software, posing a serious risk due to the absence of immediate patches.

Windows Mitigation: Staying vigilant with regular OS and software updates is vital to safeguard against these threats. Microsoft actively releases patches for zero-day vulnerabilities as they emerge.

<b>USB/Removable Media Attacks</b>

Harm: Malicious USB drives can introduce malware, steal data, and disrupt your system. They can also facilitate the spread of infections across networks.

Windows Mitigation: You can disable Windows' AutoPlay and Autorun features to prevent automatic code execution from USB drives. Employing reliable antivirus software to scan and block malicious files is an effective countermeasure.

<b>Password Cracking</b>

Harm: Password cracking poses a significant risk by potentially granting unauthorized access to your accounts, leading to privacy breaches and identity theft.

Windows Mitigation: Create strong, unique passwords, and take advantage of Windows' account lockout policies and support for multi-factor authentication. Utilizing password managers is a valuable step to fortify your security.
 
### Task4: Logging

Different types of log files typically store different kinds of information, depending on the purpose they serve within a system. Here's a general idea of what kind of information would be saved into each type of log file:

<b>Application logs</b>

We can find in application logs information related to the functioning of a specific application but also errors, warnings, and debugging information. The app store user activities or transactions within the application. It can also store performance metrics of the application, such as response times or resource usage.

https://www.crowdstrike.com/cybersecurity-101/observability/application-log/

<b>Event logs</b>

Event logs can store records of significant events or occurrences within a system but also records of system shutdowns, restarts, or critical system events. If someone try to login, the log file can contain information about user logins, logouts, or failed login attempts. 

https://www.crowdstrike.com/cybersecurity-101/observability/event-log/

<b>Service logs</b>

Just like for the others kind of logs, service logs can store information related to the performance and behavior of specific services running on a system and status updates, errors, and warnings specific to the services. To solve issues, it can store records of service start-ups, shutdowns, or failures.

https://docs.oracle.com/en-us/iaas/Content/General/Concepts/service_logs.htm

<b>System logs</b>

Syslog store : information about the overall functioning and health of the operating system; records of hardware events, such as hardware failures, disk errors, or network issues; system-level error messages, warnings, and critical alerts; information about resource usage, including CPU usage, memory usage, and disk usage; records of system-level processes, tasks, or background operations.

https://www.techopedia.com/definition/1858/system-log-syslog

Specific information stored in each type of log file can vary based on the configuration and settings of the system, application, or service generating the logs. The format and structure of log files can vary depending on the logging mechanism used and the specific needs of the system administrators.

In windows, application logs are stored in <b>%AppData%</b>; event logs are stored in <b>%SystemRoot%\System32\Winevt\Logs</b>; service logs are stored in <b>%SystemRoot%\System32\LogFiles</b> and system logs are stored in <b>%SystemRoot%\System32\Config</b>.

<b>Application logs</b>

Monitoring application logs helps detect unusual user activities, errors that may signal security vulnerabilities, and performance issues, all of which could indicate a security threat.

<b>Event logs</b>

Watching event logs enables the identification of irregular login patterns, unexpected system shutdowns or restarts, and security-related events, such as policy modifications or unauthorized access attempts.

<b>Service logs</b>

Keeping an eye on service logs allows for the detection of service disruptions, irregular network traffic patterns, and errors indicating potential unauthorized access attempts or configuration changes.

<b>System logs</b>

Monitoring system logs helps in recognizing hardware errors impacting system stability, abnormal resource usage suggesting malicious activity, and security events such as unauthorized system modifications or suspicious processes.

I can use my operating system's built-in log management tools, such as Event Viewer or System Log Viewer, to check for any issues or irregular activities.

I can make sure that logging is enabled for all critical components and services on my computer, allowing me to capture necessary information.

I can make it a habit to regularly review logs for any potential security threats or system errors that might require my attention.

I can install reputable antivirus and anti-malware software and keep it updated to detect and prevent security threats effectively.

I can make sure to keep my operating system and software updated to benefit from the latest security patches, reducing the risk of potential vulnerabilities.
