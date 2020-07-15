---
uid: Create_trusts
---

## Create trusts

If you are installing the PI UFL interface on a node separate from PI Data Archive, you must create trusts for the following programs:
* PI UFL interface
* PI Interface Configuration Utility (PI ICU)
* PI SDK (if you are using PI annotations, automatic point configuration, or digital set or digital state creation)
* PI SDK or PI API buffering (if running against a PI Data Archive with high availability features)

### Procedure

1. Start PI System Management Tools (PI SMT) and connect to the PI Data Archive.
2. Click **Security > Mappings & Trusts**.
3. On the **Trusts** tab, right-click and then choose **New Trust** when the Add Trust wizard opens.
4. In the Add Trust wizard, specify a meaningful name and description.
5. Configure settings as follows:

| Program | Type of Trust | Application Name |
| ------- | ------------- | ---------------- |
| Buffering | PI-API application | APIBE (PI Buffer Server) or pibufss (PI SDK buffering) |
| PI ICU | PI-API application | PI-ICU.exe |
| PI UFL interface | PI-API application | PI_UE |
| PI UFL interface | PI-SDK application | PI_UFL.exe |

The PI identity you specify for the trust must have permission to update the PI Module Database. For maximum security, specify the network path using a fully-qualified node name or IP address plus netmask 255.255.255.255.
