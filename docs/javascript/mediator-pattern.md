# Mediator Pattern

The mediator pattern makes it possible for components to interact with each other through a central point: the mediator.
Instead of letting every objects talk directly to the other objects, resulting in a many-to-many relationship, the object's requests get handled by the mediator. The mediator processes this request, and sends it forward to where it needs to be.

```
class ChatRoom {
    logMessage(user, message) {
        const sender ) user.getName();
        console.log(`${sender}: ${message}`)
    }
}

class User {
    constructor(name, chatroom) {
        this.name = name;
        this.chatroom = chatroom;
    }

    getName() {
        return this.name;
    }

    send(message) {
        this.chatroom.logMessage(this, message);
    }
}

const chatroom = new ChatRoom();

const user1 = new User("John Doe", chatroom);
const user2 = new User("Jane Doe", chatroom);

user1.send("Hi");
user2.send("Hey");

```

A case study of this pattern is in Express.js, applying middlewares. 
We can add logic in a middleware and then call `next` to call the next callback, creating a chain between request and response.

