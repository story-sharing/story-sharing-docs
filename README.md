# Story Sharing

### Links

* Github: https://github.com/story-sharing
* Firebase: https://console.firebase.google.com/project/story-share-app
* Firebase hosting: https://story-share-app.web.app/

### Terminology

* Story: an ordered list of scenes
* Scene: an element of a story with audio, imagery
* Creator(s): The user(s) who made the story
* Series: an ordered list of related/episodic stories
* Studio: the section in an app where creators construct stories
* Group: a group has a name, icon and a list of users who can see stories
* Public: a story that is published for everyone to see

### Database Structure

* stories: a collection of public stories
  * createdAt: timestamp the story was created
  * title: name of the story
  * owners: a list of user IDs who created the story
  * scenes: a list of scenes in the story
    * backgroundColour: a hex colour for the background of the UI
    * title: name of the scene
    * audio: link to audio
    * text: text representation of audio
* groups: a collection of private groups
  * createdAt: timestamp the group was created
  * title: name of the group
  * image: link to image
  * messages: a collection of private chat messages
    * createdAt: the timestamp the message was created
    * text: the message text
    * author: the user who created the message
      * uid: the ID of the user
      * name: Te name of the user
      * photoURL: link to user photo
      * email: email of user
   * stories: a collection of private stories
* users: a collection of user accounts
  * admin: boolean to say if admin
  * username: name of user
  * email: email of user
