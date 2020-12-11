# Vigil Probes Readme
Vigil probes are meant to be simple and open source.

## Probe Readme template
We all know that code should be self explainatory, but readme's are still mandatory for the probes.

### [information]
Name: SELinux Verifier
Description: A probe checking if SELinux is running or not. Can be configured to
force enablement of SELinux of choosen.

Author: John Doe

Contact: example@email.com

### [installation]
1. Place binary in $PLUGINS_DIR
   For example: /usr/local/vigil/plugins/selinux 
   
   You can also run the following command to see configured directories:
     <code> $ vigilctl --show-dirs </code>
  
2.  Update the vigil-probes.conf file
	For example:
		<code>[SELinux Enabled]=$PLUGINS_DIR/selinux -c enabled</code>

3. Validate that the probe is working by running:
  <code>$ vigilctl --validate-probes </code>
    Or run the <code> $PLUGINS_DIR/selinux -c enabled </code> command from the terminal/command line.

### [MAN Page]


	--critical [-c] : String that will cause the probe to return a Critical state
	
	--warning [-w] : String that will cause the probe to return a Warning state
### [MAN Page - Example]



### [Output interpretation]
	Return codes:
		0 : OK
		1 : Warning
		2 : Critical
		3 : UNKNOWN
		
	Return message/string: 
		OK : SELinux is [enabled/disabled] !
		Warning : SELinux is [enabled/disabled] !
		Error	: SELinux is [enabled/disabled] !
		UNKNOWN	: SELinux state unavailable !
		
### [Other / Please Note / Warning]
