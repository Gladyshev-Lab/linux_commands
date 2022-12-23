# linux_commands

### Check all user ids
`awk -F: '($3 >= 1000) {printf "%s:%s:%s\n",$1,$3,$4}' /etc/passwd`

### Adding a new user
```
u= [username]
ui= [user ID]  # need to choose an available ID
sudo addgroup --gid $ui $u
sudo adduser --uid $ui --gid $ui $u
```

### Change password
`sudo passwd $u`
