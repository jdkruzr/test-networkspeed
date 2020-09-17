# test-networkspeed
Powershell utility to test speeds reading from and writing to an SMB network resource.

This is a derivative work from Martin Pugh's excellent script posted here: https://community.spiceworks.com/scripts/show/2502-network-bandwidth-test-test-networkspeed-ps1?login_from=%7C%20google%20%7C%20MVPReg1

The main difference between these is that mine is specifically intended to test *storage* performance over the network, while Martin's is intended to test *network* performance by using data transfers from one storage location to another. So, Martin's takes many targets as arguments and generates its own dummy file of arbitrary size from 1M to 1G. Mine only takes two arguemnts: a local folder for source files whose transfer times you want to profile, and a remote folder in the form of a UNC path to a share the network storage performance of which you want to test. I've also simplified a few other things and removed a few features, because frankly I'm a Powershell neophyte and I wasn't sure how to reimplement them with my test structure 😅
