Simples - The Simple HTTP Server
================================

Build:

    $ ./gradlew shadowJar

If you have `kotlinc` in your `PATH` variable you can also run:

    $ ./build.sh


Run:
    

    $ java -jar lib/simples.jar

    Usage:  java -jar simples.jar [-u] [-s] [-p port] dir [prefix]
    -u       Enable uploads
    -i       Enable index files (index.html, index.htm)
    -s       https: (insecure self-signed certificate)
    -p port  Set port (default 6001)
    dir      Directory to serve
    prefix   Use fixed prefix instead of random number.  "/" for no prefix.

    If no prefix is specified, a random number will be used.  If you're on an open
    network, the prefix makes it unlikely an attacker will be able to do anything.

    You might need to configure your firewall to allow incoming connections.
    For example, on Ubuntu Linux, I use "ufw allow 6001/tcp".
    Remember to deny access when you're done!