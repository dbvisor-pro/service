# General Principies

For a comprehensive understanding of how the database processing occurs, we recommend reading the article linked below. As a brief overview, the processing involves three main components, as outlined in the [Getting Started](https://outline.bridge.digital./../Getting%20Started.md) page:


1. **Service:** This is the public website where you manage rules.
2. **Server (DBVisor Agent):** This is a private application installed on your server, responsible for processing the database.
3. **Client (DBVisor Client):** Another private application that developers install on their computers to download the database.


Now, let's delve into the server side (DBVisor Agent) and how it processes the database:


1. **Installation and Linking:** After installing the application on your server and linking it with the service (refer to the **[Installation](https://outline.bridge.digital./Installation.md)** section), you need to add a new database and configure it (see [Database Management](https://outline.bridge.digital./../DBVisor%20Agent/Database%20Management.md) section).
2. **Database Configuration:** Once a database is added, you can configure rules on the service and specify them accordingly.
3. **Processing Workflow:** The DBVisor Agent sends a request to the service to check if there is a scheduled database, as per the rules defined on the service. If a scheduled database is found, it initiates the processing. The processing workflow is as follows:
   * Attempt to obtain a backup from the specified source (see Dump Methods section) and download/dump it.
   * After the download/dump is completed, it creates a temporary database on the internal DB server.
   * The backup is then imported into this temporary database.
   * The processing of rules is initiated.
   * A dump is created from the temporary database.
   * The temporary database is dropped.
4. **Key Points:**
   * Database processing is not parallel, meaning that while one database is processing, another scheduled database goes into the queue.
   * The DBVisor Agent sends reports and logs to the service, which can be viewed at the database edit page on the service side.


 ![The diagram that explains the general life cycle of processing databases](uploads/7721627a-f600-462f-aa6a-f5a2a2bcd82e/cc9ae746-d3aa-4d59-ae49-eafe8dd647b0/DB%20(2).jpg)


\