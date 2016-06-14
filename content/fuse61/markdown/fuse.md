## JBoss Fuse

--

![Fuse](img/fuse-components.png) <!-- .element: fullscreen-size="contain" -->

--

![Enterprise_Community](img/JBossCommunity-EnterpriseDifferentiation.png) <!-- .element: fullscreen-size="contain" -->

--

![Fabric8](img/fabric8.png) <!-- .element: class="noshadow" fullscreen-size="contain" -->

--

## Fuse

* <p>JBoss Fuse is the Red Hat product distro of **Apache ServiceMix, Apache Karaf, Apache Camel, fabric8, Apache Active-MQ**</p>
* <p>open source - free to download and run anywhere at any time</p>
* <p>free $0 developer subscription</p>
* <p>comes with commercial 24/7 production support for 7 years on each version</p>

--

## Karaf 1

* OSGi Container
* Extends OSGi with features for handling/managing OSGi bundles
* Hot deployment support for OSGi bundles
* Dynamic configuration of services
* Dynamic logging back-end provided by Log4J

--

## Karaf 2

* Application provisioning
* CLI console
* Maven repository
* Remote download (http://)
* File system
* Secure remote access via ssh

--

## Lab 1 (Download and install JBoss Fuse)

* Download Fuse http://www.jboss.org/products/fuse/overview/
* https://www.jboss.org/download-manager/file/jboss-fuse-6.1.0.GA-full_zip.zip
* Unzip it
* <p>Go into bin directory and start **./bin/fuse**</p>

--

## Directory Structure

tree -L 1
<pre><code>
├── bin
├── data
├── deploy
├── etc
├── extras
├── fabric
├── lib
├── quickstarts
└── system
</code></pre>

--

## Directory Structure Explained

<pre><code>
├── bin  -> Scripts for starting, stopping and ssh-ing into a karaf container
├── data -> Runtime data folder (logs etc)
├── deploy -> Hot Deployment
├── etc -> Configuration (admin user, http proxies, startup ports)
├── extras -> camel and cxf for external use + CDC
├── fabric -> Used for initial fabric bootstrapping
├── lib -> Bootstrap classpat for karaf
├── quickstarts -> Learning
└── system -> Profile Library
</code></pre>

--

## Lab 2 (User Management, Web Console, Karaf Client)

* Start fuse with <code>./bin/start</code>
* CLI Connect <code>./bin/client</code>
* exit
* <code>ssh admin@localhost -p 8101</code>

--

<pre><code>
1090 [pool-2-thread-3] WARN org.apache.sshd.client.keyverifier.
AcceptAllServerKeyVerifier - Server at /0.0.0.0:8101
presented unverified key:
Password:
Authentication failure
</code></pre>
* <pre><code>vim ./etc/users.properties   </code></pre>

--

Admin Console - http://localhost:8181

--

## Data Directory

* log -> log files
* mavenIndexer -> maven index files
* git -> fabric config
* amq -> active-mq files
* txlog -> transaction log

--

## Maven

* Fuse pulls artefacts from maven
* Almost everything in fuse is identified by a artefact/bundle id and version that relates to its maven co-ordinate
* system directory has the supported artefacts that are shipped and supported by Red Hat
* Production environments can differ in how they use Maven


