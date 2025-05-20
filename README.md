## Experimental aarch64 based Android emulator on Github runner
**!!!!WARNING TO USE YOUR OWN BORE SERVER CHANGE TO CUSTOM-SERVER BRANCH**  
### Getting Started
For connection this package uses [bore](https://github.com/ekzhang/bore)  
To use the emulator you can start by forking this repository.  
To start the emulator you can go to Action tab and manually start the CI workflow.  
You can get the bore.pub port from 'run bore' section.  
```bash
## It wil be listed like this 
listening at bore.pub:XXXX
```

### Connect to emulator from client
Install required package

```bash
sudo apt update
sudo apt install cargo adb scrcpy
```
Then connect to devices using adb and mirror using [scrcpy](https://github.com/Genymobile/scrcpy)

```bash
adb connect bore.pub:XXXX
scrcpy -s bore.pub:XXXX
```
### TODO
- Add GMS
- Create custom tunnel for scrcpy
- ...
