Rete.js  [![Build Status](https://travis-ci.org/retejs/rete.svg?branch=master)](https://travis-ci.org/retejs/rete) 
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=retejs_rete&metric=alert_status)](https://sonarcloud.io/dashboard?id=retejs_rete)
[![Join the chat at https://gitter.im/retejs/Lobby](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/retejs/Lobby)
====
#### JavaScript framework for visual programming

![rete logo](https://i.imgur.com/rydGu6B.png)

Introduction
----
THIS IS A CUSTOM RETE.JS. If you need original - go to rete.js(https://github.com/retejs/rete)  

**Rete** is a modular framework for visual programming. **Rete** allows you to create node-based editor directly in the browser. You can define nodes and workers that allow users to create instructions for processing data in your editor without a single line of code.

CHANGES
----
- New events:
  - dblclick - double click with the left mouse button not changing zoom now, but you can use it on a nodes
  - connectionclick - now you can click to connections

How to use an event: 
I. 'connectionclick': 
  1.  In the file with rete settings add:
      ```
      editor.on('renderconnection', (connection) => {
        const { el } = connection;
        el.classList.add('connection-wrapper');
      });
      ```

      and then you can use `connectionclick` event
      ```
        editor.on('connectionclick', (connection) => {
          // your code
          console.log('connectionclick');
        }
      ```
  2. In `ComponentFileWhereReteInit.vue` you could setup css styles for `connection-wrapper` class. 
      Example:
      ```
        .connection-wrapper {
          svg:hover {
            cursor: pointer;
          }
        }
      ```

Documentation
----
Check the [docs](https://rete.js.org/#/docs) and learn about the components and capabilities.

Examples
----
[Flow-based programming](https://codepen.io/Ni55aN/pen/xzgQYq)

[Events (tasks)](https://codepen.io/Ni55aN/pen/MOYPEz)

[Modules](https://codepen.io/Ni55aN/pen/QOEbEW)

[Programming a Messenger Bot](https://codepen.io/Ni55aN/pen/rpOKNb)

[3D Car configurator](https://codesandbox.io/embed/9jp88p1jpy?view=preview)

License
----
[MIT](http://opensource.org/licenses/MIT)

[Donate](http://rete.js.org/#support)
---