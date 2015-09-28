To get started, ensure you have the latest JDK installed, and download Maven from:

  http://maven.apache.org/

Then run "mvn -Dmaven.test.skip=true clean install -U" to compile the software. For now you have to disable the tests as they are not working yet. You can also run "mvn site:site" to generate a website with useful information like JavaDocs. The outputs are under the target/ directory.

Alternatively, just import the project using your IDE. IntelliJ has Maven integration once you tell it where to find your unzipped Maven install directory.

Now try running one of the example apps:

  cd Examples
  mvn compile
  mvn exec:java -Dexec.mainClass=org.casinocoin.examples.ForwardingService -Dexec.args="<insert a casinocoin address here>"

It will download the block chain and eventually print a Casinocoin address. If you send coins to it, it will forward them on to the address you specified when you started the ForwardingService. Note that this example app does not use checkpointing, so the initial chain sync will be pretty slow.
You can make an app that starts up and does the initial sync much faster by including a checkpoints file; see the documentation for more info on this.

Now you are ready to follow the tutorial:

   https://github.com/casinocoin/CasinocoinJ/wiki/Getting-Started! 

