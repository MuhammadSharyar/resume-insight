# Resume Insight Web App

This web app allows users to upload multiple CSV files and ask AI-powered questions about the data within those files. The app leverages various technologies to provide a seamless and efficient experience.

## Table of Contents

- [Tech Stack](#tech-stack)
- [Features](#features)
- [Installation](#installation)
- [Environment Variables](#environment-variables)
- [Usage](#usage)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Tech Stack

- **Frontend:**
  - React.js
  - Next.js
  - Tailwind CSS

- **Backend:**
  - Node.js
  - Express.js
  - Drizzle ORM
  - PostgreSQL

- **AI & Data:**
  - OpenAI (for AI-powered questions)
  - Langchain (for natural language processing)
  - Pinecone DB (for vector database)

- **Storage & Authentication:**
  - AWS S3 (for file storage)
  - Clerk Auth (for user authentication)

## Features

- **CSV Upload:** Users can upload multiple CSV files simultaneously.
- **AI Query:** Users can ask AI-powered questions about the uploaded CSV files.
- **User Authentication:** Secure authentication using Clerk Auth.
- **Data Storage:** Uploaded CSV files are stored securely on AWS S3.
- **Vector Database:** Pinecone DB is used for vector search capabilities.
- **Responsive UI:** Built with Tailwind CSS for a modern and responsive design.

## Installation

### Prerequisites

- Node.js (v14.x or later)
- PostgreSQL
- AWS Account (for S3)
- OpenAI API Key
- Pinecone DB Account
- Clerk Account

### Clone the Repository

```bash
git clone https://github.com/your-username/csv-query-web-app.git
cd csv-query-web-app
```

### Install Dependencies

```bash
npm install
```

### Set Up Environment Variables

Create a `.env.local` file in the root directory and add the following environment variables:

```plaintext
NEXT_PUBLIC_CLERK_FRONTEND_API=<Your Clerk Frontend API Key>
CLERK_API_KEY=<Your Clerk API Key>
NEXT_PUBLIC_OPENAI_API_KEY=<Your OpenAI API Key>
AWS_ACCESS_KEY_ID=<Your AWS Access Key ID>
AWS_SECRET_ACCESS_KEY=<Your AWS Secret Access Key>
AWS_S3_BUCKET_NAME=<Your S3 Bucket Name>
PINECONE_API_KEY=<Your Pinecone API Key>
PINECONE_ENVIRONMENT=<Your Pinecone Environment>
DATABASE_URL=<Your PostgreSQL Database URL>
```

### Database Migration

Ensure that your PostgreSQL database is set up. Use Drizzle ORM for migrations:

```bash
npx drizzle-kit up
```

## Usage

### Running the Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to view the app.

### Building for Production

```bash
npm run build
```

### Starting the Production Server

```bash
npm start
```

## Deployment

This app can be deployed on any cloud platform that supports Node.js and PostgreSQL. For AWS, you can use services like EC2 for the backend, RDS for the database, and S3 for storage.

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License.
