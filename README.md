## Experimental aarch64 based Android emulator on Github runner

### Getting Started
For connection this package uses [bore](https://github.com/ekzhang/bore)  
To use the emulator you can start by forking this repository.  
To start the emulator you can go to Action tab and manually start the CI workflow.  
You must supply your own server key in the git repository secret with variable **BORE_IP**  
```bash
## It wil be listed like this 
listening at ...:XXXX
```

### Connect to emulator from client
Install required package

```bash
sudo apt update
sudo apt install cargo adb scrcpy
```
Then connect to devices using adb and mirror using [scrcpy](https://github.com/Genymobile/scrcpy)

```bash
adb connect $BORE_IP:XXXX
scrcpy -s $BORE_IP:XXXX
```
### TODO
- Add GMS
- Create custom tunnel for scrcpy
- ...
