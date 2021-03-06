# MCNW Project Run
## Installation and Configuration

To install application, make sure npm is installed, clone the repository and run the following when in the project's root directory:
```
npm install
```
To start the server, if all dependencies are in place, simply run:
```
npm start
```

The following environment variables can be set to modify the server's configuration:

| Variable Name     | Options                       | Default               | Effect|
| :-------------:   |:-------------:                | :-----:               |:----:|
|  NODE_ENV         | ['test', 'production']        | 'production'          |Attempts to connect to test database, actions are safe for testing|
| LOAD_LOCAL_INFILE | [false, true]                 |   false               |Switches to use `LOAD DATA LOCAL INFILE` statement over `INSERT` for bulk uploads |
| DATABASE_HOST     | Host URL of MySQL database    |    localhost          |-|
| DATABASE_URL      | Name of database at Host      |   module_selection    |-|
| DATABASE_USER     | Name of user to connect as    |    root               |-|
| DATABASE_PASS     | Password to connect with      |    ''                 |-|
| MAIL_USER         | Username of gmail account     |    moduleselectionnoreply@gmail.com | Tries to use this account to send out reset password e-mails|
| MAIL_PASSWORD     | Password of gmail account     |    NOT SHOWN HERE |-|



## Documentation

For documentaion, internal functions are commented in source, and exposed function documentation can be generated by running:
```
npm run doc
```
Documentation will be generated to the doc/ folder in the root of the project directory. The **apidoc** folder will contain documentation for the server's HTTP API and **jsdoc** folder
will contain public functions exposed in either front-end or server-side components.

For documentation of the server's API only, a single command can be run as follows:
```
npm run apidoc
```
and likewise for jsdoc:
```
npm run jsdoc
```

## Testing

To Run tests of the server application and receive a coverage report, run:
```
npm run coverage
```

For end-to-end testing of front end interaction and Functionality, the server **must** be started with the NODE_ENV variable set to test and then the following cqn be run safely:
```
npm run protractor
```
>**Note**
> - Results of client-side testing may vary on different environments due to uncontrollable factors such as operating system, web driver version etc..



