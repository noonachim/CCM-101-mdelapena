# Mission Reflection

This laboratory activity helped me understand why object storage is useful for applications that need to manage a very large amount of unstructured data. For a photo-sharing application, millions of user-uploaded images can grow quickly. Object storage is designed to store objects such as photos, videos, documents, and backups without requiring them to be stored directly inside the web server. Compared with using a traditional block storage hard drive for this purpose, object storage provides a model that is more appropriate for large collections of independent files and can be accessed through a service interface.

Docker made deploying MinIO easier because I did not have to manually install and configure every component of the storage server. With one Docker command, the MinIO image could be downloaded and started as a container. The command also allowed me to expose the required ports and provide environment variables for the login credentials. This made the deployment process organized and repeatable.

A bucket is a logical container used to organize objects in object storage. In this activity, `client-photos` was the bucket created for the client's photo-sharing application. The uploaded sample file became an object inside that bucket.

Large enterprise companies can protect object storage data from physical server failures by maintaining redundant copies of data and using distributed storage systems. They can also use replication, backups, monitoring, and geographically separated infrastructure to reduce the risk of data loss. These approaches help ensure that a hardware failure does not automatically result in the permanent loss of stored data.

Finally, this activity increased my confidence in navigating the Linux command line. I became more comfortable running Docker commands, checking containers, reading service output, and connecting command-line work with a web-based cloud service. The activity showed me how Linux, Docker, and cloud storage technologies can work together in a practical environment.
