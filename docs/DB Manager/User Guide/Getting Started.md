# Getting Started

# **Overview**

\nOverview

This application serves several key purposes:


1. **Protect Your Client's Data:** The application facilitates the removal of sensitive information, such as customer addresses, emails, bills, etc., from databases. Not only does it cleanse the data, but it also substitutes it with predefined patterns. This enables developers to work with realistic data sizes while safeguarding against data leaks. Additionally, access to databases can be restricted based on user groups.
2. **Ease of Sharing:** Developers can effortlessly keep their databases current, saving time on tasks like sharing and backup. Users have the flexibility to configure the frequency at which the application cleans data, and updated databases can be downloaded as needed.
3. **Versatile Usage:** In addition to the aforementioned features, this application is valuable for preparing your application or website for demos, presentations, and more.

The primary advantage of our service is that we do not retain any sensitive client data in our databases. We exclusively store database schemas devoid of client data, ensuring the security of your information.


# Architecture

From a technical standpoint, our system consists of three applications::


1. **DBvisor Service:** This is the main website where users interact. It allows configuration of rules, access to database configurations, and viewing important logs..
2. **DBvisor Agent:** This application is installed on your server and is responsible for processing and backing up databases.
3. **DBvisor Client:** Installed locally on developers' computers, this application simplifies logging in and downloading the latest backup.


:::warning
**Important Note:** All database credentials and data are stored on your server side. The service side exclusively retains database schemas and the server's IP address 

:::