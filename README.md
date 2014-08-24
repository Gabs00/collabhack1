collabhack1
===========

### Demonstrating the eaze of firebase with Gonzo chat

Once you've set up your firebase data store, and have the data URL, it just takes three steps to begin sending and receivng data 
with firebase

1. Connect to your firebase using the steps below:
  `var fb = new Firebase(/path/to/data/store);`
2. Set up an event listener on the data store to check for new data additions, this will listen to and respond to additions:
    fb.on('child_added', function(snapshot) {
            var message = snapshot.val();
          displayChatMessage(message.name, message.text);
    });
3. Create an object with data that you wish to store and push to your data store with:
  `data.push(obj)`