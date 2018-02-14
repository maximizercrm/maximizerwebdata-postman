# Maximizer.Web.Data Postman Collection

A Postman collection containing example requests for the [Maximizer.Web.Data API](https://developer.maximizer.com/doc/maximizerwebdata).

## Getting Started

### Get Postman

If you aren't already using Postman, [you can download it here](https://www.getpostman.com/postman). 

### Import the Collection

To [import the collection into Postman](https://www.getpostman.com/docs/postman/collections/data_formats):
1. In the Postman toolbar, click **Import**.
2. Select the **Import From Link** option.
3. Copy-and-paste the following address into the URL field and click **Import**:
`https://raw.githubusercontent.com/jasontdc/maximizerwebdata-postman/master/maximizerwebdata-postman.json`

### Create an Environment

In order to use the collection, you will need to [create an Environment in Postman](https://www.getpostman.com/docs/postman/environments_and_globals/manage_environments) to store your Maximizer.Web.Data API URL and credentials.

To create a Postman environment:
1. In the toolbar, click **New**.
2. Select **Environment**.
3. Enter a name for the environment, and add your environment variables.
4. Click **Add**.

The following environment variables are required:
- **BaseURL** - The base URL of your Maximizer.Web.Data API, excluding the "/Data.svc" portion. For example, if you are using an on-premise installation of Maximizer, this should look something like `https://example.com/MaximizerWebData`. Or, if you are using Maximizer CRM Live, this should look something like `https://ca1.maximizercrmlive.com/api15`.
- **Database** - The Maximizer database to use, for example `EsconaTutorial` for on-premise or `aa9cfdcbf63b4c518a648475891678d6` for Maximizer CRM Live.
- **UID** - Your Maximizer username. This user must be enabled for Web Access, Service Access, or both.
- **Password** - Your Maximizer password.

If you are using Maximizer CRM Live, you will also need to add the following additional environment variables:
- **VendorId** - Your Maximizer CRM Live vendor ID.
- **AppKey** - The AppKey for your Maximizer CRM Live app.

## Using the Collection

Once you have imported the collection and set up your environment, you should be able to run any request in the collection by selecting it in the *Collections* pane, and clicking **Send**.

### Create, Update, and Delete Requests

Please note that any of the *Create*, *Update*, and *Delete* method requests will make changes to your Address Book data, so you should only run them against a database that you are comfortable making changes to.

Before running the *Update* or *Delete* request for an entity type, you must first run the corresponding *Create* request. When you create an entity, the test script for the request sets an environment variable containing the Key of the entry that was created. The corresponding *Update* and *Delete* requests then update/delete the same entry by referencing the environment variable, so if the environment variable is not set, the requests will fail.

## Contributing

Contributions are welcome! If you find this collection useful and would like to help improve it, please feel free to create a pull request with your changes. If you are unsure about whether or not to create a pull request, you are welcome to create an issue first to discuss your changes.
