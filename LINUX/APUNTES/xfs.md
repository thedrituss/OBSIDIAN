`xfs` (X Filesystem)

- [[Journaling]] filesystem known for its high performance, scalability, and reliability.
- Well-suited for large file systems and high-performance workloads.

- Key Features:
	- __High Performance__ : Optimized for sequential read and write operations, ideal for file servers and databases.
	- __Large File System Support__ : Can handle file systems up to 8 exabytes in size.
	- __Reliability__ : Like ext4, uses [[Journaling]] to ensure data integrity in case of system crashes or power failures.
	- __Scalability__ : It can handle a large number of files and directories, making it suitable for file servers with many users.
	- __Flexibility__ : Offers features like online filesystem resizing and real-time defragmentation
- Common Use Cases:
	- __High-Performance Servers__ : Often used on high-performance servers, such as web servers, databases servers, and file servers.
	- __NAS Devices__ : Network-attached storage (NAS) devices often use XFS to store large amounts of data.
	- __Virtual machines__ : XFS can be used as the filesystem for virtual machine disk images.