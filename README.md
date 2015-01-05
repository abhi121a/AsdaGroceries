
=============
If you face problem while cloning the Project.

check below links -http://stackoverflow.com/questions/18356502/github-failed-to-connect-to-github-443-windows-failed-to-connect-to-github
or below text.
Well I did following steps-

Google the error
Got to SO Links(here, here) which suggested the same thing, that I have to update the Git Config for proxy setting

God Damn, can not see proxy information from control panel. IT guys must have hidden it. I can not even change the setting to not to use proxy.

Found this wonderful tutorial of finding which proxy your are connected to

Updated the http.proxy key in git config by following command

git config --global http.proxy http[s]://userName:password@proxyaddress:port

Error - could not resolve proxy some@proxyaddress:port. It turned out my password had @ symbol in it.

Encode @ in your password to %40 because git splits the proxy setting by @

git config --global http.proxy http[s]://userName:password(encoded)@proxyaddress:port

Baam ! it worked !

Note - I just wanted to answer this question for souls like me, who would come looking for answer on SO :D
http://superuser.com/questions/346372/how-do-i-know-what-proxy-server-im-using
