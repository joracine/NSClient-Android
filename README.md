=NS Client

[![Join the chat at https://gitter.im/nightscout/NSClient-Android](https://badges.gitter.im/nightscout/NSClient-Android.svg)](https://gitter.im/nightscout/NSClient-Android?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

**What does NS Client do?**

It connects to your Nightscout server, and provides an means for applications to connect to it.
 
**Does it have a GUI?**

Only debugging GUI, for developers. None for regular. Maybe someone can build and contribute back? :)
 
**How do I use it?**
 
It sends broadcasts with data from nightscout. So you can write an app that listen to the broadcasts and can do stuff with it. You can send broadcasts back to write back to the MongoDB database.
 
**Any other features?**

You can emulate xDrip apps with NS Client if you don't have access to a physical device. It supports the xDrip extension for DanaAps too (OpenAPS implementation for DanaR pump).
 
**Do you code sample/examples?**

Look at the and of MainActivity, in source.
 
**And how do I test that it works?**

When you upload a treatment, you should recieve it through a treatment broadcast, once it is written to MongoDB.
 
**I need to write retry logic for connection failures and similar errors?**

No. NSClient queues requests, and retries undelivered records once the client reconnects to the Nightscout server.
