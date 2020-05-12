● 修改jks密码
keytool -storepasswd -keystore xx.jks

● 打印jks信息
keytool -list -v -keystore xx.jks    

● 打印 RSA
 keytool -printcert -file META-INF/CERT.RSA 