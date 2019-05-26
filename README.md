# "Security Architecture and the Big Picture” Pluralsight Course by Christopher Rees.

## Installing and configuring network components

Security threats sources include internal, external, unknown devices on network, misconfigured devices, unintentional data loss / leakage
tcp/ip and osi model

Network components that can be configured include;

`Firewalls` (network) e.g packet filtering firewalls (all or deny based on ports) proxy firewalls (uses `NAT`). firewalls (web app) e.g cisco, citrix, for sql injection, cross site forgery, 
`VPN`, creates a private network across a public network (tunnelling and encryption), 2FA for RSA token.

`NIPS` & `NIDS` network intrusion detection and prevention (log alerts & events and taking action). works best when placed in front and behind a firewall
Router (connects two networks and allows them talk to each other)

`Layer 2` vs `layer 3` (data link layer - mac addresses and network layer - ip addresses) switches and routers

`Load balancers` - dynamically balance load between servers / devices. balance distribution of traffic across servers. scheduling (affinity / round-robin) active-passive active-active

Web security gateways (proxy servers that prevent connection to wrong sites, data loss, and enables virus scanning). it also enables granular access to websites.

`Port security - configuring a switch to learn one Mac address per port

Loop protection and flood guards (layer 3 implements time to live (ttl)

`Access points / wifi-security` (mac filtering, disabling ssid broadcast - wifi network name)

Security info and event management systems ( automated alerts and triggers, data aggregation, correlation, time sync, logs)

`Data loss prevention - DLP` (detects potential breaches and exfiltration of data

`NAC - network access control`  (set of policies that define a minimal set of requirements each device must have before being allowed on the network) anti-virus, OS,

Hardware based encryption (usb encryption, hard drive)

Mail gateway (spam filter, data loss prevention)

Summary (firewalls, VPNS, NIDS/NIPS, encryption/data protection, wireless access / gateways, networking components (routers, switches, lbs)


## Implementing secure protocols

Secure protocols ensure communication is safe from hackers and prying eyes

Networking protocols e.g

`dns` secure (resolving web to ip addresses) digitally signed, authenticating their origin

`ssh` -secure shell. connecting to remote servers over tcp port 22

`ssl/tls` - secure sockets layer, transport layer security. adds confidentiality and data integrity by encapsulating other protocols. It initiates stateful session with handshake

`https` - http secure via tls or ssl. authenticating visited sites and privacy of the data exchange

`snmp` - simple network mgt protocol. remote mgt and reporting of IP’s

Use cases include; email and web browsing, file transfer, voice and audio, time synchronization 



## Implementing secure network architecture

Topology concepts - `Honeynets` (monitored networks that are left vulnerable to attract hackers and cybercriminals

`NAT - network address translation` - masks private IP address from the internal network as it enters the public external network.

`Network segregation` for more security e.g 

`Virtualisation` - Keeps host in a sandboxed isolated environment

`Airgaps` - isolating a computer or network from external networks / internet. 

`VPN concetrator` to create a large number of VPN tunnels typically used for site to site architectures. Usually between secured and hidden networks. 

`SDN - software defined networking` (allows separation of the application tier, data plane tier and control plane) through a single orchestrator. 


## Troubleshooting common security issues 

Unencrypted credentials sharing.

Logs and events should be reviewed. Setting up triggers is awesome.

Access violations to identify brute force attacks. 

Common misconfigurations e.g firewalls, access points and content filters

Personal issues e.g having a method to deal with policy violations

Unauthorized software e.g pirated software which often contains malware.

Authentication audit e.g Minimum required levels of access, single sign on (SSO)

## Implanting secure systems design

Hardware/firmware security e.g boot loader protections like secure boot to allow only signed boot software to load. Measured launch  of the boot components. Universal extensible firmware interface with CPU independent architecture and drivers.

Enabling data encryption e.f hardest to prevent access without proper credentials. 

Securing data e.g data in transit, data at rest and data at use. by using passwords, VPN etc

Operating system types e.g network, servers, workstation, appliance. Trusted OS ensures an OS meets the minimum level of security. 

Mobile OS designs e.g insecure access to websites and WI-FI

Hardening servers and removing unneeded services.

User accounts and least permissive. 

Worksrstaion e.g screensavers, passwords change timeframes


## Secure application development and deployment 

Development lifecycle modes e.g ensuring security in agile since it’s feedback oriented with the customer. Also testing new requirements. 

Secure devOps e.g tests and automation

Version control vs change mgt. Integrating early and often, having continuous delivery pipeline in place. 

Provisioning and deprovisioning

Secure coding techniques e.g proper error handling, proper input validation, DB normalisation, encryption.

Code quality and testing e.g TDD, integration tests, functionality tests. 

Compiled vs runtime code . compiles catches errors during compilation before code is actually run. Runtime enables an interpreter to execute at runtime. It detects error int he process which brings risks like crashing, memory dump etc.

Immutable systems e.g replacing components after every deployment like artefacts and terraform state. IAAS - scripts that represent our infrastructure state. 

Three takeaways - always develop secure code, think and test like a hacker, manage change to ensure security.



## Physical security controls

`Proper lighting`

`Fencing`

`Guards`

`Alarms`

`Signs`

`Securing physical address`

`Hardware locks`

`Biometrics`

`Fire suppression`
