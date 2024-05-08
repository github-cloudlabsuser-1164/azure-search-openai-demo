# Backend Application

The backend application for this project is built using [Quart](https://quart.palletsprojects.com/), a Python framework for asynchronous web applications. The backend code is stored in the [``app/backend``](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2FC%3A%2FUsers%2Fazureuser%2Fsource%2Frepos%2Fazure-search-openai-demo%2Fapp%2Fbackend%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Users\azureuser\source\repos\azure-search-openai-demo\app\backend") folder.

## Structure

The backend application is structured into several modules and scripts, including:

- [``auth_init.py``](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fazureuser%2Fsource%2Frepos%2Fazure-search-openai-demo%2Fscripts%2Fauth_init.py%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Users\azureuser\source\repos\azure-search-openai-demo\scripts\auth_init.py"): This script is responsible for initializing the authentication process. It includes functions for creating an application, adding a client secret, and updating environment variables.

- `approaches` folder: This folder contains the classes powering the Chat and Ask tabs. Each class uses a different RAG (Retrieval Augmented Generation) approach.

## Key Functions

Here are some of the key functions in the backend application:

- `create_application`: This function creates an application in the Azure Active Directory.

- `add_client_secret`: This function adds a client secret to the application.

- `create_or_update_application_with_secret`: This function creates or updates an application with a secret.

- `server_app_initial`: This function initializes the server application.

- `server_app_permission_setup`: This function sets up permissions for the server application.

- `client_app`: This function creates a client application.

- `server_app_known_client_application`: This function sets up a known client application for the server application.

## Customization

You can customize the backend application to suit your needs. For example, you can modify the `system_message_chat_conversation` variable in the `chatreadretrieveread.py` file to match your data.

For more details on customizing the backend, refer to the customization guide.

## Deployment

The backend application is deployed using Azure Bicep, as defined in the [``infra/main.bicep``](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2FC%3A%2FUsers%2Fazureuser%2Fsource%2Frepos%2Fazure-search-openai-demo%2Finfra%2Fmain.bicep%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Users\azureuser\source\repos\azure-search-openai-demo\infra\main.bicep") file. The application is hosted on an App Service Plan, and the backend service is configured with various parameters such as location, tags, and app settings.

For more details on deploying the backend, refer to the [``infra/main.bicep``](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2FC%3A%2FUsers%2Fazureuser%2Fsource%2Frepos%2Fazure-search-openai-demo%2Finfra%2Fmain.bicep%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Users\azureuser\source\repos\azure-search-openai-demo\infra\main.bicep") file.

## API

The backend provides an API endpoint for the frontend to interact with. The [`askApi`](command:_github.copilot.openSymbolFromReferences?%5B%7B%22%24mid%22%3A1%2C%22fsPath%22%3A%22c%3A%5C%5CUsers%5C%5Cazureuser%5C%5Csource%5C%5Crepos%5C%5Cazure-search-openai-demo%5C%5Capp%5C%5Cfrontend%5C%5Csrc%5C%5Capi%5C%5Capi.ts%22%2C%22_sep%22%3A1%2C%22external%22%3A%22file%3A%2F%2F%2Fc%253A%2FUsers%2Fazureuser%2Fsource%2Frepos%2Fazure-search-openai-demo%2Fapp%2Ffrontend%2Fsrc%2Fapi%2Fapi.ts%22%2C%22path%22%3A%22%2Fc%3A%2FUsers%2Fazureuser%2Fsource%2Frepos%2Fazure-search-openai-demo%2Fapp%2Ffrontend%2Fsrc%2Fapi%2Fapi.ts%22%2C%22scheme%22%3A%22file%22%7D%2C%7B%22line%22%3A24%2C%22character%22%3A0%7D%5D "app/frontend/src/api/api.ts") function in [``app/frontend/src/api/api.ts``](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2FC%3A%2FUsers%2Fazureuser%2Fsource%2Frepos%2Fazure-search-openai-demo%2Fapp%2Ffrontend%2Fsrc%2Fapi%2Fapi.ts%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Users\azureuser\source\repos\azure-search-openai-demo\app\frontend\src\api\api.ts") sends a POST request to the `/ask` endpoint of the backend service, passing in a `ChatAppRequest` and receiving a `ChatAppResponse`.

For more details on the API, refer to the [``app/frontend/src/api/api.ts``](command:_github.copilot.openRelativePath?%5B%7B%22scheme%22%3A%22file%22%2C%22authority%22%3A%22%22%2C%22path%22%3A%22%2FC%3A%2FUsers%2Fazureuser%2Fsource%2Frepos%2Fazure-search-openai-demo%2Fapp%2Ffrontend%2Fsrc%2Fapi%2Fapi.ts%22%2C%22query%22%3A%22%22%2C%22fragment%22%3A%22%22%7D%5D "c:\Users\azureuser\source\repos\azure-search-openai-demo\app\frontend\src\api\api.ts") file.