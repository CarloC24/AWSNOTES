EC2 101

> EC2 A amazon web service that provides resizable compute capacity in the cloud.
> Amazon EC2 reduces the time required to obtain and boot new server instances to minutes, allowing you to quickly scale capacity, both up and down, as your computing requir ements change.

EC2 Pricing

1. On Demand - Allows you to pay a fixed rate by the hour with no long term commitment.
   > Useful for people who want the low cost and flexibility of Amazon EC2 without any upfront payment and long term commitment
   > Applications with short term, spiky, or unpredictable workloads that cannot be interrupted.
   > Applications being developed or tested on Amazon EC2 for the first time.
2. Reserved - Provides you with a capacity reservation, and offer a significant discount on the hourly changed for an instance. Contract Terms are 1 year to 3 years.
   > Useful for applications with a steady state.
   > Applications that require reserved capacity.
   > Users that are able to make upfront payments to reduce their total computing costs even further.
   > Comes in Different Pricing Types
3. ) Standard Reserved instances
   > These offer up to 75% off. The more you pay upfront and the longer the contract. The greater the discount.
   > 2 .) Convertible Reserved Instances
   > These offer up to 54% off on demand capability to change the attributes of the RI as long as the exchange results in the creation of Reserved Instances of equal or greater value.
   > 3.) Scheduled Reserved Instances
   > These are scheduled to launch within the time windows you reserve. This option allows you to match your capacity reservation to a predictable recurring schedule that only requires a fraction of a day, a week, or a month.
4. Spot - Enables you to bid whatever price you wawnt for instance capacity. Providing for even greater savings if your applications have flexible start and end timesheet.
   > Applications that have flexible start and end times.
   > Applications that are only feasible at very low compute prices.
   > Users with urgent computing needs for large amounts of additional capacity.
5. Dedicated Hosts - Physical EC2 server dedicated for your use. Dedicated Hosts can help you reduce costs by allowing you to use your existing server-bound software licenses.
   > Useful for regulatory requirements that may not support multi-tenant virtualization
   > Great for licensing which does not support multi-tenancy or cloud deployments.
   > Can be purchased On-Demand(hourly.)
   > Can be purchased as a Reservation for up to 70% off the On-Demand price.

EC2 Instance Types

1. F1 (Field Programmable Gate Array) - Geonomics Research, financial analytics, real-time video processing, big data.
2. I3 (High Speed Storage) - NoSQL DBs, Data Warehousing etc.
3. G3 (Graphics Intensive) - Video Encoding/ 3D Application Streaming.
4. H1 (High Disk Throughput) - Map Reduce based workloads, distributed file systems such as HDFS and MapR-FS.
5. T3 (Lowest Cost, General Purpose) - Web Servers/Small DB's
6. D2 (Dense Storage) - Fileservers/Data Warehousing/ Hadoop
7. R5 (Memory Optimized) - Memory Intensive Apps / DB
8. M5 (General Purpose) - Application Servers
9. C5 (Compute Optimized) - CPU Intensive Apps/DBs
10. P3 (Graphics/General Purpose GPU) - Machine Learning, Bitcoin Mining etc.
11. X1 (Memory Optimized) - SAP HANA/ Apache Spark.
12. Z1D (High Compute Capacity and a High Memory Footprint) - Ideal for electronic design automation (EDA) and certain relational database workloads with high per-core licensing costs.
13. A1 (Arm based workloads) - Scale-out workloads such as web servers.
14. U-6tb1 (Bare metal) - Bare metal capabilities that eliminate virtualization overhead.

EC2 Instance Types - Mnemonic

> F - FPGA
> I - IOPS
> G - Graphics
> H - High Disk Througput
> T - Cheap general purpose
> D - Density
> R - Ram
> M - Main Choice for general purpose app
> C - For Compute
> P - Graphics (Pics)
> X - Extreme Memory
> Z - Extreme Memory and CPU
> A - Arm-based workloads
> U - Bare Metal

(FIGHTING DR MC PIXIE IN AU)

Exam Tips 101 EC2

> EC2 instances are virtual machines in the cloud
> Prices vary from ( On-Demand , Reserved (Standard, Convertible , Scheduled), Spot , Dedicated hosts).
> EC2 Instance (FIGHTING DR MC PIXIE IN AU)

### Launching our first ec2 instance.

EC2 Labs
Step 1. Click on EC2 under services.
Step 2. Click on create a new instance.
Step 3. Create a new Amazon Machine Image (AMI) (Amazon Linux 2 AMI).
Step 4. Configuring Instance Detail. (Enable Accidental Shutdown Protection).
Step 5. Configure Storage

- The root volume can only have magnetic or SSD for storage.

Step 6. Add tags!
Step 7. Add Security Groups.

- HTTP is on port 80.
- SSH is in port 22.

Step 8. Add a new key pair!

- Create a new key pair and download it

Step 9. Get you `.pem` file and put it in a directory.
Step 10. Type in `CHMOD 400 <pemfile>`
Step 11. type in the following command `ssh ec2-user@<myipaddress> -i <yourpemfile>`

- Your ip address is your IP address from the EC2 instance.

Step 12. Type in `Sudo su` to gain root access.
Step 13. Type in `yum update -y` to look for operating system updates.
Step 14. Install apache by typing `yum install httpd -y`
Step 15. cd into `/var/www/html`
Step 16. run the command `nano index.html`
