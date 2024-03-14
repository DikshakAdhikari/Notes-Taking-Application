# Note Taking Application

**Introduction**  

This is an advanced Notes making app consists of all CRUD operations with secure authentication using JWT. Client implemented using Next.js, Typescript and Tailwind Css, Server implemented using Nest.js 

**Features**  

This application provides users with the following features  


- Authentication using **JWT Tokens and Passport.js**  
- Provide all CRUD operations in app
- Server is Highly opinionated. Follows the design paradigm of "convention over configuration".

## Frontend Deployment Steps at Vercel- 

- Go to vercel -> add new -> project
- Choose appropriate Github repository to deploy
- Locate the directory inside github that needs to deploy
- Give environment variables if used any
- Give your deployment project a unique name
- Now we're ready for our frontend deployment

## Backend Deployment Steps at AWS Lambda using CDK-

**Setting Up the Infrastructure with AWS CDK**

- In the lib/my-stack.ts file, begin with the core of your setup: the Lambda function.

```bash
  // LambdaNestStack in stack.ts
const apiNestHandlerFunction = new Function(this, "ApiNestHandler", {
  code: Code.fromAsset("api/dist"), // 👈 This is crucial
  runtime: Runtime.NODEJS_18_X,
  handler: "main.handler",
  environment: {}, // 👈 You might need env variables
});
```

  



