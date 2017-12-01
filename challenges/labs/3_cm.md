* Add the following to 3_cm.md: 

  * `hdfs dfs -ls /user/`
      *Found 7 items
      *drwxr-xr-x   - hdfs   supergroup          0 2017-12-01 18:54 /user/haley
      *drwxrwxrwx   - mapred hadoop              0 2017-12-01 18:50 /user/history
      *drwxrwxr-t   - hive   hive                0 2017-12-01 18:51 /user/hive
      *drwxrwxr-x   - hue    hue                 0 2017-12-01 18:51 /user/hue
      *drwxrwxr-x   - oozie  oozie               0 2017-12-01 18:52 /user/oozie
      *drwxr-xr-x   - hdfs   supergroup          0 2017-12-01 18:53 /user/saturn
      *drwxr-x--x   - spark  spark               0 2017-12-01 18:50 /user/spark

* The command and output from the CM API call ../api/v14/hosts

0	
hostId	"fb937200-8c44-4e55-a321-92df5500e39a"
ipAddress	"10.0.1.4"
hostname	"nodo1.rodo.com"
rackId	"/default"
hostUrl	"http://nodo2.rodo.com:7180/cmf/hostRedirect/fb937200-8c44-4e55-a321-92df5500e39a"
maintenanceMode	false
maintenanceOwners	[]
commissionState	"COMMISSIONED"
numCores	8
numPhysicalCores	4
totalPhysMemBytes	33722032128
1	
hostId	"2e248605-fa0b-4888-8f45-dc85ed0f3802"
ipAddress	"10.0.1.5"
hostname	"nodo2.rodo.com"
rackId	"/default"
hostUrl	"http://nodo2.rodo.com:7180/cmf/hostRedirect/2e248605-fa0b-4888-8f45-dc85ed0f3802"
maintenanceMode	false
maintenanceOwners	[]
commissionState	"COMMISSIONED"
numCores	8
numPhysicalCores	8
totalPhysMemBytes	33722032128
2	
hostId	"a26b5a3a-f670-4edb-956c-fa150bc18dae"
ipAddress	"10.0.1.6"
hostname	"nodo3.rodo.com"
rackId	"/default"
hostUrl	"http://nodo2.rodo.com:7180/cmf/hostRedirect/a26b5a3a-f670-4edb-956c-fa150bc18dae"
maintenanceMode	false
maintenanceOwners	[]
commissionState	"COMMISSIONED"
numCores	8
numPhysicalCores	8
totalPhysMemBytes	29502754816
3	
hostId	"9050cb70-4e23-4ddc-a8d2-966e8597d9ed"
ipAddress	"10.0.1.7"
hostname	"nodo4.rodo.com"
rackId	"/default"
hostUrl	"http://nodo2.rodo.com:7180/cmf/hostRedirect/9050cb70-4e23-4ddc-a8d2-966e8597d9ed"
maintenanceMode	false
maintenanceOwners	[]
commissionState	"COMMISSIONED"
numCores	8
numPhysicalCores	8
totalPhysMemBytes	29502754816

* The command and output from the CM API call ../api/v8/clusters/<githubName>/services

{
  "items" : [ {
    "name" : "hive",
    "type" : "HIVE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://nodo2.rodo.com:7180/cmf/serviceRedirect/hive",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HIVE_HIVEMETASTORES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HIVE_HIVESERVER2S_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hive"
  }, {
    "name" : "zookeeper",
    "type" : "ZOOKEEPER",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://nodo2.rodo.com:7180/cmf/serviceRedirect/zookeeper",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "ZOOKEEPER_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "ZOOKEEPER_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "ZooKeeper"
  }, {
    "name" : "hue",
    "type" : "HUE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://nodo2.rodo.com:7180/cmf/serviceRedirect/hue",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HUE_HUE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Hue"
  }, {
    "name" : "oozie",
    "type" : "OOZIE",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://nodo2.rodo.com:7180/cmf/serviceRedirect/oozie",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "OOZIE_OOZIE_SERVERS_HEALTHY",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Oozie"
  }, {
    "name" : "yarn",
    "type" : "YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://nodo2.rodo.com:7180/cmf/serviceRedirect/yarn",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "YARN_JOBHISTORY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_NODE_MANAGERS_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_RESOURCEMANAGERS_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "YARN_USAGE_AGGREGATION_HEALTH",
      "summary" : "DISABLED"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "YARN (MR2 Included)"
  }, {
    "name" : "spark_on_yarn",
    "type" : "SPARK_ON_YARN",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://nodo2.rodo.com:7180/cmf/serviceRedirect/spark_on_yarn",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "Spark"
  }, {
    "name" : "hdfs",
    "type" : "HDFS",
    "clusterRef" : {
      "clusterName" : "cluster"
    },
    "serviceUrl" : "http://nodo2.rodo.com:7180/cmf/serviceRedirect/hdfs",
    "serviceState" : "STARTED",
    "healthSummary" : "GOOD",
    "healthChecks" : [ {
      "name" : "HDFS_BLOCKS_WITH_CORRUPT_REPLICAS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_CANARY_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_DATA_NODES_HEALTHY",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_FREE_SPACE_REMAINING",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_HA_NAMENODE_HEALTH",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_MISSING_BLOCKS",
      "summary" : "GOOD"
    }, {
      "name" : "HDFS_UNDER_REPLICATED_BLOCKS",
      "summary" : "GOOD"
    } ],
    "configStalenessStatus" : "FRESH",
    "clientConfigStalenessStatus" : "FRESH",
    "maintenanceMode" : false,
    "maintenanceOwners" : [ ],
    "displayName" : "HDFS"
  } ]
}
