# KerberosAndSSLClients

Collection of various client programs and steps to test the working of kerberos SSL. 

SSL:
Run any program with following option to se the details of SSL transactions and it's error:

-Djavax.net.debug=ssl:handshake:verbose:keymanager:trustmanager -Djava.security.debug=access:stack

Use the SSLPoke program taken from https://gist.github.com/4ndrej/4547029 as following to check if the truststore and password are correct 

java -Djavax.net.ssl.trustStore=/<path of trustore>/truststore.jks -Djavax.net.ssl.trustStorePassword=<password> SSLPoke <host> <port>
  
  Or use with extra debug options to see verbose log
  
java -Djavax.net.ssl.trustStore=/<path of trustore>/truststore.jks -Djavax.net.ssl.trustStorePassword=<password> -Djavax.net.debug=ssl:handshake:verbose:keymanager:trustmanager -Djava.security.debug=access:stack SSLPoke <host> <port>
  
  
  KERBEROS:
  
  
