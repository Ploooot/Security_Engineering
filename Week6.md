# Task 1: Secure Running Environment?

## TPM

“The primary scope of TPM (Trusted Platform Module is to ensure the integrity of a platform. In this context, “integrity" means "behave as intended", and a "platform" is any computer device regardless of its operating system. This is to ensure that the boot process starts from a trusted combination of hardware and software, and continues until the operating system has fully booted and applications are running.
When TPM is used, the firmware and the operating system are responsible for ensuring integrity.”

https://en.wikipedia.org/wiki/Trusted_Platform_Module

However, TPM has limitations, such as its inability to protect against attacks targeting the operating system or applications running on the system. It also cannot prevent physical attacks or attacks targeting memory and buses.

## Virtualization

“Hardware virtualization or platform virtualization refers to the creation of a virtual machine that acts like a real computer with an operating system. Software executed on these virtual machines is separated from the underlying hardware resources.”

https://en.wikipedia.org/wiki/Virtualization

I personally had couple of opportunity to use one of theses VM to be able to use some software which could be run only on linux. The virtual machine is like a guest in the physical machine with its own memory and software in it.

Virtualization provides improved resource allocation, scalability, and flexibility, enabling efficient use of hardware and reducing costs. However, vulnerabilities in the virtualization layer can be exploited to compromise the entire infrastructure. Moreover, virtualization introduces the risk of "escape attacks," where an attacker compromises one virtual machine and attempts to break out of the virtual environment to access the underlying host or other virtual machines.
 
# Task2: Supply Chain Attacks

This comprehensive report emphasizes several vital strategies to counter potential supply chain threats. It advocates for enhancing transparency and verification measures by utilizing blockchain technology, which facilitates a seamless, transparent, and immutable record-keeping process throughout the supply chain. By ensuring secure transportation and storage, companies can maintain the integrity of their products. This involves collaborating with trusted partners, enforcing stringent security protocols, and implementing a combination of GPS tracking systems and tamper-evident packaging to monitor the products in real-time and protect them from any potential falsification during transit and storage. Guaranteeing code and update integrity is equally crucial. The report highlights the significance of conducting regular code reviews and audits by credible third-party firms to identify any vulnerabilities or backdoors in the software. 

The report also emphasizes the necessity of managing vendor and employee risks, especially in scenarios where certain components are outsourced. To mitigate these risks, thorough due diligence on all vendors is recommended, which includes a comprehensive evaluation of their security practices, certifications, and past records. The implementation of a robust vendor risk management program is suggested to regularly assess and monitor the security practices of each vendor. Additionally, the report suggests conducting regular security awareness training for employees and implementing strict access controls to reduce the potential threat of insider attacks.

To effectively implement these strategies, the report recommends the deployment of secure hardware components by integrating tamper-resistant hardware and trusted platform modules, which play a pivotal role in ensuring the integrity of the hardware during the manufacturing process. It also suggests the use of advanced threat detection mechanisms such as Network Detection and Response (NDR) solutions and User Behavioral Analytics (UBA) to detect and mitigate any potential supply chain attacks in real-time.

In the context of ensuring secure software development, the report stresses the significance of enforcing secure coding practices within the organization and among contractual coders. This involves the incorporation of secure coding guidelines, conducting regular security training sessions for developers, and the utilization of automated code scanning tools to identify and rectify any vulnerabilities during the development phase.

However, the implementation of these strategies might pose various challenges, such as increased operational costs and complexity of supply chain management. To address these challenges, the report recommends the allocation of sufficient resources for ongoing security investments, the establishment of clear communication channels with all stakeholders, and the promotion of a culture of security awareness and responsibility among employees and partners.

Furthermore, establishing a dedicated supply chain security team is deemed crucial for the successful implementation and enforcement of these security measures. Such a team can ensure effective coordination, implementation, and monitoring of security protocols, while also keeping abreast of the latest security trends and emerging threats.

In conclusion, a comprehensive approach integrating robust security measures, regular audits, and effective risk management practices is indispensable for fortifying the supply chain and ensuring the integrity of products. The necessity of maintaining a vigilant and collaborative security mindset is a key factor in ensuring the long-term resilience of the supply chain ecosystem.
