![Logo](https://mend-toolkit-resources-public.s3.amazonaws.com/img/mend-io-logo-horizontal.svg)

# PS-Helicopter-Report
Provided in this repository is the JAR file for Mend Helicopter Reports. These reports give an overall understanding of a Global Organization in Mend, and helps provide a clear picture of alerts, and which ones are reachable.

### Examples
In order to run this tool a few parameters need to be specified on the command line or in a params.config file. In order to run the helicopter report with command line options, you will need to specify:

```shell
java -jar ./wss-helicopter-view-1.3.jar -userKey <your_user_key> -globalOrgToken <your_global_org_token> [-threadCount <num_of_threads> -url saas.whitsesourcesoftware.com]
```

> __*NOTE:*__ If you do not specify a url then it will default to **saas&#46;whitesourcesoftware&#46;com**

<br />
If you would like the tool to get its configuration from a configuration file, then you will need to create a ``params.config`` file in the same directory as where you are running the command from. Here is an example params.config file.

```conf
userKey=<your_user_key>
globalOrgToken=<your_global_organization_token>
threadCount=num_of_threads          #Optional
url=saas.whitesourcesoftware.com    #Optional
```

From there, all you need to do is run: 
```shell
java -jar ./wss-helicopter-view-1.3.jar
```

### Memory
If you have some projects that have a large amount of data, then it might be best to increase the amount of memory allocated to the Java Virtual Machine. To do this you can run:
```shell
java -Xmx12G -jar wss-helicopter-view-1.3.jar
```

Where 12G means 12 GB.