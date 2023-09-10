# Appwrite-Migration-Tool

Appwrite-Migration-Tool is a versatile utility package designed to simplify database migrations and data seeding for the [Appwrite](https://appwrite.io/) platform. It offers an easy-to-use interface for managing migrations and seeding data in your Appwrite project, all while ensuring performance, maintainability, and scalability.

## Features

- **Database Migrations:** Seamlessly create and manage database migrations for your Appwrite project. Keep your database schema up-to-date with ease.

- **Data Seeding:** Populate your Appwrite database with sample data using configurable seeders. Perfect for development, testing, and staging environments.

- **Customizable Configuration:** Configure your Appwrite-Migrate package to fit your project's specific needs, including Appwrite API endpoint, project ID, API key, migration paths, seed paths, and more.

- **TypeScript Support:** Appwrite-Migrate is built with TypeScript, providing type definitions for a better development experience.

- **Easy Setup:** The package includes an initialization script that guides you through the configuration process, making it simple to get started.

## Installation

To get started, install the package using your package manager of choice (npm, pnpm, or yarn):

```bash
npm install appwrite-migration-tool

# or

pnpm install appwrite-migration-tool

# or

yarn add appwrite-migration-tool

```
## Usage
-----

### Configuration

Before using the package, you need to configure it with your Appwrite settings. Run the following command to set up the configuration:

`npx appwrite-migration-tool init`

This command will prompt you to provide the following information:

-   Appwrite endpoint
-   Project ID
-   API key
-   Paths for migrations and seeds

### Database Migrations

To create a new migration, use the following command:

`npx migrate:make migration_name`

Replace `migration_name` with a descriptive name for your migration.

To run pending migrations, execute:

`npx migrate`

### Seeding Data

To create a seed file, use the following command:

`npx seed:make SeedFileName`

Replace `SeedFileName` with the name of your seed file.

To seed data into your Appwrite database, run:

`npx seed SeedFileName`

### User Factory

To generate fake user data, you can use the provided user factory utility. Here's an example:

javascriptCopy code

```
const { createMultipleFakeUsers } = require('appwrite-migration-tool/lib/utils/userFactory');

createMultipleFakeUsers(10); // Creates 10 fake user profiles
```

Contributing
------------

Contributions are welcome! Feel free to open issues, suggest improvements, or submit pull requests on our [Appwrite Migration Tool](https://github.com/upperdo/appwrite-migration-tool).

License
-------

This project is licensed under the MIT License. See the [LICENSE](https://github.com/upperdo/appwrite-migration-tool/blob/main/LICENSE) file for details.