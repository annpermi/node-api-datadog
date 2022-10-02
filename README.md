# node-api-datadog

A sample node js api for finding cars and accounts for a dealership,its used here to demonstrate the steps to extend API/ML with your own rest api.

## Steps

**Note**  
`Only rest api with https support can be deployed behind API/ML, make sure to enable https support in your rest api. `  
This sample express app, has https enabled already.

```
//on local
git clone https://github.com/zowe/sample-node-api
cd sample-node-api
npm install
```

`open your docker`

To add service to the dadadog APM:

1. Start agent on you local machine;
2. Run this command in the termanal for you project:

```
//on local
DD_ENV="prod"
DD_LOGS_INJECTION=true
node src/index.js
```

Should see this in the terminal: `http server listening at port 18000`

3. Open yout POSTMAN and make several calls:  
   `http://localhost:18000/accounts/`  
   `http://localhost:18000/accounts/1`  
   `http://localhost:18000/accounts/1/cars/`

4. Restart Datadog agent on mac;
5. Open datadog dashboard webpage, refresh the page. Go to APM and you will see now
6. Now you can dashboard to your service with different widjects
