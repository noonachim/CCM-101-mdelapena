# Types of Cloud Storage

Cloud storage can be divided into three primary types: Block Storage, File Storage, and Object Storage.

| Storage Type | Description | Primary Use Case | Cloud Provider Example |
|---|---|---|---|
| Block Storage | Stores data as fixed-size blocks that can be independently managed and attached to a virtual machine. | Operating system disks, databases, and applications that require low-latency storage. | AWS EBS |
| File Storage | Stores data in a hierarchical file and folder structure that can be accessed by multiple systems over a network. | Shared files, team directories, application files, and content repositories. | AWS EFS |
| Object Storage | Stores data as objects together with metadata and a unique identifier, rather than as blocks or a traditional folder-based file system. | Large amounts of unstructured data such as images, videos, backups, and documents. | AWS S3 |

## Recommendation for the Client

Object Storage is well suited for the client's photo-sharing application because user-uploaded images are unstructured data and may grow to millions of files. It is designed for scalable storage and easy access to large collections of objects, making it appropriate for storing photos separately from temporary web server containers.
