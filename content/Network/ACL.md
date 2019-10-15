+++
title = "Access List Cisco"
description = ""
weight = 1
+++

### Standard ACL Syntax
```bash
# Legacy syntax
access-list <number>{permit | deny} <source>

# Modern syntax
ip access-list standard {<number> | <name>} {permit | deny}
```
### Extended ACL Syntax
```bash
# Legacy syntax
access-list <number>{permit | deny} <protocol><source> [<ports>]<destination> [<ports>]

# Modern syntax
p access-list extended {<number>| <name>}[<sequence>] {permit | deny} <protocol><source> [<ports>]<destination> [<ports>]
```
