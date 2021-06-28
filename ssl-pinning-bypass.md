# SSL Pinning Bypass

## SSL Pinning Bypass

### Steps :

1. Go to geanymotions tools/ folder. \( /tools/mobile/genymotion/tools\)  
2. Use adb server from there.  
3. Find a device you want to connect to  

   ```text
   ./adb devices
   ```

4. Push any files to Mobile storage  

   ```text
   ./adb push -p /home/ohhboy/Figmdwork/NBIR App/cert.cer /data/local/tmp/cert-der.crt
   ```

5. You can get emulator shell via  

   ```text
   ./adb shell
   ```

_Option to have shell on device_

1. Upload frida-server to this path /data/local/tmp  

   ```text
   ./adb push ~/Downloads/frida-server /data/local/tmp
   ```

2. Change the permission of frida-server  

   ```text
   ./adb shell chmod 777 /data/local/tmp/frida-server
   ```

3. Start the firda-server & in backgroud  

   ```text
   ./adb shell /data/local/tmp/frida-server &
   ```

4. Find the app's process you want to hook the frida using frida-ps client installed on PC  

   ```text
   frida-ps -U | grep nbir
   ```

com.figmd.nbir

1. Inject the frida.js  

   ```text
   frida -U -f com.figmd.nbir -l frida.js --no-pause
   ```

/tools/mobile/genymotion/tools

**References**

[https://arben.sh/bugbounty/Configuring-Frida-with-Burp-and-GenyMotion-to-bypass-SSL-Pinning/](https://arben.sh/bugbounty/Configuring-Frida-with-Burp-and-GenyMotion-to-bypass-SSL-Pinning/)  
[https://codeshare.frida.re/](https://codeshare.frida.re/)  
[https://github.com/frida/frida/releases](https://github.com/frida/frida/releases)  
[https://medium.com/@briskinfosec/getting-started-with-frida-de44d932ae7](https://medium.com/@briskinfosec/getting-started-with-frida-de44d932ae7)

adb push -p /home/ohhboy/Figmdwork/NBIR App/cert.cer /data/local/tmp/cert-der.crt

adb connect 192.168.56.104:5555

/usr/bin/adb push -p /home/ohhboy/Figmdwork/NBIR App/cert.cer /data/local/tmp/cert-der.crt

/opt/genymotion/tools/adb push ~/Downloads/frida-server /data/local/tmp

/opt/genymotion/tools/adb shell chmod 777 /data/local/tmp/frida-server  
/opt/genymotion/tools/adb shell /data/local/tmp/frida-server &

frida-ps -U \| grep nbir

com.figmd.nbir

frida -U -f com.figmd.nbir -l frida.js –no-pause

adb shell "/data/local/tmp/frida-server &"

**Mobile Reverse engineering**

[https://github.com/linkedin/qark](https://github.com/linkedin/qark)  
[https://www.ragingrock.com/AndroidAppRE/index.html](https://www.ragingrock.com/AndroidAppRE/index.html)  
[https://github.com/skylot/jadx](https://github.com/skylot/jadx)  
[https://ibotpeaches.github.io/Apktool/](https://ibotpeaches.github.io/Apktool/)

**Checklist**

[https://github.com/b-mueller/android\_app\_security\_checklist](https://github.com/b-mueller/android_app_security_checklist)



