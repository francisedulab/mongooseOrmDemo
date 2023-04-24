## How to use

- Clone the project
- change directory and npm install
- Add the following code in app.js file and run the code



```sh

const mongoose = require('mongoose');                                              // Importing Mongoose 

async function connect(){

    await mongoose.connect('mongodb://localhost:27017/interns');                  // Making connect to mongodb by using connect method
    const Cat = mongoose.model('Cat', { name: String , color : String});          // Creating collection or model by using model method of mongooes

    const peppa = new Cat({ name: 'peppa' });                                     // Creating a instance of Cat model 
    const kitty = new Cat({ name: 'kitty' ,color: 'black' });                     // Creating a instance of Cat model
    peppa.save().then(() => console.log('peppa Created'));                        // Calling a save method to inserting data into model
    kitty.save().then(() => console.log('kitty Created'));                        // Calling a save method to inserting data into model
}

connect();                                                                        // connect function called 

```
