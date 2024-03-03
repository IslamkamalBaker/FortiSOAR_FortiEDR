# FortiSOAR_FortiEDR
Update Exist connector to include Move Collector to Specific Group

## About the connector
FortiEDR protects endpoints pre and post infection, stopping data breaches in real-time and automatically orchestrating incident investigation and response. This connector facilitates the automated operations related to events, forensics and collectors.
<p>This document provides information about the Fortinet FortiEDR Connector, which facilitates automated interactions, with a Fortinet FortiEDR server using FortiSOAR&trade; playbooks. Add the Fortinet FortiEDR Connector as a step in FortiSOAR&trade; playbooks and perform automated operations with Fortinet FortiEDR.</p>
### Version information

Connector Version: 2.0.0


Authored By: Islam Baker

Certified: No
## Installing the connector
<p>Use the <strong>Content Hub</strong> to install the connector. For the detailed procedure to install a connector, click <a href="https://docs.fortinet.com/document/fortisoar/0.0.0/installing-a-connector/1/installing-a-connector" target="_top">here</a>.</p><p>You can also use the <code>yum</code> command as a root user to install the connector:</p>
<pre>yum install cyops-connector-fortinet-fortiedr_dev</pre>

## Prerequisites to configuring the connector
- You must have the credentials of Fortinet FortiEDR server to which you will connect and perform automated operations.
- The FortiSOAR&trade; server should have outbound connectivity to port 443 on the Fortinet FortiEDR server.

## Minimum Permissions Required
- Not applicable

## Configuring the connector
For the procedure to configure a connector, click [here](https://docs.fortinet.com/document/fortisoar/0.0.0/configuring-a-connector/1/configuring-a-connector)
### Configuration parameters
<p>In FortiSOAR&trade;, on the Connectors page, click the <strong>Fortinet FortiEDR</strong> connector row (if you are in the <strong>Grid</strong> view on the Connectors page) and in the <strong>Configurations</strong> tab enter the required configuration details:</p>
<table border=1><thead><tr><th>Parameter</th><th>Description</th></tr></thead><tbody><tr><td>Server URL</td><td>URL of the Fortinet FortiEDR server to which you will connect and perform the automated operations.
</td>
</tr><tr><td>Username</td><td>Username that contains a Rest API role and using which you will access the Fortinet FortiEDR server to which you will connect and perform the automated operations.
</td>
</tr><tr><td>Password</td><td>Password used to access the FortiEDR server to which you will connect and perform the automated operations.
</td>
</tr><tr><td>Verify SSL</td><td>Specifies whether the SSL certificate for the server is to be verified or not. <br/>By default, this option is set to True.</td></tr>
</tbody></table>
## Actions supported by the connector
The following automated operations can be included in playbooks and you can also use the annotations to access operations from FortiSOAR&trade; release 4.10.0 and onwards:
<table border=1><thead><tr><th>Function</th><th>Description</th><th>Annotation and Category</th></tr></thead><tbody><tr><td>Get Event by ID</td><td>Retrieves a specific event from Fortinet FortiEDR based on the event ID you have specified.</td><td>get_event <br/>Investigation</td></tr>
<tr><td>Get Events</td><td>Retrieves all the events from Fortinet FortiEDR that match the condition(s) you have specified. Note: If none of the input parameters that you specify match the events in Fortinet FortiEDR, then an empty result set is returned.</td><td>get_event_list <br/>Investigation</td></tr>
<tr><td>Update Events</td><td>Updates events in Fortinet FortiEDR that match the condition(s) you have specified. 
Note: If none of the input parameters that you specify match the events in Fortinet FortiEDR, then an empty result set is returned.</td><td>update_event <br/>Investigation</td></tr>
<tr><td>Get Raw Data Items</td><td>Retrieves the raw data items from Fortinet FortiEDR based on the event ID and other input parameters you have specified.</td><td>get_raw_data_items <br/>Investigation</td></tr>
<tr><td>Get Event Count</td><td>Retrieves the event count from Fortinet FortiEDR based on the filter parameters you have specified.</td><td>get_event_count <br/>Investigation</td></tr>
<tr><td>Get Event List Extended</td><td>Retrieves archived/unarchived events together from Fortinet FortiEDR based on the filter parameters you have specified. 
Note: If none of the input parameters that you specify match the events in Fortinet FortiEDR, then an empty result set is returned. </td><td>get_event_list <br/>Investigation</td></tr>
<tr><td>Search Filehash</td><td>Searches a file hash among the current events, threat hunting repository, and communicating applications that exist in the Fortinet FortiEDR system.</td><td>search_filehash <br/>Investigation</td></tr>
<tr><td>Get File</td><td>Retrieves a specific file from the specified device from Fortinet FortiEDR, based on the device type, device name/ID, and file paths you have specified, and adds it as an attachment in CyOPs™</td><td>get_file <br/>Investigation</td></tr>
<tr><td>Retrieve File or Memory</td><td>Retrieves a file or memory related to a specific event from Fortinet FortiEDR based on the raw event ID and other input parameters you have specified and adds it as an attachment in CyOPs™.</td><td>get_event_file <br/>Investigation</td></tr>
<tr><td>Remediate Device</td><td>Takes remediation actions on Fortinet FortiEDR such as killing a process, deleting a file and/or cleaning persistent data on which malware was detected based on the device type, device name/ID, and other input parameters you have specified.</td><td>remediate_device <br/>Remediation</td></tr>
<tr><td>Get Collector List</td><td>Retrieves the list of the collectors from Fortinet FortiEDR based on the device type, device name/ID, and other input parameters you have specified.</td><td>get_collector_list <br/>Investigation</td></tr>
<tr><td>Isolate Collector</td><td>Isolates a collector from the Fortinet FortiEDR network based on the device ID and other input parameters you have specified.</td><td>isolate_collector <br/>Investigation</td></tr>
<tr><td>Unisolate Collector</td><td>Unisolates a collector from the Fortinet FortiEDR network based on the device ID and other input parameters you have specified.</td><td>unisolate_collector <br/>Investigation</td></tr>
<tr><td>Create Exception</td><td>Creates an IPSet in Fortinet FortiEDR using the set of IP addresses and other parameters you have specified.</td><td>create_exception <br/>Investigation</td></tr>
<tr><td>Get Exception List</td><td>Retrieves a list of IPSets from Fortinet FortiEDR based on the IP address and other input parameters you have specified.</td><td>list_exception <br/>Investigation</td></tr>
<tr><td>Update Exception</td><td>Updates IP addresses in the specific IPSet in Fortinet FortiEDR using the set of IP addresses, the IPSet name, and other parameters you have specified.</td><td>update_exception <br/>Investigation</td></tr>
<tr><td>MOVE COLLECTOR TO ANOTHER GROUP</td><td>Move Collector to Specific Group</td><td>Move_collector<br/>Investigation</td></tr>

