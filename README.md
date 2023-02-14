# cassidy-likay-collaboration

Our Team:

Cassidy Lawrence (Node.js)

Lindokuhle Mgoqi (MySQL)




CleverCloud Creds

Host: bq5pcsf88bwozdmxinbq-mysql.services.clever-cloud.com

Database Name: bq5pcsf88bwozdmxinbq

User: udjcoe9yqoh1q6kk

Password: e9SwES8izswcH7btGfn4

Port: 3306

Connection URL: mysql://udjcoe9yqoh1q6kk:e9SwES8izswcH7btGfn4@bq5pcsf88bwozdmxinbq-mysql.services.clever-cloud.com:3306/bq5pcsf88bwozdmxinbq




Routes.js

module.exports = app => {
    const tutorial = require("../controllers/controller.js");
  
    var router = require("express").Router();
  
    router.post("/", tutorial.create);

    router.get("/", tutorial.findAll);

    router.get("/published", tutorial.findAllPublished);

    router.get("/:id", tutorial.findOne);
  
    router.put("/:id", tutorial.update);
  
    router.delete("/:id", tutorial.delete);

    router.delete("/", tutorial.deleteAll);
  
    app.use('/api/tutorial', router);
  };
