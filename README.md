# 1) Basic set up of express.

// Install Dependencies
// Create ./server.js file
// Add a simple get request to the root route to start it off.


// Files changed or created

// package.json (Changed)
 ```javascript
        "dependencies": {
        "bcrypt": "^4.0.1",
        "config": "^3.3.1",
        "express": "^4.17.1",
        "express-validator": "^6.5.0",
        "gravatar": "^1.8.0",
        "jsonwebtoken": "^8.5.1",
        "mongoose": "^5.9.15",
        "request": "^2.88.2"
        },
        "devDependencies": {
        "concurrently": "^5.2.0",
        "nodemon": "^2.0.4"
        }
```

// server.js  (Created)
````javascript
        //  server.js

        // Import express
        const express = require("express");

        // Inherit the power of express
        const server = express();

        // Check for port first or run on 5000
        const PORT = process.env.PORT || "5000";

        // Create a basic get request for testing. (See in post man or browser.)
        server.get("/", (req, res) => { res.send("Server is running") });

        // Set the server to listen on PORT & execute a callback function.
        server.listen(PORT, () => { console.log(`Listening on port ${PORT}...`) })
```
