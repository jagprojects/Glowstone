mc^2
==========

Introduction
------------

mc^2 is an offspring of the open-source implementation of the
[Minecraft](http://minecraft.net) server software written in Java, called [Glowstone](https://github.com/SpaceManiac/Glowstone) which was originally
forked from Graham Edgecombe's now-defunct
[Lightstone](https://github.com/grahamedgecombe/lightstone) project.

The official server software has some shortcomings such as the use of threaded, synchronous I/O along with high CPU and RAM usage. mc^2 aims to be a
lightweight and high-performance alternative.

mc^2's main aim as a project independent from Lightstone is to offer a
higher-performance server while maintaining compatability with the multitude of plugins available for the popular [Bukkit](http://bukkit.org) server plugin development interface. It does this through implementing Bukkit classes and loading Bukkit plugins which interface with these classes.

Building
--------

mc^2 can be built with the
[Java Development Kit](http://oracle.com/technetwork/java/javase/downloads) and
[Apache Maven](http://maven.apache.org). Maven is also used for dependency
management.

You may download and compile [Bukkit](https://github.com/Bukkit/Bukkit)
yourself if you desire and install it using `mvn install`, but it and other
dependencies will be automatically downloaded by Maven if they are not found.

The command `mvn package` will build mc^2, and `mvn install` will copy it
to your local Maven repository. Official builds of mc^2 may be found on
[Jenkins](http://ci.onarandombox.com/job/mc^2).

Running
-------

Running mc^2 is simple because all dependencies, including Bukkit, are
shaded into the output jar at compile time thanks to a nifty Maven plugin.
Simply execute `java -jar mc^2_10-28-11.jar` along with whatever
memory-related options to Java you desire, and the server should start.

By default, configuration is stored in the `config/` subdirectory and logs
are stored in the `logs/` subdirectory. The main configuration file is
`config/mc^2.yml`, which replaces CraftBukkit's `server.properties` and
`bukkit.yml`. Settings from these two files will be copied over to mc^2's
configuration during the default configuration generation process.

mc^2 uses a [JLine](http://jline.sf.net)-based server console for command
input. On non-Windows systems, console output can also be colored. 

Documentation
-------------

Javadocs can be generated by using the `mvn javadoc:javadoc` command in the
terminal. This utilizes Maven's javadoc plugin and may need to download
dependencies the first time it is run.

For documentation on the Bukkit API, see the
[Bukkit Javadocs](http://jd.bukkit.org/).

Credits
-------

 * SpaceManiac - author of [Glowstone](https://github.com/SpaceManiac/Glowstone)
 * [The Minecraft Coalition](http://wiki.vg/wiki) - protocol and file formats
   research.
 * [Trustin Lee](http://gleamynode.net) - author of the
   [Netty](http://jboss.org/netty) library.
 * Graham Edgecombe - author of the original
   [Lightstone](https://github.com/grahamedgecombe/lightstone) - and everyone
   else who has contributed to Lightstone.
 * All the people behind [Maven](http://maven.apache.org) and
   [Java](http://java.oracle.com).
 * [Notch](http://mojang.com/notch) and all the other people at
   [Mojang](http://mojang.com) - for making such an awesome game in the first
   place!

Copyright
---------

mc^2 is open-source software released under the MIT license. Please see
the `LICENSE` file for details.

