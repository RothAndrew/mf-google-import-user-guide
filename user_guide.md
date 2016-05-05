#MF Google Import - User Guide

##System Requirements
MF Google Import requires .NET Framework 4.5 or later. It also requires M-Files server to be installed since it is at it's core an M-Files vault app. While MF Google Import may work with earlier versions of M-Files, it is officially supported on version 2015 (11.0) or later.

##Installation
MF Google Import can be installed using the MSI file provided on this page. It will create a desktop shortcut and start menu entry under Start>Programs>Andrew Roth Solution Development.

##M-Files Configuration
MF Google Import requires the following properties to be aliased. You will be asked for the aliases in the MF Google Import Configuration Tool.
* Message ID
* Thread/Conversation ID

Additionally, you may assign aliases to the following properties in M-Files.
* Send Date
* Send Time
* To Address
* From Address
* CC
* BCC
* Subject

##MF Google Import Configuration
All MF Google Import configuration can be done from the MF Google Import configuration tool that was added to the desktop and start menu.

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
This is the name of the primary label under which all imported emails will be assigned. You may also add just this label to the email for it to be imported with no extra metadata.