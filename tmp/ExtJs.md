Ext.define(className, members, onClassCreated);

- className is the class name
- members is an object that represents a collection of class members in key-value pairs
- onClassCreated is an optional function callback that is invoked when all dependencies of the defined class are ready and the class itself is fully created. Due to the asynchronous nature of class creation, this callback can be useful in many situations.

Ext.create();

Ext.onReady();

Ext.extend();

Ext.getElementById('');

Ext.MessageBox.alert('', '');