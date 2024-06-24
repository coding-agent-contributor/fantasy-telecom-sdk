### Fantasy Telecom SDK Documentation

---

#### Overview

The Fantasy Telecom SDK enables developers to integrate with the Fantasy Telecom platform to manage telecommunications services, including messaging, voice calls, and user management. 

---

### Installation

Install via npm:

```bash
npm install fantasy-telecom-sdk
```

---

### Authentication

```javascript
const { FantasyTelecom } = require('fantasy-telecom-sdk');

const client = new FantasyTelecom({
    apiKey: 'YOUR_API_KEY',
    apiSecret: 'YOUR_API_SECRET',
});
```

---

### Messaging

#### Send SMS

```javascript
client.messaging.sendSMS({
    to: '+1234567890',
    from: '+0987654321',
    message: 'Hello from Fantasy Telecom!'
}).then(response => {
    console.log(response);
}).catch(error => {
    console.error(error);
});
```

#### Check SMS Status

```javascript
client.messaging.getSMSStatus('messageId')
    .then(status => {
        console.log(status);
    }).catch(error => {
        console.error(error);
    });
```

---

### Voice

#### Make a Call

```javascript
client.voice.makeCall({
    to: '+1234567890',
    from: '+0987654321',
    url: 'http://example.com/call-handler'
}).then(response => {
    console.log(response);
}).catch(error => {
    console.error(error);
});
```

#### Get Call Status

```javascript
client.voice.getCallStatus('callId')
    .then(status => {
        console.log(status);
    }).catch(error => {
        console.error(error);
    });
```

---

### User Management

#### Create User

```javascript
client.users.createUser({
    username: 'newuser',
    password: 'password123',
    email: 'newuser@example.com'
}).then(user => {
    console.log(user);
}).catch(error => {
    console.error(error);
});
```

#### Get User Details

```javascript
client.users.getUser('userId')
    .then(user => {
        console.log(user);
    }).catch(error => {
        console.error(error);
    });
```

#### Delete User

```javascript
client.users.deleteUser('userId')
    .then(response => {
        console.log(response);
    }).catch(error => {
        console.error(error);
    });
```

---

### Errors

Errors are returned as standard JavaScript Error objects. Handle them using `catch` blocks or async error handling.

---

### Support

For more information, visit our [documentation](http://fantasy-telecom.example.com/docs) or contact support at support@fantasy-telecom.example.com.

---

This SDK simplifies interaction with the Fantasy Telecom platform, allowing for seamless integration of telecom features into your applications.
