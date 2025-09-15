# <img src="https://objectreef.dev/reef.png" width="25" />  The Octopus Basic
This is the Octopus application written in ObjectReef technology. It is used to organize work independently or in a team. You can manage tasks, task lists, notes, and documentation. The application also includes a built-in messenger for conversations between team members. The code is released under the terms of the MIT license, the content of which you can find [here](./LICENSE.md).



## Service launch
The most convinient way to develop ObjectReef solutions is to use [Visual Studio Code](https://code.visualstudio.com/) with [Reefs Language support extension](https://marketplace.visualstudio.com/items?itemName=humandialog.object-reef).

To run the service on the local machine, type the following command at the command line in the project directory:  
`reef dev`  


ObjectReef will try to start the web service by opening an unsecured port **1996**. If the port is not used by any other process, then the message `local service:  http://localhost:1996/` will appear, indicating that the service is ready for use and the running `reef dev` process is in interactive mode. If the primary port is busy, another free random port will be used.

Before we move on to testing, the source code still needs to be compiled, so let's press 
**<kbd>Shift+Ctrl+B</kbd>** to run vscode build task and choose `ObjectReef: build` from the dropdown list.

This command reads the project settings file **.refs** and all source files with extension **.reef**. The compiler creates intermediate executable code, executed by ObjectReef run-time environment.  
After a successfull compilation you should see the message:  
`SUCCESS: Compiled: 29 classes, 281 operations, 9 invariants, 30 constraints, 0 functions. Parsed 23 source files.`


Although the application model is ready the service does not have any data yet. We can quickly fix this by calling this operations:  
`app/InitUsers`

`sys/login?u=alice`

`app/InitSample`


At the end of the preparation, it is worth saving the data just created, so as not to call  this operation in the future.  
`sys/save`

Now that our service is ready to use, you can send HTTP requests to it using any client, i.e. cURL, Postman or using one of the sample fronteds listed above.

## About ObjectReef
ObjectReef is a complete platform to design, test and deploy any high performance backend services. It ensures robust, scalability and security with zero tech debt. That Model-driven developement solution offers you everything you need to develop, maintain, integrate and run the software without the advanced technical knowledge.

No matter, if you are creating the simple or complex and critical product, ObjectReef is the platform, that simplifies the process of delivering the application backend. It has never been so quick and so robust.

More info you'll find at [https://objectreef.dev/](https://objectreef.dev/)

 