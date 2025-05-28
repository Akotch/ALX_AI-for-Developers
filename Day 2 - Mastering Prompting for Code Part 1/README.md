## Tasks

##### 0\. Generating Code with Context and System Constraints

You are working on a Node.js project that uses the Express web framework and the Mongoose library for interacting with a MongoDB database. You need to create a new API endpoint that retrieves a user by their ID.

Write a prompt that uses **Contextual Prompting** to inform the AI about the project’s technology stack (Node.js, Express, Mongoose) and the specific task (get user by ID from MongoDB). Additionally, use **System Prompting** to instruct the AI to return _only_ the JavaScript code for the Express route handler function, with no extra text or explanation.

---

##### 1\. Getting a Code Review from a Specific Role with Context

You have written the following TypeScript code snippet to read the entire content of a file into memory. You are concerned about its memory usage and efficiency when dealing with very large files.

```
import * as fs from 'fs';
import * as path from 'path';

function processLargeFile(filepath: string): string | null {
    try {
        const fileContent: string = fs.readFileSync(filepath, 'utf-8');
        console.log(`Read ${fileContent.length} characters.`);
        // Assume further processing of fileContent happens here
        return fileContent;
    } catch (error: any) {
        console.error(`Error processing file: ${error.message}`);
        return null;
    }
}

const fileToProcess = path.join(__dirname, 'very_large_data.txt');
const processedData = processLargeFile(fileToProcess);
```

---

Write a prompt that you would send to the AI to get a code review of the _provided_ TypeScript code snippet.

- Use **Role Prompting** to ask for the review from the perspective of a “Senior Node.js Performance Specialist” known for optimizing I/O operations and memory usage in Node.js applications.
- Use **Contextual Prompting** to mention that the script processes a potentially “very large” file and that your specific concerns are “memory usage” and “efficiency” when dealing with such files. Include the TypeScript code snippet above within your prompt.

---
