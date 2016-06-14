## What is fabric

* <p>Based on the upstream project **fabric8**</p> <!-- .element: class="fragment" data-fragment-index="1" -->
* <p>Set of **plugins for ServiceMix & Karaf**</p> <!-- .element: class="fragment" data-fragment-index="2" -->
* <p>Leverages **Apache Zookeeper**</p> <!-- .element: class="fragment" data-fragment-index="3" -->
* <p>Packaged and integrated into Fuse</p> <!-- .element: class="fragment" data-fragment-index="4" -->
* <p>Designed to make it easy to scale integration solutions</p> <!-- .element: class="fragment" data-fragment-index="5" -->
* <p>Helps move integration solutions from dev -> test -> prod</p> <!-- .element: class="fragment" data-fragment-index="6" -->

--

## What is fabric **really**?

* Profiles (collection of bundles/components)
* Containers (collection of karaf containers)
* Runtime Registry (zookeeper)
* Configuration Repository (git)
* Tooling (mvn, hawt, karaf commands)

--

![Fabric](img/fabric-image.png) <!-- .element: fullscreen-size="contain" -->

--

## Profile

* Feature - Collection of bundles.
* Profile - Wraps a collection of features. Features are normally OOTB + custom.
* Container -> Karaf, but a fabric creates many.
* Registry -> Zookeper. Important to understand 2 generals' problem/quorum-ing. It affects the deployment.
