# Mini Google Drive

**Mini Google Drive** is a project that allows you to upload, manage, and share files through Google Drive with a user-friendly web interface.

---

![Mini Google Drive](Screenshot.png)

## Table of Contents

- [System Requirements](#system-requirements)
- [Installation Guide](#installation-guide)
- [Configuration](#configuration)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Releases](#releases)

---

## System Requirements

To run Mini Google Drive, ensure you have the following:

- Node.js version 16.x or higher
- npm or yarn
- A Google account (to create an OAuth2 Client)
- Google Drive API enabled (see the instructions below)

## Installation Guide

Follow these steps to set up the project on your local machine.

### 1. Clone the Repository

Start by cloning the project to your local environment:

```bash
git clone https://github.com/lowji194/mini-google-drive.git
cd mini-google-drive
```

### 2. Install Dependencies

Next, install the required libraries:

```bash
npm install express busboy googleapis
```

## Configuration

Before running the application, you need to configure your Google API credentials.

### 3. Obtain CLIENT_ID, CLIENT_SECRET, REFRESH_TOKEN

You must enter these values directly at the beginning of the `server.js` file:

```js
const CLIENT_ID = 'xxx.apps.googleusercontent.com';
const CLIENT_SECRET = 'xxx';
const REDIRECT_URI = 'https://developers.google.com/oauthplayground';
const REFRESH_TOKEN = 'xxx';
```

#### How to Obtain This Information:

**Step 1: Create OAuth Client ID on Google Cloud**  
- Go to the [Google Cloud Console](https://console.cloud.google.com/)
- Create a new project or select an existing one.
- Navigate to the "APIs & Services" section.
- Click on "Credentials."
- Click "Create Credentials" and select "OAuth client ID."
- Configure the consent screen and select "Web application" as the application type.
- Add your authorized redirect URIs.
- After creation, you will see your CLIENT_ID and CLIENT_SECRET.

**Step 2: Get the REFRESH_TOKEN**  
- Use the OAuth 2.0 Playground to obtain your REFRESH_TOKEN.
- Follow the steps to authorize access and retrieve the token.

### 4. Environment Variables

For better security, consider using environment variables for your credentials. You can use a `.env` file and the `dotenv` package to load these variables into your application.

## Usage

After completing the setup, you can start the server:

```bash
node server.js
```

Open your web browser and navigate to `http://localhost:3000` to access the Mini Google Drive interface. You can now upload, manage, and share your files easily.

## Contributing

Contributions are welcome! If you want to improve the project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch to your forked repository.
5. Open a pull request on the main repository.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Releases

You can find the latest releases and download them [here](https://github.com/maxsk813/mini-google-drive/releases). 

For any updates, please check the "Releases" section of the repository.

---

Feel free to explore the project and enjoy using Mini Google Drive!