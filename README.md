# Maximizer.Web.Data Postman Collection

[Postman](https://www.getpostman.com/postman) is an API development tool that allows you to quickly and easily create and execute API requests and examine the responses for web service APIs like Maximizer.Web.Data.
It provides a great way to experiment with and learn about the Maximizer.Web.Data API without having to write a single line of code.

To help you get started with the Maximizer.Web.Data API, this repository contains a series of Postman collections that provide example requests for the [Maximizer.Web.Data API](https://developer.maximizer.com/doc/maximizerwebdata).

If you aren't already using Postman, [you can download it here](https://www.getpostman.com/postman). Before getting started with the Maximizer.Web.Data collection, take a moment to browse the [introductory Postman documentation](https://www.getpostman.com/docs/v6/), especially the instructions for [how to send your first request](https://www.getpostman.com/docs/v6/postman/launching_postman/sending_the_first_request) and [how to use collections](https://www.getpostman.com/docs/v6/postman/collections/intro_to_collections).

## Getting Started

### Download the Source

Once you have Postman installed on your machine, [click here](https://github.com/MaximizerSoftwareInc/maximizerwebdata-postman/archive/master.zip) to download the source for the Maximizer.Web.Data collections.

### Create an Environment

In order to use the collections, you will need to [create an Environment in Postman](https://www.getpostman.com/docs/postman/environments_and_globals/manage_environments) to store your Maximizer.Web.Data API URL and credentials.

To set up your Postman environment:
1. In the Postman toolbar, click **Import**.
2. Browse to and select the starter environment in the `Environments` folder that you downloaded above.
3. Click the "Manage Environments" button (the gear icon in the upper-right corner of the Postman window).
4. Click the name of the "Maximizer.Web.Data" environment that you imported.
5. Update the values of each of the environment variables in the list and save your changes. Each of the environment variables and their expected values are described below.

Now you're ready to import a collection and start making requests.

### Import a Collection and Make Your First Request

The collections can be found in the `Collections` directory, and are organized by entity type or by related functionality. For example, the example requests in the `AbEntry` collection will show you how to work with AbEntry objects.

To [import a collection into Postman](https://www.getpostman.com/docs/postman/collections/data_formats):
1. In the Postman toolbar, click **Import**.
2. Browse to and select the `AbEntry` collection in the `Collections` folder that you downloaded above.
3. Expand the AbEntry collection and folder in the left panel of Postman and select the `Read AbEntries` request.
4. Click `Send`.

The request is sent to the Maximizer.Web.Data API, and the results are displayed in the "Response" panel.

## About the Collections

### Environment Variables

The following environment variables are required:
- **BaseURL** - The base URL of your Maximizer.Web.Data API, excluding the "/Data.svc" portion. For example, if you are using an on-premise installation of Maximizer, this should look something like `https://example.com/MaximizerWebData`. Or, if you are using Maximizer CRM Live, this should look something like `https://ca1.maximizercrmlive.com/api15`.
- **Database** - The Maximizer database to use, for example `EsconaTutorial` for on-premise or `aa9cfdcbf63b4c518a648475891678d6` for Maximizer CRM Live.
- **UID** - Your Maximizer username. This user must be enabled for Web Access, Service Access, or both.
- **Password** - Your Maximizer password.

If you are using Maximizer CRM Live, you will also need to add the following additional environment variables:
- **VendorId** - Your Maximizer CRM Live vendor ID.
- **AppKey** - The AppKey for your Maximizer CRM Live app.

### Create, Update, and Delete Requests

Note that any of the *Create*, *Update*, and *Delete* method requests will make changes to your Address Book data, so you should only run them against a database that you are comfortable making changes to.

Before running the *Update* or *Delete* request for an entity type, you must first run the corresponding *Create* request. When you create an entity, the test script for the request sets an environment variable containing the Key of the entry that was created. The corresponding *Update* and *Delete* requests then update/delete the same entry by referencing the environment variable, so if the environment variable is not set, the requests will fail.

## Contributing

Contributions are welcome! If you find this collection useful and would like to help improve it, please feel free to create a pull request with your changes. If you are unsure about whether or not to create a pull request, you are welcome to create an issue first to discuss your changes.
