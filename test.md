# use
* name
* options 

Register a plugin. The plugin will usually add some actions to the Seneca instance. You can optionally provide some options for the plugin (for example, database connection details

---

# ready
* ready 

Provide a callback to be executed once all the plugins registered up this point are initialized. You use this to wait for database connections to establish.

---

# add
* pattern
* action 

Add a new action to the Seneca instance. The action is triggered when an object matching the pattern is submitted to Seneca using the act method.

---

# act
* object
* callback 

Invoke an action using an object. The action pattern that matches the object in the most specific manner will be invoked.

---

# make
* entity-canon
* properties 

Create an instance of a data entity. The entity-canon defines the kind of entity to create ('product', 'sys/user',...) and the properties (optional)
define the values of some of the entity fields.

---

# export
* name 

Returns a reference to a named object. These are provided by some plugins so that you can integrate into other systems (for example, providing a middleware function for express)

---

# log.level
* [ entry ... ]

Create a log entry using the Seneca logging system. Use this inside plugins as it handles all the context information (time, which plugin, etc) for you. Levels are debug, info, warn, error, fatal.

---

# pin
* pin-pattern 

Creates a convenience object that can call actions directly using method calls.

---

# close
* done 

Calls the close:name action on all plugins that have registered this action. You can use this to close database connections after tests complete to ensure the process ends.

---

# client
* options 

Calls the role:transport,cmd:client action from the transport plugin.

---

# listen
* options 

Calls the role:transport,cmd:listen action from the transport plugin.
