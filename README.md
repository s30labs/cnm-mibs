# cnm-mibs
SNMP MIB files repository for a Network Management Console usage. 

Created for public usage and seamlessly integration with net-snmp and Custom Network Manager

All MIB files included are checked and verified with net-snmp (version: 5.6.1)


-----------------------------------------------------------
A. CONSIDERATIONS
-----------------------------------------------------------

In order to simplify the usage, the name of the MIB files follow this convention:

enterprise_ID-enterprise_name-MIB_name.[mib|txt]

enterprise_ID: Numeric ID of the enterprise with five digits.
enterprise_name: Textual Name of the enterprise as defined by the IANA.
MIB_name: The name of the MIB as specified inside the file.

The extension is usually txt or mib (it tries to follow the original format of the file)

Some examples:

00000-mib2-BRIDGE-MIB.txt
06876-vmware-VMWARE-CIMOM-MIB.mib

-----------------------------------------------------------
B. USAGE
-----------------------------------------------------------

git clone https://github.com/s30labs/cnm-mibs.git /opt/cnm-mibs

export MIBS=ALL

Use the -M option (-M /opt/cnm-mibs) in your net-snmp command

or  specify the MIB path in the snmp.conf (mibdirs /opt/cnm-mibs)

