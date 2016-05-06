#MF Google Import - User Guide

##System Requirements
MF Google Import requires .NET Framework 4.5 or later. It also requires M-Files server to be installed since it is at it's core an M-Files vault app. While MF Google Import may work with earlier versions of M-Files, it is officially supported on version 2015 (11.0) or later.

##Installation
MF Google Import can be installed using the MSI file provided on this page. It will create a desktop shortcut and start menu entry under Start>Programs>Andrew Roth Solution Development.

##M-Files Configuration
MF Google Import requires the following properties to be created and aliased. You will be asked for the aliases in the MF Google Import Configuration Tool.
* Message ID
* Thread/Conversation ID

Additionally, you may create and assign aliases to the following properties in M-Files. If you define the aliases for these fields in the MF Google Import configuration tool the properties will be automatically added to the imported emails.
* Send Date
* Send Time
* To Address
* From Address
* CC
* BCC
* Subject

##MF Google Import Configuration
All MF Google Import configuration can be done from the MF Google Import configuration tool that was added to the desktop and start menu. You may make changes to the configuration without restarting your vault. Each time MF Google Import runs it will retrieve any new configuration changes that were made.

###Licensing
MF Google Import will not work without a license. To apply your license click the License Management button in the toolbar at the top of the window. Navigate to and click Apply License File. An Open File window will appear. Choose the license file that was sent to you and click Open.

After you apply your license, the details of the license may be viewed at any time by navigating to License Management > View License Details.

A license has 2 main components, a "Valid Until" date and a list of licensed email addresses. If you purchase a permanent license your "Valid Until" date will be December 31, 2099.

When purchasing a permanent license, you only need pay the up-front server license once. You may at any time request a new license with more email addresses and only pay the per-email-address fee.

To request a license, please contact your vendor.

###Email Addresses
To add an email address, click the + button next to the email addresses box. Your default browser will launch a window with a Google authentication prompt. Choose or type the email address you would like to add, then type the password. Once the email address and password are entered successfully and the new email address has been added to the list in the configuration tool you may close the browser window.

To remove an email address, click the email address you'd like to remove, then click the - button next to the email addresses box.

###Gmail Main Label To Watch
This is the name of the primary label under which all imported emails will be assigned. You may also add just this label to the email for it to be imported with no extra metadata (unless one of the sublabels is mapped to a required property).

###Radio Button - Class is first secondary label
If this radio button is selected, the first sublabel under the primary label is the name of the document class to use. The value needs to be the name of the class, not the alias.

###Radio Button - Class is fixed
If this radio button is selected, the document class for imported emails will be fixed to the value in the "Name of Fixed Class to Use" text field. The value needs to be the name of the class, not the alias.

###Import Frequency
The number of seconds MF Google Import waits between processing. If you change this value you need to restart your vault for it to take effect.

###Radio Button - Import labeled emails only
If this radio button is selected, only emails that you label will be imported. Other emails that are part of the same conversation that arrive later will not be imported. Please note that if you assign a label to a conversation all emails currently in that conversation will be imported.

###Radio Button - Import unlabeled emails in a labeled conversation
If this radio button is selected, emails in the same conversation will continue to be imported automatically. If you wish to stop the import of a particular conversation, you can remove the import label or add the "Imported to M-Files" label.

###Secondary Label Levels
Use sublabels underneath your primary label to set metadata. For example: If you wanted to organize and import emails for a certain company and topic you would set up your labels like this:

 * MFIMPORT (main label)
  * Joe's Fish Shack
    * Lunch Orders

Set up your secondary label levels in the configuration tool as shown:

| Descriptions | Aliases                  |
| ------------ | ------------------------ |
| Company      | M-Files.Property.Company |
| Topic        | M-Files.Property.Topic   |

If you drop the label "MFIMPORT/Joe's Fish Shack/Lunch Orders" onto an email MF Google Import will import the message(s) with properties:

| Property     | Value            |
| ------------ | ---------------- |
| Company      | Joe's Fish Shack |
| Topic        | Lunch Orders     |

###Message ID Alias
Type the alias of the Message ID property in M-Files. MF Google Import will run an M-Files search using this property when importing messages. If the message ID it is looking for is already present in M-Files it won't import the message.

###Thread ID Alias
Type the alias of the Thread/Conversation ID property in M-Files. MF Google Import uses this property when controlling importing of conversations.

##Installing the Vault App
Once you are finished with configuration click Tools > Create Vault App Zip Package to create the .zip file that is used to install an M-Files Vault Application.

Once you have the .zip file, open M-Files Admin tool, Right-Click your vault, click Applications, click Install, and navigate the the .zip file. After installing the vault app make sure the vault is restarted. M-Files will usually ask to restart the vault as soon as you install it.

##Troubleshooting
If you are having issues, open the Windows Event Viewer application and navigate to Windows Logs > Application. All MF Google Import log entries will be made under the Source "MF Google Import".