# Admin Guide

This section has hints and tips for instructors on how to run the workshop:

## Lecture material

> Add a link to a box folder here so any lectures or presentations are easily accessible. Below is an example.

For a full set of lectures to be used in this lab check out the link below:

* [Lectures + Box](https://ibm.ent.box.com/folder/121012035949)

## Provisioning environments

> Add a brief description on how to access or spin up environments that the students will use. Below is an example.

Use <https://bluedemos.com/show/2543> to provision instances of the Skytap environment as needed.

* Only IBMers can provision an instance, you'll need to log in with your w3ID.
* You're limited to one request at a time.
* You can schedule how long you want to keep the instance live.
* You'll be emailed a link and a password. Distribute these to the lab attendees.
* There's no cost to running these instances.
* Instances will automatically suspend after 2 hours of inactivity. Just turn them back on to continue.

## Enabling a non-default feature

> Sometimes images are provisioned that don't have everything enabled. Include any steps here for instructors to perform so students don't have to. Below is an example.

Access the `iis-server` VM. Log in with the Linux credentials. Run the following command to change to the Information Server install path:

```bash
cd /opt/IBM/InformationServer/Server/DSODB
```

Edit the `DSODBConfig.cfg` file. set the `DSODBON` value to `1`. It should be the first value at the top of the file. Save your changes and exit your editor.

```ini
DSODBON=1
```

If you're not familiar with `vi` you can use `sed`

```bash
sed -i 's/DSODBON=0/DSODBON=1/g' DSODBConfig.cfg
```

Restart your console:

```bash
cd /opt/IBM/InformationServer/Server/DSODB/bin
./DSAppWatcher.sh -start
```

## Copy the data over

> Add any steps for copying data that will be used during the workshop over to a host machine. Below is an example.

Access the `iis-server` VM. Log in with the Linux credentials. Run the following commands:

Change to the right folder:

```bash
cd /IBMdemos
```

Download the data:

> **NOTE**: the command uses `-O` (not zero)

```bash
wget http://ibm.biz/datastage-standalone-data -O raviga-products.csv
```

Verify the content

```bash
cat raviga-products.csv
```

Should have the following output:

```bash
RAV8XLIGA,90033
...
RAV9XLIGA,90033
```
