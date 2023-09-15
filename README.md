# Grumpy Bear 6
Bear's vanilla version

What it is: 
+ GregTech 6 on Java 21, based on Bear's default testing pack
+ performance mods: NotFine + Neodymium + Archaicfix + CoreTweaks
+ no Fastcraft or Optifine
+ updated mods, but no other changes

 
It should import and run with PolyMC/Prism, but you need to point it to your local Java 21 version.

My Java flags work with GraalVM. Due to Java 21 not being officially out at this moment, I'm using dev builds:  
https://github.com/graalvm/graalvm-ce-dev-builds/releases
(direct link for windows) https://github.com/graalvm/graalvm-ce-dev-builds/releases/download/23.1.0-dev-20230905_1517/graalvm-community-java21-windows-amd64-dev.zip

When Java 21 is officially out I'll use the build offered directly by Oracle, as they usually have very slightly better peformance:    
https://www.oracle.com/downloads/graalvm-downloads.html  
 
(remove "-Darchaicfix.debug.noUpdateAcceleration=true" from Java flags for much faster chunk generation) 
 
To use with MultiMC you need some additional steps. You need to add these java flags:  

--illegal-access=warn -Djava.security.manager=allow -Dfile.encoding=UTF-8 --add-opens java.base/jdk.internal.loader=ALL-UNNAMED --add-opens java.base/java.net=ALL-UNNAMED --add-opens java.base/java.nio=ALL-UNNAMED --add-opens java.base/java.io=ALL-UNNAMED --add-opens java.base/java.lang=ALL-UNNAMED --add-opens java.base/java.lang.reflect=ALL-UNNAMED --add-opens java.base/java.text=ALL-UNNAMED --add-opens java.base/java.util=ALL-UNNAMED --add-opens java.base/jdk.internal.reflect=ALL-UNNAMED --add-opens java.base/sun.nio.ch=ALL-UNNAMED --add-opens jdk.naming.dns/com.sun.jndi.dns=ALL-UNNAMED,java.naming --add-opens java.desktop/sun.awt.image=ALL-UNNAMED --add-modules jdk.dynalink --add-opens jdk.dynalink/jdk.dynalink.beans=ALL-UNNAMED --add-modules java.sql.rowset --add-opens java.sql.rowset/javax.sql.rowset.serial=ALL-UNNAMED

more infos here: https://github.com/GTNewHorizons/lwjgl3ify

Bear's GT6 default pack:  
https://bearsden.overminddl1.com/Downloads/Gregtech%206%20packs/Surviving%20GT6%20Season%203(cont.%20from%20Take%202)/
