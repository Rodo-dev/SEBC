[saturn@nodo2 jars]$ hadoop jar hadoop-examples.jar teragen 10000000 /user/saturn/terasort-inputki^C
[saturn@nodo2 jars]$ kinit 
Password for saturn@RODO.COM: 
[saturn@nodo2 jars]$ hadoop jar hadoop-examples.jar teragen 10000000 /user/saturn/terasort-input
17/12/01 20:37:13 INFO client.RMProxy: Connecting to ResourceManager at nodo1.rodo.com/10.0.1.4:8032
17/12/01 20:37:13 INFO hdfs.DFSClient: Created token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@RODO.COM, renewer=yarn, realUser=, issueDate=1512160633256, maxDate=1512765433256, sequenceNumber=1, masterKeyId=2 on 10.0.1.4:8020
17/12/01 20:37:13 INFO security.TokenCache: Got dt for hdfs://nodo1.rodo.com:8020; Kind: HDFS_DELEGATION_TOKEN, Service: 10.0.1.4:8020, Ident: (token for saturn: HDFS_DELEGATION_TOKEN owner=saturn@RODO.COM, renewer=yarn, realUser=, issueDate=1512160633256, maxDate=1512765433256, sequenceNumber=1, masterKeyId=2)
17/12/01 20:37:13 WARN security.UserGroupInformation: PriviledgedActionException as:saturn@RODO.COM (auth:KERBEROS) cause:org.apache.hadoop.security.AccessControlException: Permission denied: user=saturn, access=WRITE, inode="/user/saturn":hdfs:supergroup:drwxr-xr-x
	at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.checkFsPermission(DefaultAuthorizationProvider.java:281)
	at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.check(DefaultAuthorizationProvider.java:262)
	at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.check(DefaultAuthorizationProvider.java:242)
	at org.apache.hadoop.hdfs.server.namenode.DefaultAuthorizationProvider.checkPermission(DefaultAuthorizationProvider.java:169)
	at org.apache.hadoop.hdfs.server.namenode.FSPermissionChecker.checkPermission(FSPermissionChecker.java:152)
	at org.apache.hadoop.hdfs.server.namenode.FSDirectory.checkPermission(FSDirectory.java:3560)
	at org.apache.hadoop.hdfs.server.namenode.FSDirectory.checkPermission(FSDirectory.java:3543)
	at org.apache.hadoop.hdfs.server.namenode.FSDirectory.checkAncestorAccess(FSDirectory.java:3525)
	at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.checkAncestorAccess(FSNamesystem.java:6593)
	at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.mkdirsInternal(FSNamesystem.java:4384)
	at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.mkdirsInt(FSNamesystem.java:4354)
	at org.apache.hadoop.hdfs.server.namenode.FSNamesystem.mkdirs(FSNamesystem.java:4327)
	at org.apache.hadoop.hdfs.server.namenode.NameNodeRpcServer.mkdirs(NameNodeRpcServer.java:873)
	at org.apache.hadoop.hdfs.server.namenode.AuthorizationProviderProxyClientProtocol.mkdirs(AuthorizationProviderProxyClientProtocol.java:323)
	at org.apache.hadoop.hdfs.protocolPB.ClientNamenodeProtocolServerSideTranslatorPB.mkdirs(ClientNamenodeProtocolServerSideTranslatorPB.java:618)
	at org.apache.hadoop.hdfs.protocol.proto.ClientNamenodeProtocolProtos$ClientNamenodeProtocol$2.callBlockingMethod(ClientNamenodeProtocolProtos.java)
	at org.apache.hadoop.ipc.ProtobufRpcEngine$Server$ProtoBufRpcInvoker.call(ProtobufRpcEngine.java:617)
	at org.apache.hadoop.ipc.RPC$Server.call(RPC.java:1073)
	at org.apache.hadoop.ipc.Server$Handler$1.run(Server.java:2141)
	at org.apache.hadoop.ipc.Server$Handler$1.run(Server.java:2137)
	at java.security.AccessController.doPrivileged(Native Method)
	at javax.security.auth.Subject.doAs(Subject.java:415)
	at org.apache.hadoop.security.UserGroupInformation.doAs(UserGroupInformation.java:1912)
	at org.apache.hadoop.ipc.Server$Handler.run(Server.java:2135)
