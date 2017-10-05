{
  "timestamp" : "2017-10-05T13:18:38.527Z",
  "clusters" : [ {
    "name" : "cluster",
    "displayName" : "Cluster 1",
    "version" : "CDH5",
    "fullVersion" : "5.11.0",
    "services" : [ {
      "name" : "hive",
      "type" : "HIVE",
      "config" : {
        "items" : [ {
          "name" : "hive_metastore_database_host",
          "value" : "ip-172-31-0-35.us-west-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "hive_metastore_database_name",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "hive_metastore_database_password",
          "value" : "hive_password",
          "sensitive" : true
        }, {
          "name" : "hive_service_config_safety_valve",
          "value" : "<property>\n  <name>hive.server2.authentication</name>\n  <value>KERBEROS</value>\n</property>\n<property>\n  <name>hive.server2.authentication.kerberos.principal</name>\n  <value>hive/_HOST@AGNOSTIC.COM</value>\n</property>\n<property>\n <name>hive.stats.ndv.error</name>\n <value>5.0</value>\n</property>",
          "sensitive" : false
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn",
          "sensitive" : false
        }, {
          "name" : "sentry_service",
          "value" : "sentry",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hive-GATEWAY-1d5ebd2b0df1b3b2fa19e60d48650a06",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-6a79581cc19fe61b273f42c00cb81ea7",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "d976a169-9cf7-4957-9261-7bce157e02b3"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-c084d065ceb016d0ac41d016cb34a0db",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "cee41973-7d13-443c-8408-c29701fd1fec"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-GATEWAY-f0cc68c416857cfbe6b81cf071aa3363",
        "type" : "GATEWAY",
        "hostRef" : {
          "hostId" : "dbc99722-1d71-46cd-b0eb-48f2859bdee3"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-GATEWAY-BASE"
        }
      }, {
        "name" : "hive-HIVEMETASTORE-1d5ebd2b0df1b3b2fa19e60d48650a06",
        "type" : "HIVEMETASTORE",
        "hostRef" : {
          "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6zl7m3v8vgn7fxr9s5dw80pkn",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVEMETASTORE-BASE"
        }
      }, {
        "name" : "hive-HIVESERVER2-1d5ebd2b0df1b3b2fa19e60d48650a06",
        "type" : "HIVESERVER2",
        "hostRef" : {
          "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3w7t3ss8wdg5qq8qpv69w54zo",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hive-HIVESERVER2-BASE"
        }
      } ],
      "displayName" : "Hive",
      "roleConfigGroups" : [ {
        "name" : "hive-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hive-HIVEMETASTORE-BASE",
        "displayName" : "Hive Metastore Server Default Group",
        "roleType" : "HIVEMETASTORE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hive_metastore_java_heapsize",
            "value" : "5294260224",
            "sensitive" : false
          }, {
            "name" : "hive_metastore_server_max_message_size",
            "value" : "529426022",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hive-HIVESERVER2-BASE",
        "displayName" : "HiveServer2 Default Group",
        "roleType" : "HIVESERVER2",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ {
            "name" : "hiveserver2_enable_impersonation",
            "value" : "false",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_driver_memory",
            "value" : "966367641",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_cores",
            "value" : "4",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_executor_memory",
            "value" : "4031748505",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_driver_memory_overhead",
            "value" : "102",
            "sensitive" : false
          }, {
            "name" : "hiveserver2_spark_yarn_executor_memory_overhead",
            "value" : "678",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hive-WEBHCAT-BASE",
        "displayName" : "WebHCat Server Default Group",
        "roleType" : "WEBHCAT",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hive"
        },
        "config" : {
          "items" : [ ]
        }
      } ],
      "replicationSchedules" : [ ]
    }, {
      "name" : "zookeeper",
      "type" : "ZOOKEEPER",
      "config" : {
        "items" : [ {
          "name" : "enableSecurity",
          "value" : "true",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "zookeeper-SERVER-6a79581cc19fe61b273f42c00cb81ea7",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "d976a169-9cf7-4957-9261-7bce157e02b3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "5cvzcfk6y8uh1w49frpvor9hw",
            "sensitive" : true
          }, {
            "name" : "serverId",
            "value" : "3",
            "sensitive" : false
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-c084d065ceb016d0ac41d016cb34a0db",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "cee41973-7d13-443c-8408-c29701fd1fec"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6ft3a3zay1g2gpbxe6xunhmg3",
            "sensitive" : true
          }, {
            "name" : "serverId",
            "value" : "1",
            "sensitive" : false
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      }, {
        "name" : "zookeeper-SERVER-f0cc68c416857cfbe6b81cf071aa3363",
        "type" : "SERVER",
        "hostRef" : {
          "hostId" : "dbc99722-1d71-46cd-b0eb-48f2859bdee3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6y87apji4mefit7bk8npqe7e4",
            "sensitive" : true
          }, {
            "name" : "serverId",
            "value" : "2",
            "sensitive" : false
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "zookeeper-SERVER-BASE"
        }
      } ],
      "displayName" : "ZooKeeper",
      "roleConfigGroups" : [ {
        "name" : "zookeeper-SERVER-BASE",
        "displayName" : "Server Default Group",
        "roleType" : "SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "zookeeper"
        },
        "config" : {
          "items" : [ ]
        }
      } ]
    }, {
      "name" : "hue",
      "type" : "HUE",
      "config" : {
        "items" : [ {
          "name" : "database_host",
          "value" : "ip-172-31-0-35.us-west-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "database_password",
          "value" : "hue_password",
          "sensitive" : true
        }, {
          "name" : "database_type",
          "value" : "mysql",
          "sensitive" : false
        }, {
          "name" : "hive_service",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "hue_webhdfs",
          "value" : "hdfs-NAMENODE-c084d065ceb016d0ac41d016cb34a0db",
          "sensitive" : false
        }, {
          "name" : "oozie_service",
          "value" : "oozie",
          "sensitive" : false
        }, {
          "name" : "sentry_service",
          "value" : "sentry",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-1d5ebd2b0df1b3b2fa19e60d48650a06",
        "type" : "HUE_LOAD_BALANCER",
        "hostRef" : {
          "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "azzedc7g12ulp3jitm1cgqqi0",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_LOAD_BALANCER-BASE"
        }
      }, {
        "name" : "hue-HUE_SERVER-1d5ebd2b0df1b3b2fa19e60d48650a06",
        "type" : "HUE_SERVER",
        "hostRef" : {
          "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
        },
        "config" : {
          "items" : [ {
            "name" : "navmetadataserver_cmdb_password",
            "value" : "98989549-db1f-46bc-afe9-4928e15aad9c",
            "sensitive" : true
          }, {
            "name" : "role_jceks_password",
            "value" : "aqr69bt7l0vm781d2qxhvvhox",
            "sensitive" : true
          }, {
            "name" : "secret_key",
            "value" : "nZkQuzhEkT6TvzeCBwUoGtoJF5lvBQ",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-HUE_SERVER-BASE"
        }
      }, {
        "name" : "hue-KT_RENEWER-1d5ebd2b0df1b3b2fa19e60d48650a06",
        "type" : "KT_RENEWER",
        "hostRef" : {
          "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "erov8g0ouo3xiaahqs4ouwu5b",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hue-KT_RENEWER-BASE"
        }
      } ],
      "displayName" : "Hue",
      "roleConfigGroups" : [ {
        "name" : "hue-HUE_LOAD_BALANCER-BASE",
        "displayName" : "Load Balancer Default Group",
        "roleType" : "HUE_LOAD_BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hue-HUE_SERVER-BASE",
        "displayName" : "Hue Server Default Group",
        "roleType" : "HUE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ {
            "name" : "hue_http_port",
            "value" : "18888",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hue-KT_RENEWER-BASE",
        "displayName" : "Kerberos Ticket Renewer Default Group",
        "roleType" : "KT_RENEWER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hue"
        },
        "config" : {
          "items" : [ ]
        }
      } ]
    }, {
      "name" : "oozie",
      "type" : "OOZIE",
      "config" : {
        "items" : [ {
          "name" : "hive_service",
          "value" : "hive",
          "sensitive" : false
        }, {
          "name" : "mapreduce_yarn_service",
          "value" : "yarn",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "oozie-OOZIE_SERVER-1d5ebd2b0df1b3b2fa19e60d48650a06",
        "type" : "OOZIE_SERVER",
        "hostRef" : {
          "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_health_suppression_oozie_server_scm_health",
            "value" : "true",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "355jdqlscs4sdvt5sza58nmsh",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "oozie-OOZIE_SERVER-BASE"
        }
      } ],
      "displayName" : "Oozie",
      "roleConfigGroups" : [ {
        "name" : "oozie-OOZIE_SERVER-BASE",
        "displayName" : "Oozie Server Default Group",
        "roleType" : "OOZIE_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "oozie"
        },
        "config" : {
          "items" : [ {
            "name" : "oozie_database_host",
            "value" : "ip-172-31-0-35.us-west-2.compute.internal",
            "sensitive" : false
          }, {
            "name" : "oozie_database_password",
            "value" : "oozie",
            "sensitive" : true
          }, {
            "name" : "oozie_database_type",
            "value" : "mysql",
            "sensitive" : false
          }, {
            "name" : "oozie_database_user",
            "value" : "oozie",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "yarn",
      "type" : "YARN",
      "config" : {
        "items" : [ {
          "name" : "hadoop_secure_web_ui",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "hdfs_service",
          "value" : "hdfs",
          "sensitive" : false
        }, {
          "name" : "rm_dirty",
          "value" : "false",
          "sensitive" : false
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "80",
          "sensitive" : false
        }, {
          "name" : "yarn_service_cgroups",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "yarn_service_lce_always",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "zk_authorization_secret_key",
          "value" : "nQOematg9V2G6UZEm4Uw8O5xPGCxlu",
          "sensitive" : true
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "yarn-JOBHISTORY-f0cc68c416857cfbe6b81cf071aa3363",
        "type" : "JOBHISTORY",
        "hostRef" : {
          "hostId" : "dbc99722-1d71-46cd-b0eb-48f2859bdee3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "7yiamju2cwrzvq3g2o0dm72ws",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-JOBHISTORY-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-6a79581cc19fe61b273f42c00cb81ea7",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "d976a169-9cf7-4957-9261-7bce157e02b3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "8efl6oi3j02f8235t6fgy67pc",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-c084d065ceb016d0ac41d016cb34a0db",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "cee41973-7d13-443c-8408-c29701fd1fec"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "3bcrdil1zqmwmw3d5ygh401f7",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-BASE"
        }
      }, {
        "name" : "yarn-NODEMANAGER-f0cc68c416857cfbe6b81cf071aa3363",
        "type" : "NODEMANAGER",
        "hostRef" : {
          "hostId" : "dbc99722-1d71-46cd-b0eb-48f2859bdee3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "966a0opx6a9oyp211obwgcil5",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-NODEMANAGER-1"
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-c084d065ceb016d0ac41d016cb34a0db",
        "type" : "RESOURCEMANAGER",
        "hostRef" : {
          "hostId" : "cee41973-7d13-443c-8408-c29701fd1fec"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_id",
            "value" : "52",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "78w8cq6x903d2camb90exh7qb",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "yarn-RESOURCEMANAGER-BASE"
        }
      } ],
      "displayName" : "YARN (MR2 Included)",
      "roleConfigGroups" : [ {
        "name" : "yarn-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "mapred_reduce_tasks",
            "value" : "12",
            "sensitive" : false
          }, {
            "name" : "mapred_submit_replication",
            "value" : "3",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-JOBHISTORY-BASE",
        "displayName" : "JobHistory Server Default Group",
        "roleType" : "JOBHISTORY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-1",
        "displayName" : "NodeManager Group 1",
        "roleType" : "NODEMANAGER",
        "base" : false,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1600",
            "sensitive" : false
          }, {
            "name" : "rm_io_weight",
            "value" : "800",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm,/mnt/disco1/yarn/nm,/mnt/disco2/yarn/nm",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs,/mnt/disco1/yarn/container-logs,/mnt/disco2/yarn/container-logs",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "6",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "13706",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-NODEMANAGER-BASE",
        "displayName" : "NodeManager Default Group",
        "roleType" : "NODEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "rm_cpu_shares",
            "value" : "1600",
            "sensitive" : false
          }, {
            "name" : "rm_io_weight",
            "value" : "800",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_heartbeat_interval_ms",
            "value" : "100",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_local_dirs",
            "value" : "/yarn/nm,/mnt/disco1/yarn/nm,/mnt/disco2/yarn/nm",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_log_dirs",
            "value" : "/yarn/container-logs,/mnt/disco1/yarn/container-logs,/mnt/disco2/yarn/container-logs",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_cpu_vcores",
            "value" : "6",
            "sensitive" : false
          }, {
            "name" : "yarn_nodemanager_resource_memory_mb",
            "value" : "8048",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "yarn-RESOURCEMANAGER-BASE",
        "displayName" : "ResourceManager Default Group",
        "roleType" : "RESOURCEMANAGER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "yarn"
        },
        "config" : {
          "items" : [ {
            "name" : "yarn_scheduler_maximum_allocation_mb",
            "value" : "13706",
            "sensitive" : false
          }, {
            "name" : "yarn_scheduler_maximum_allocation_vcores",
            "value" : "6",
            "sensitive" : false
          } ]
        }
      } ]
    }, {
      "name" : "hdfs",
      "type" : "HDFS",
      "config" : {
        "items" : [ {
          "name" : "dfs_encrypt_data_transfer_algorithm",
          "value" : "AES/CTR/NoPadding",
          "sensitive" : false
        }, {
          "name" : "dfs_ha_fencing_cloudera_manager_secret_key",
          "value" : "tuZ5cTsuQVyAnnV8XIKYyEjHxw2Orq",
          "sensitive" : true
        }, {
          "name" : "fc_authorization_secret_key",
          "value" : "yGxluAfz9VkG9JhFEpD99mcVmyF1Rg",
          "sensitive" : true
        }, {
          "name" : "hadoop_secure_web_ui",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "hadoop_security_authentication",
          "value" : "kerberos",
          "sensitive" : false
        }, {
          "name" : "hadoop_security_authorization",
          "value" : "true",
          "sensitive" : false
        }, {
          "name" : "http_auth_signature_secret",
          "value" : "wffB3W8kldWdiPrA8eMqNNoKbbGyTZ",
          "sensitive" : true
        }, {
          "name" : "rm_dirty",
          "value" : "false",
          "sensitive" : false
        }, {
          "name" : "rm_last_allocation_percentage",
          "value" : "20",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "hdfs-BALANCER-6a79581cc19fe61b273f42c00cb81ea7",
        "type" : "BALANCER",
        "hostRef" : {
          "hostId" : "d976a169-9cf7-4957-9261-7bce157e02b3"
        },
        "config" : {
          "items" : [ ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-BALANCER-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-6a79581cc19fe61b273f42c00cb81ea7",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "d976a169-9cf7-4957-9261-7bce157e02b3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "wpd46i7xi31asp7430mxa4et",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-c084d065ceb016d0ac41d016cb34a0db",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "cee41973-7d13-443c-8408-c29701fd1fec"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "rd061ntgtwl6wblkab2u2tf0",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-DATANODE-f0cc68c416857cfbe6b81cf071aa3363",
        "type" : "DATANODE",
        "hostRef" : {
          "hostId" : "dbc99722-1d71-46cd-b0eb-48f2859bdee3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "26y3tvf7dkxn2e45m4es8u5go",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-DATANODE-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-6a79581cc19fe61b273f42c00cb81ea7",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "d976a169-9cf7-4957-9261-7bce157e02b3"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "89mb1g8pjfjy0buwq6xg5gm17",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-c084d065ceb016d0ac41d016cb34a0db",
        "type" : "FAILOVERCONTROLLER",
        "hostRef" : {
          "hostId" : "cee41973-7d13-443c-8408-c29701fd1fec"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "6ryr64gizqdp7dc21yikyi7f7",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-FAILOVERCONTROLLER-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-6a79581cc19fe61b273f42c00cb81ea7",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "d976a169-9cf7-4957-9261-7bce157e02b3"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/mnt/disco1/dfs/jn",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "2a4v6m4z8jxjs1bmho26rlvay",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-c084d065ceb016d0ac41d016cb34a0db",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "cee41973-7d13-443c-8408-c29701fd1fec"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "bwv1u46a41aulwrpbt48rclcx",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-JOURNALNODE-f0cc68c416857cfbe6b81cf071aa3363",
        "type" : "JOURNALNODE",
        "hostRef" : {
          "hostId" : "dbc99722-1d71-46cd-b0eb-48f2859bdee3"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/mnt/disco1/dfs/jn",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "aszk5dbezaltiqtfho4b6wka4",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-JOURNALNODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-6a79581cc19fe61b273f42c00cb81ea7",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "d976a169-9cf7-4957-9261-7bce157e02b3"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true",
            "sensitive" : false
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1",
            "sensitive" : false
          }, {
            "name" : "namenode_id",
            "value" : "59",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "alwxefkgdzc9w8mvf9g9fd3im",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      }, {
        "name" : "hdfs-NAMENODE-c084d065ceb016d0ac41d016cb34a0db",
        "type" : "NAMENODE",
        "hostRef" : {
          "hostId" : "cee41973-7d13-443c-8408-c29701fd1fec"
        },
        "config" : {
          "items" : [ {
            "name" : "autofailover_enabled",
            "value" : "true",
            "sensitive" : false
          }, {
            "name" : "dfs_federation_namenode_nameservice",
            "value" : "nameservice1",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_quorum_journal_name",
            "value" : "nameservice1",
            "sensitive" : false
          }, {
            "name" : "namenode_id",
            "value" : "54",
            "sensitive" : false
          }, {
            "name" : "role_jceks_password",
            "value" : "bmnucusxv7g6ishlhz46269lu",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "hdfs-NAMENODE-BASE"
        }
      } ],
      "displayName" : "HDFS",
      "roleConfigGroups" : [ {
        "name" : "hdfs-BALANCER-BASE",
        "displayName" : "Balancer Default Group",
        "roleType" : "BALANCER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-DATANODE-BASE",
        "displayName" : "DataNode Default Group",
        "roleType" : "DATANODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "datanode_java_heapsize",
            "value" : "1073741824",
            "sensitive" : false
          }, {
            "name" : "dfs_data_dir_list",
            "value" : "/dfs/dn,/mnt/disco1/dfs/dn,/mnt/disco2/dfs/dn",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_data_dir_perm",
            "value" : "700",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_failed_volumes_tolerated",
            "value" : "1",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_http_port",
            "value" : "1006",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_max_locked_memory",
            "value" : "4294967296",
            "sensitive" : false
          }, {
            "name" : "dfs_datanode_port",
            "value" : "1004",
            "sensitive" : false
          }, {
            "name" : "rm_cpu_shares",
            "value" : "400",
            "sensitive" : false
          }, {
            "name" : "rm_io_weight",
            "value" : "200",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-FAILOVERCONTROLLER-BASE",
        "displayName" : "Failover Controller Default Group",
        "roleType" : "FAILOVERCONTROLLER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_client_use_trash",
            "value" : "true",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-HTTPFS-BASE",
        "displayName" : "HttpFS Default Group",
        "roleType" : "HTTPFS",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-JOURNALNODE-BASE",
        "displayName" : "JournalNode Default Group",
        "roleType" : "JOURNALNODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_journalnode_edits_dir",
            "value" : "/dfs/jn",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-NAMENODE-BASE",
        "displayName" : "NameNode Default Group",
        "roleType" : "NAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "dfs_name_dir_list",
            "value" : "/dfs/nn,/mnt/disco1/dfs/nn",
            "sensitive" : false
          }, {
            "name" : "dfs_namenode_servicerpc_address",
            "value" : "8022",
            "sensitive" : false
          }, {
            "name" : "namenode_bind_wildcard",
            "value" : "true",
            "sensitive" : false
          } ]
        }
      }, {
        "name" : "hdfs-NFSGATEWAY-BASE",
        "displayName" : "NFS Gateway Default Group",
        "roleType" : "NFSGATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "hdfs-SECONDARYNAMENODE-BASE",
        "displayName" : "SecondaryNameNode Default Group",
        "roleType" : "SECONDARYNAMENODE",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "hdfs"
        },
        "config" : {
          "items" : [ {
            "name" : "fs_checkpoint_dir_list",
            "value" : "/dfs/snn",
            "sensitive" : false
          } ]
        }
      } ],
      "replicationSchedules" : [ ],
      "snapshotPolicies" : [ ]
    }, {
      "name" : "sentry",
      "type" : "SENTRY",
      "config" : {
        "items" : [ {
          "name" : "hdfs_service",
          "value" : "hdfs",
          "sensitive" : false
        }, {
          "name" : "sentry_server_database_host",
          "value" : "ip-172-31-0-35.us-west-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "sentry_server_database_password",
          "value" : "sentry_password",
          "sensitive" : true
        }, {
          "name" : "sentry_service_admin_group",
          "value" : "hive,impala,hue,solr,kafka,sergiosadaniowski",
          "sensitive" : false
        }, {
          "name" : "zookeeper_service",
          "value" : "zookeeper",
          "sensitive" : false
        } ]
      },
      "roles" : [ {
        "name" : "sentry-SENTRY_SERVER-1d5ebd2b0df1b3b2fa19e60d48650a06",
        "type" : "SENTRY_SERVER",
        "hostRef" : {
          "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
        },
        "config" : {
          "items" : [ {
            "name" : "role_jceks_password",
            "value" : "aiw8zv82x2jsn3cpx0lwjixau",
            "sensitive" : true
          } ]
        },
        "roleConfigGroupRef" : {
          "roleConfigGroupName" : "sentry-SENTRY_SERVER-BASE"
        }
      } ],
      "displayName" : "Sentry",
      "roleConfigGroups" : [ {
        "name" : "sentry-GATEWAY-BASE",
        "displayName" : "Gateway Default Group",
        "roleType" : "GATEWAY",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "sentry"
        },
        "config" : {
          "items" : [ ]
        }
      }, {
        "name" : "sentry-SENTRY_SERVER-BASE",
        "displayName" : "Sentry Server Default Group",
        "roleType" : "SENTRY_SERVER",
        "base" : true,
        "serviceRef" : {
          "clusterName" : "cluster",
          "serviceName" : "sentry"
        },
        "config" : {
          "items" : [ {
            "name" : "sentry_server_java_heapsize",
            "value" : "268435456",
            "sensitive" : false
          } ]
        }
      } ]
    } ],
    "parcels" : [ {
      "product" : "CDH",
      "version" : "5.11.0-1.cdh5.11.0.p0.34",
      "stage" : "DISTRIBUTED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    }, {
      "product" : "CDH",
      "version" : "5.11.0-1.cdh5.11.0.p0.34",
      "stage" : "ACTIVATED",
      "clusterRef" : {
        "clusterName" : "cluster"
      }
    } ],
    "uuid" : "d8a37546-8480-4755-9d2e-136081696b29"
  } ],
  "hosts" : [ {
    "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f",
    "ipAddress" : "172.31.0.35",
    "hostname" : "ip-172-31-0-35.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "cee41973-7d13-443c-8408-c29701fd1fec",
    "ipAddress" : "172.31.0.87",
    "hostname" : "ip-172-31-0-87.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "d976a169-9cf7-4957-9261-7bce157e02b3",
    "ipAddress" : "172.31.10.186",
    "hostname" : "ip-172-31-10-186.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  }, {
    "hostId" : "dbc99722-1d71-46cd-b0eb-48f2859bdee3",
    "ipAddress" : "172.31.3.178",
    "hostname" : "ip-172-31-3-178.us-west-2.compute.internal",
    "rackId" : "/default",
    "config" : {
      "items" : [ ]
    }
  } ],
  "users" : [ {
    "name" : "__cloudera_internal_user__hue-HUE_SERVER-1d5ebd2b0df1b3b2fa19e60d48650a06",
    "roles" : [ "ROLE_NAVIGATOR_ADMIN" ],
    "pwHash" : "393253a22a98b84cb0e94818e97d0b5d09252ba1275981856999bf21f2100e0f",
    "pwSalt" : -8581633910717860733,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-ACTIVITYMONITOR-1d5ebd2b0df1b3b2fa19e60d48650a06",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "53e617292b46e0b6fa3e3c301ac870d4e111ecba49786efb6071b8efad0a76df",
    "pwSalt" : 2176683177986427949,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-EVENTSERVER-1d5ebd2b0df1b3b2fa19e60d48650a06",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "af5a3d1c9f223aba69104fe27c92898a8cb988fb8fc992814054f3d06827f82c",
    "pwSalt" : -8577375280390476683,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-HOSTMONITOR-1d5ebd2b0df1b3b2fa19e60d48650a06",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "7590d2b08b725fde5f489bff968a979a5a9cd753535c19da6be75bf21d66843c",
    "pwSalt" : -7453348850090541764,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-REPORTSMANAGER-1d5ebd2b0df1b3b2fa19e60d48650a06",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "651a6e3776f0bf5181cc6b450c9b26b2aeb553b65adde8a8e36e1ac8bc4d3374",
    "pwSalt" : -11919989884482233,
    "pwLogin" : true
  }, {
    "name" : "__cloudera_internal_user__mgmt-SERVICEMONITOR-1d5ebd2b0df1b3b2fa19e60d48650a06",
    "roles" : [ "ROLE_USER" ],
    "pwHash" : "48fd96e1823a3e3e76716721a0be44936db05447cd2bbe51435444236731b296",
    "pwSalt" : 7969482535205617804,
    "pwLogin" : true
  }, {
    "name" : "admin",
    "roles" : [ "ROLE_LIMITED" ],
    "pwHash" : "1fe8562c1fb1b907ebbb6fbc32b236b46238ffb82ebabcb0a886f9568a391b19",
    "pwSalt" : 5562772943232982362,
    "pwLogin" : true
  }, {
    "name" : "minotaur",
    "roles" : [ "ROLE_CONFIGURATOR" ],
    "pwHash" : "f8bb702c1616b692a4347045bcf33517f3ba3ff6b0c0d5bd72357b87a823a89f",
    "pwSalt" : -7223391634129856426,
    "pwLogin" : true
  }, {
    "name" : "sergiosadaniowski",
    "roles" : [ "ROLE_ADMIN" ],
    "pwHash" : "55f29ef82af9e4d37ad6bde0e2ee06d8bc0ddd3bce6b28c80b598ff582632223",
    "pwSalt" : -133772725083195399,
    "pwLogin" : true
  } ],
  "versionInfo" : {
    "version" : "5.12.1",
    "buildUser" : "jenkins",
    "buildTimestamp" : "20170818-0807",
    "gitHash" : "9bdee611802535491d400e03c98ef694a2c77d0a",
    "snapshot" : false
  },
  "managementService" : {
    "name" : "mgmt",
    "type" : "MGMT",
    "config" : {
      "items" : [ ]
    },
    "roles" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-1d5ebd2b0df1b3b2fa19e60d48650a06",
      "type" : "ACTIVITYMONITOR",
      "hostRef" : {
        "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "7a05uiuvczv7yvm3ymitlqqme",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ACTIVITYMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-1d5ebd2b0df1b3b2fa19e60d48650a06",
      "type" : "ALERTPUBLISHER",
      "hostRef" : {
        "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "3wnblhj9k7hpw3mj1tetjc2nu",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-ALERTPUBLISHER-BASE"
      }
    }, {
      "name" : "mgmt-EVENTSERVER-1d5ebd2b0df1b3b2fa19e60d48650a06",
      "type" : "EVENTSERVER",
      "hostRef" : {
        "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "3ha5454aeiuuoh3mvmuufmp5y",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-EVENTSERVER-BASE"
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-1d5ebd2b0df1b3b2fa19e60d48650a06",
      "type" : "HOSTMONITOR",
      "hostRef" : {
        "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "8tcw7lbqi0g09aw48f63syo9b",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-HOSTMONITOR-BASE"
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-1d5ebd2b0df1b3b2fa19e60d48650a06",
      "type" : "REPORTSMANAGER",
      "hostRef" : {
        "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "4b6do2ae7345n1nhnijr379qn",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-REPORTSMANAGER-BASE"
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-1d5ebd2b0df1b3b2fa19e60d48650a06",
      "type" : "SERVICEMONITOR",
      "hostRef" : {
        "hostId" : "42c55724-15cf-4db1-99fd-7fd68a370c4f"
      },
      "config" : {
        "items" : [ {
          "name" : "role_jceks_password",
          "value" : "5u94eaxkm0qmrvh9s72dgdq3e",
          "sensitive" : true
        } ]
      },
      "roleConfigGroupRef" : {
        "roleConfigGroupName" : "mgmt-SERVICEMONITOR-BASE"
      }
    } ],
    "displayName" : "Cloudera Management Service",
    "roleConfigGroups" : [ {
      "name" : "mgmt-ACTIVITYMONITOR-BASE",
      "displayName" : "Activity Monitor Default Group",
      "roleType" : "ACTIVITYMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_database_host",
          "value" : "ip-172-31-0-35.us-west-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "firehose_database_name",
          "value" : "amon",
          "sensitive" : false
        }, {
          "name" : "firehose_database_password",
          "value" : "amon_password",
          "sensitive" : true
        }, {
          "name" : "firehose_database_user",
          "value" : "amon",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-ALERTPUBLISHER-BASE",
      "displayName" : "Alert Publisher Default Group",
      "roleType" : "ALERTPUBLISHER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-EVENTSERVER-BASE",
      "displayName" : "Event Server Default Group",
      "roleType" : "EVENTSERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-HOSTMONITOR-BASE",
      "displayName" : "Host Monitor Default Group",
      "roleType" : "HOSTMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-NAVIGATOR-BASE",
      "displayName" : "Navigator Audit Server Default Group",
      "roleType" : "NAVIGATOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-NAVIGATORMETASERVER-BASE",
      "displayName" : "Navigator Metadata Server Default Group",
      "roleType" : "NAVIGATORMETASERVER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    }, {
      "name" : "mgmt-REPORTSMANAGER-BASE",
      "displayName" : "Reports Manager Default Group",
      "roleType" : "REPORTSMANAGER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "headlamp_database_host",
          "value" : "ip-172-31-0-35.us-west-2.compute.internal",
          "sensitive" : false
        }, {
          "name" : "headlamp_database_name",
          "value" : "rman",
          "sensitive" : false
        }, {
          "name" : "headlamp_database_password",
          "value" : "rman_password",
          "sensitive" : true
        }, {
          "name" : "headlamp_database_user",
          "value" : "rman",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-SERVICEMONITOR-BASE",
      "displayName" : "Service Monitor Default Group",
      "roleType" : "SERVICEMONITOR",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ {
          "name" : "firehose_non_java_memory_bytes",
          "value" : "1610612736",
          "sensitive" : false
        } ]
      }
    }, {
      "name" : "mgmt-TELEMETRYPUBLISHER-BASE",
      "displayName" : "Telemetry Publisher Default Group",
      "roleType" : "TELEMETRYPUBLISHER",
      "base" : true,
      "serviceRef" : {
        "serviceName" : "mgmt"
      },
      "config" : {
        "items" : [ ]
      }
    } ]
  },
  "managerSettings" : {
    "items" : [ {
      "name" : "AD_USE_SIMPLE_AUTH",
      "value" : "false",
      "sensitive" : false
    }, {
      "name" : "CLUSTER_STATS_START",
      "value" : "10/23/2012 0:30",
      "sensitive" : false
    }, {
      "name" : "KDC_ADMIN_PASSWORD",
      "value" : "BQIAAAA/AAEADEFHTk9TVElDLkNPTQAMY2xvdWRlcmEtc2NtAAAAAVnVDxUBABcAEPUP/L7ALX9ztuxIQA4TPFEAAAAB",
      "sensitive" : true
    }, {
      "name" : "KDC_ADMIN_USER",
      "value" : "cloudera-scm@AGNOSTIC.COM",
      "sensitive" : false
    }, {
      "name" : "KDC_HOST",
      "value" : "ip-172-31-0-35.us-west-2.compute.internal",
      "sensitive" : false
    }, {
      "name" : "KRB_DOMAIN",
      "value" : "",
      "sensitive" : false
    }, {
      "name" : "KRB_ENC_TYPES",
      "value" : "arcfour-hmac",
      "sensitive" : false
    }, {
      "name" : "KRB_MANAGE_KRB5_CONF",
      "value" : "true",
      "sensitive" : false
    }, {
      "name" : "PUBLIC_CLOUD_STATUS",
      "value" : "ON_PUBLIC_CLOUD",
      "sensitive" : false
    }, {
      "name" : "REMOTE_PARCEL_REPO_URLS",
      "value" : "https://archive.cloudera.com/cdh5/parcels/5.11.0/",
      "sensitive" : false
    }, {
      "name" : "SECURITY_REALM",
      "value" : "AGNOSTIC.COM",
      "sensitive" : false
    } ]
  },
  "allHostsConfig" : {
    "items" : [ {
      "name" : "rm_enabled",
      "value" : "true",
      "sensitive" : false
    } ]
  },
  "peers" : [ ],
  "hostTemplates" : {
    "items" : [ ]
  }
}