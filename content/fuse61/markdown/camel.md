## Camel

* Background EIP's
* What does a camel route look like
* Lab - Deploy a camel route

--

![EIP](img/eip-book.png) <!-- .element: fullscreen-size="contain" -->

--

![Camel](img/camel-box.png) <!-- .element: fullscreen-size="contain" -->

--

![Patterns](img/patterns.png) <!-- .element: fullscreen-size="contain" -->

--

![Examples](img/patterns-2.png) <!-- .element: fullscreen-size="contain" -->

--

![components](img/components.png) <!-- .element: fullscreen-size="contain" -->

--

![Context](img/context.png) <!-- .element: fullscreen-size="contain" -->

--

![CBR](img/camel-cbr.png) <!-- .element: fullscreen-size="contain" -->

--

# Lab 3

* Run and deploy the cbr quickstart to jboss fuse
* Ensure Fuse is running
* <code>ps -ax  | grep karaf</code>
* <code>cd $FUSE_HOME/quickstarts/cbr</code>
* <code>mvn clean install</code>
* <code>cd $FUSE_HOME/bin</code>
* <code>./client</code>
* <code>install -s mvn:org.jboss.quickstarts.fuse/cbr/6.1.0.redhat-379</code>