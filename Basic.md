**Disable DNS Lookup**

`no ip domain lookup`

**Defines a new password or changes an existing password for access to privileged EXEC mode**

`enable secret <password>`

**Define console password and enable login**

```jsx
line con 0
password <password>
login
```

**Encrypt all plain text passwords**

`service password-encryption`

**To ensure that all configured passwords are at least a specified length**

`(no) security passwords min-length <length>`

**Banner**

`banner motd`

**Enable SSH**

Configure username, password and privilege

`username richard privilege 7 secret keepOUT`

Set domain-name

`ip domain-name <name>` 

Generate RSA key

`crypto key generate rsa general-keys modulus 1024`

Configure VTY Lines

```jsx
line vty 0 15
transport input ssh
*! Use user local database*
login local
*! time-out*
exec-timeout 120
*! login block-for seconds attempts tries within seconds*
login block-for 100 attempts 2 within 100
```

**Forcez l’application de IPv6**

`tracert -6 www.adresse-de-la-cible.fr`

**The value of the configuration register**

`show version`

**This command tells the router to wait until the user’s current command and its output are completed before displaying any logging messages**

`logging synchronous [levelseverity | all] [limitnumber-of-messages]
no logging synchronous`

**Sets the amount of time a session waits for user input before timing out and closing the session**

`exec-timeout minutes [seconds]`
