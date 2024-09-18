# SMB (server message block)
#### use in windows to networking file sharing
---

`smbclient -N -L \\\\10.129.42.253`
>-L flag specifies that we want to retrieve a list of available shares on the remote host
>-N suppresses the password prompt.
>![380ae46de5f02b838c348f7e6cc20dca.png](../../_resources/380ae46de5f02b838c348f7e6cc20dca.png)

**This reveals the non-default share users. Let us attempt to connect as the guest use**
`smbclient \\\\10.129.42.253\\users`
>it will connect with guest user
>
**to connect with any user
`smbclient -U user \\\\10.123.134.1\\users`