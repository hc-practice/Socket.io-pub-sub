## Socket.io & React

### Author: Heather Cherewaty
#### Collaborated with:  Becca Lee & Brent Woodward

### Links and Resources
* [Q server repo](https://github.com/hcherewaty/q-server-hc)
* [API server repo](https://github.com/hcherewaty/api_server)
* [Q server deployed](https://qserver-hc.herokuapp.com)
* [API server deployed](https://api-server-hc.herokuapp.com)
* [Code Sandbox](https://codesandbox.io/s/r7rv0pmj74) 

### Modules
#### `index.js`
##### Exported Values and Methods

### Setup
#### `.env` requirements
* `PORT` - defined in ENV if running locally.
* `MONGODB_URI` - defined in ENV if running locally, otherwise defined in deployed config vars.

#### Running the app
* Q server: `node server.js`
* API server: `node index.js`
* Visit code sandbox link defined in links and resources
* In a new terminal window, run the following commands using httpie:
    * For teams model:
        * POST:   `echo '{"name":"Test"}' | http post <API address>/api/v1/teams`
        * PUT:    `echo '{"name":"TESTING"}' | http put <API address>/api/v1/teams/<insert id here>`
        * DELETE: `http delete <API address>/api/v1/teams/<insert id here>`
    * For players model:
        * POST:   `echo '{"name":"Heather","position":"P","throws":"R","bats":"R","team":"meows"}' | http post <API address>/api/v1/players`
        * PUT:    `echo '{"name":"Heather","position":"P","throws":"L","bats":"L","team":"woofs"}' | http put <API address>/api/v1/players/<insert id here>`
        * DELETE: `http delete <API address>/api/v1/players/<insert id here>`

  
#### Tests
* Tests run within code sandbox.
* Asserted valid components exist.
* Asserted elements exist upon component mount.
* Asserted elements created on state change are do not exist unless state change occurs.