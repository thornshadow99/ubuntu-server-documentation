(introduction-to-active-directory-integration)=
# Introduction to Active Directory integration

![Active Directory](../images/ad_integration.png)

Because the desired level of integration and the complexity of the Active Directory deployment is going to differ, joining an Ubuntu system to an Active Directory-based system will require planning, specific tools, and an appropriate configuration. The requirements change because Active Directory deployments range from single-domain and one tree, with one or more servers, up to a "forest," which is a dynamic structure with multiple domains and geographically dispersed servers.  

Once an Ubuntu system is joined to an Active Directory domain (or a forest), the Ubuntu system should be assigned an account in that domain and be able to identify and authenticate users from that domain. In other words, a joined Ubuntu system should be able to:
- authenticate Active Directory users and allow them to change their passwords
- recognize Active Directory users as valid users on the Ubuntu system, with Linux-compatible user and group identifiers
- recognize group memberships

Depending on how the join was performed and which software stacks are available on the Ubuntu system, the following is also possible:
- authenticating and recognizing users from different domains that make up the forest
- applying certain group policy objects (not covered here)
- providing file and print services to users from the domain

To set up your Active Directory integrations, we suggest first familiarising yourself with the following key topics:

* {ref}`Choosing an integration method <choosing-an-integration-method>`
* {ref}`Security identifiers <security-identifiers-sids>`
* {ref}`Identity mapping backends <identity-mapping-idmap-backends>`
* {ref}`The rid idmap backend <the-rid-idmap-backend>`
* {ref}`The autorid idmap backend <the-autorid-idmap-backend>`

## References

- About Active Directory:
  - [Security Identifiers (SIDs)](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/manage/understand-security-identifiers)
  - [Active Directory Domain Services Overview](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/get-started/virtual-dc/active-directory-domain-services-overview)
- Samba Wiki pages:
  - [Choosing an identity mapping backend](https://wiki.samba.org/index.php/Setting_up_Samba_as_a_Domain_Member#Choosing_an_idmap_backend)
  - [rid identity mapping backend](https://wiki.samba.org/index.php/Idmap_config_rid)
  - [autorid identity mapping backend](https://wiki.samba.org/index.php/Idmap_config_autorid)
- Manual pages:
  - [idmap_tdb(8)](https://manpages.ubuntu.com/manpages/noble/man8/idmap_tdb.8.html)
  - [idmap_rid(8)](https://manpages.ubuntu.com/manpages/noble/man8/idmap_rid.8.html)
  - [idmap_autorid(8)](https://manpages.ubuntu.com/manpages/noble/man8/idmap_autorid.8.html)
  - [wbinfo(1)](https://manpages.ubuntu.com/manpages/noble/en/man1/wbinfo.1.html)
