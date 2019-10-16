+++
title = "Firewall Cisco"
description = ""
weight = 2

+++

### Terminology

**Security Zone** : A group of interfaces which share a common level of security.

**Zone Pair** : A unidirectional pairing of source and destination zones to which a security policy is applied. 

**Inspection Policy** : An inspect-type policy map used to state-fully filter traffic by matching one or more inspect-type class maps.

**Parameter Map** : An optional configuration of protocol-specific parameters referenced by an inspection policy.

### Security Zones

![Security Zones](/img/ZoneBased_Firewall.png)

````raw
# Defining security zones
zone security DMZ
zone security OUTSIDE
zone security INSIDE
# Assigning interfaces to security zones
interface GigabitEthernet0/0
	zone-member security DMZ
!
interface GigabitEthernet0/1
	zone-member security INSIDE
!
interface GigabitEthernet0/2
	zone-member security OUTSIDE
````



### Add security license

````raw
R3(config)# license boot module c1900 technology-package securityk9
````

### Security zones



````raw
R3(config)#zone security <zone name>
````

### Creating Security Policies

````raw
# Create class map
R3(config)# class-map type inspect match-any <class name>

# Match protocol
R3(config-cmap)# match protocol <protocol>
R3(config-cmap)# match protocol udp
R3(config-cmap)# match protocol http

# Create policy-map
R3(config)#policy-map type inspect INSIDE_TO_INTERNET
R3(config-pmap)#class type inspect INSP_INSI_CLASS_MAP
R3(config-pmap-c)#inspect
````

### Create the Zone Pairs

````raw
R3(config)#zone-pair security INSIDE_PAIR source INSIDE destination INTERNET
R3(config-sec-zone-pair)#service-policy type inspect INSIDE_TO_INTERNET
````

