# Grumpy Bear 6
Bear's vanilla version

What it is: 
+ GregTech 6 on Java 23, based on Bear's default testing pack
+ performance mods: Angelica test + Archaicfix + CoreTweaks
+ no Fastcraft or Optifine
+ updated mods, but no other major changes (delete SpecialMobs and SpecialAI for full parity...)

It should import and run with PolyMC/Prism, but you need to point it to your local Java 23 version. My included Java flags work with GraalVM. 

I'm using Oracle official release:  
https://www.oracle.com/java/technologies/downloads/#graalvmjava23-windows   
(direct link for windows) https://download.oracle.com/graalvm/23/latest/graalvm-jdk-23_windows-x64_bin.zip  
Even if the link stays the same, the Java version gets updated every few months. Currently it's 23+37.1   
 
To use with MultiMC, instead, you need some additional steps. You need to add these java flags:  

--illegal-access=warn -Djava.security.manager=allow -Dfile.encoding=UTF-8 --add-opens java.base/jdk.internal.loader=ALL-UNNAMED --add-opens java.base/java.net=ALL-UNNAMED --add-opens java.base/java.nio=ALL-UNNAMED --add-opens java.base/java.io=ALL-UNNAMED --add-opens java.base/java.lang=ALL-UNNAMED --add-opens java.base/java.lang.reflect=ALL-UNNAMED --add-opens java.base/java.text=ALL-UNNAMED --add-opens java.base/java.util=ALL-UNNAMED --add-opens java.base/jdk.internal.reflect=ALL-UNNAMED --add-opens java.base/sun.nio.ch=ALL-UNNAMED --add-opens jdk.naming.dns/com.sun.jndi.dns=ALL-UNNAMED,java.naming --add-opens java.desktop/sun.awt.image=ALL-UNNAMED --add-modules jdk.dynalink --add-opens jdk.dynalink/jdk.dynalink.beans=ALL-UNNAMED --add-modules java.sql.rowset --add-opens java.sql.rowset/javax.sql.rowset.serial=ALL-UNNAMED

more detailed infos here: https://github.com/GTNewHorizons/lwjgl3ify

Bear's GT6 default pack:  
https://bearsden.overminddl1.com/Downloads/Gregtech%206%20packs/Surviving%20GT6%20Season%203(cont.%20from%20Take%202)/
