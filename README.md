## Text-to-Speech-Module

### Pre-requisites

- pyttsx3 is a text-to-speech conversion library in Python.
  Unlike alternative libraries, it works offline, and is compatible
  with both Python 2 and 3.
- The OS module in python provides functions for interacting
  with the operating system. OS, comes under Python's standard utility modules.
  
### Install Libraries

- pip install pyttsx3 

PS: OS library should be available before hand with python distribution.

### Import Libraries

         <code>import pyttsx3
         import os</code>

### Lets dive into the code

         <code>engine = pyttsx3.init('sapi5')</code>
<br>
sapi5 is a referance to male voice for windows. Init() is a function to create an object<br> 
of pyttsx3 type.

         <code>voices = engine.getProperty('voices')</code>
<br>         
Gets the current value of an engine property.

         <code>engine.setProperty('voice',voices[0].id)</code>
<br>
Queues a command to set an engine property. The new property value affects all utterances<br>
queued after this command.

         <code>def speak(audio):
                   engine.say(audio)
                   engine.runAndWait()</code>
<br>
It is an user defined function. The pyttsx3 function say() pronounces the actual audio.<br>
The runAndWait() function blocks while processing all currently queued commands. <br>
Invokes callbacks for engine notifications appropriately. <br>
Returns when all commands queued before this call are emptied from the queue.
  
         <code>remember = open('input.txt','r')</code>
<br>
Here our text file is opened and stored in 'remember'

         <code>speak(remember.read())</code>
 <br>
Now finally we call our function.


