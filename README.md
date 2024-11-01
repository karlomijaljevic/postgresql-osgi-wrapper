# PostgreSQL JDBC OSGI wrapper

This wrapper project was inspired by [ojdbc8-osgi](https://github.com/chenjiou/ojdbc8-osgi)
from user [chenjiou](https://github.com/chenjiou). I had the need for a OSGI
PostgreSQL JDBC driver when I was migrating my companies DB from Oracle to
PostgreSQL. We used chenjiou's wrapper to create a feature for WLP to use an
external active directory.

Once I started migrating the DB I left that feature for last and noticed there
is no equivalent wrapper for PostgreSQL. Until now :)

The current driver configuration is for version *42.7.4* but to use another one
simply change the version in the pom.xml file. The wrapper expects the driver
to be available during runtime on the classpath.

I have specified the Java compiler release of 21 for the project, but you can
change that to whichever one you prefer. Just don't forget to change then the
Apache Felix *maven-bundle-plugin* plugin version as well to a compatible one.

## Build instructions

To simply create a OSGI *.jar* in the target directory run:

```sh
mvn clean install
```

## Licensing

Any and all rights for PostgreSQL related files are as they are defined in the
PostgreSQL license for their JDBC which you can also find in the bundle once
you bundle it. As it comes to this project/wrapper the rules are the same aka
all this *shizlle* belongs to them I'm just a proxy of sorts :D.
