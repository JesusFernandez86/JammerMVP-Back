# Jammer MVP Backend
Backend of Final project from a 1200 hours bootcamp in web development in https://codehouse.academy/

Jammer MVP is a centralized platform designed to connect property owners, tenants, and refurbishment professionals. This repository contains the backend services developed using Node.js, Express, and MySQL, with Firebase integration for real-time chat and document management.

## Features

- **User Management:** Handles authentication and authorization for different user roles.
- **Property Management:** Allows owners to manage multiple properties and associated documents.
- **Real-Time Chat:** Facilitates communication between users via Firebase.
- **Document Uploads:** Enables secure uploading and storage of documents related to properties and agreements.

## Technologies Used

- **Node.js & Express:** Server-side runtime and framework.
- **MySQL:** Relational database for data persistence.
- **Firebase:** Real-time database for chat functionality and document storage.
- **Sequelize:** ORM for database interactions.

## Installation and Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/JesusFernandez86/JammerMVP-Back.git
   cd JammerMVP-Back
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Configure environment variables:**
   - Create a `.env` file in the root directory.
   - Add the following variables:
     ```
     DB_HOST=your_database_host
     DB_USER=your_database_user
     DB_PASS=your_database_password
     DB_NAME=your_database_name
     FIREBASE_API_KEY=your_firebase_api_key
     FIREBASE_AUTH_DOMAIN=your_firebase_auth_domain
     FIREBASE_PROJECT_ID=your_firebase_project_id
     FIREBASE_STORAGE_BUCKET=your_firebase_storage_bucket
     FIREBASE_MESSAGING_SENDER_ID=your_firebase_messaging_sender_id
     FIREBASE_APP_ID=your_firebase_app_id
     ```

4. **Run database migrations:**
   ```bash
   npx sequelize-cli db:migrate
   ```

5. **Start the server:**
   ```bash
   npm start
   ```
   The server should now be running on `http://localhost:3000`.

## API Endpoints

- **Authentication:**
  - `POST /api/register` - Register a new user.
  - `POST /api/login` - Authenticate a user and retrieve a token.

- **Properties:**
  - `GET /api/properties` - Retrieve a list of properties.
  - `POST /api/properties` - Add a new property.
  - `PUT /api/properties/:id` - Update property details.
  - `DELETE /api/properties/:id` - Delete a property.

- **Chat:**
  - `GET /api/chat/:propertyId` - Retrieve chat messages for a property.
  - `POST /api/chat/:propertyId` - Send a new message.

- **Documents:**
  - `POST /api/documents/:propertyId` - Upload a document.
  - `GET /api/documents/:propertyId` - List documents for a property.
  - `DELETE /api/documents/:propertyId/:docId` - Delete a document.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m "Add your feature description"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request detailing your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or suggestions, please contact me.
