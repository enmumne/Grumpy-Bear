# Grumpy Bear 6
Bear's vanilla version

What it is: 
+ GregTech 6 on Java 25, based on Bear's default testing pack
+ performance mods: Angelica test + Archaicfix + CoreTweaks
+ no Fastcraft or Optifine
+ updated mods, but no other major changes (delete SpecialMobs and SpecialAI for full parity...)

It should import and run with PolyMC/Prism, but before you can launch it you need to edit the path to your own unzipped local Java 25. My included Java flags work ONLY with GraalVM. 

While Oracle recently discontinued GraalVM, it's still the best performing version at this moment:  
https://www.graalvm.org/downloads/  
(direct link for windows) https://download.oracle.com/graalvm/25/latest/graalvm-jdk-25_windows-x64_bin.zip   
Even if the link stays the same, the Java version contained gets updated every few months. Currently it's 25+37.1   

I use the following custom flags, ZGC seems to only work better on newer Minecraft when using higher amounts of memory, for 1.7.10 I stick to these for the best performance: 
 
-XX:+UnlockExperimentalVMOptions -XX:+EnableJVMCI -XX:+EagerJVMCI -XX:+UseCompactObjectHeaders -Dfml.readTimeout=120 -Dgraal.ShowConfiguration=info -XX:+UseG1GC -Dsun.rmi.dgc.server.gcInterval=900000 -XX:+DisableExplicitGC -XX:G1NewSizePercent=20 -XX:G1ReservePercent=20 -XX:MaxGCPauseMillis=51 -XX:G1HeapRegionSize=32M  
 
To use with MultiMC, instead, you need some additional steps. You need to add these java flags (these may be OUTDATED, it's really better to simply use Prism, or read more carefully instructions from the link just below):  

-Dfile.encoding=UTF-8 -Djava.system.class.loader=com.gtnewhorizons.retrofuturabootstrap.RfbSystemClassLoader --add-opens java.base/java.io=ALL-UNNAMED --add-opens java.base/java.lang.invoke=ALL-UNNAMED --add-opens java.base/java.lang.ref=ALL-UNNAMED --add-opens java.base/java.lang.reflect=ALL-UNNAMED --add-opens java.base/java.lang=ALL-UNNAMED --add-opens java.base/java.net.spi=ALL-UNNAMED --add-opens java.base/java.net=ALL-UNNAMED --add-opens java.base/java.nio.channels=ALL-UNNAMED --add-opens java.base/java.nio.charset=ALL-UNNAMED --add-opens java.base/java.nio.file=ALL-UNNAMED --add-opens java.base/java.nio=ALL-UNNAMED --add-opens java.base/java.text=ALL-UNNAMED --add-opens java.base/java.time.chrono=ALL-UNNAMED --add-opens java.base/java.time.format=ALL-UNNAMED --add-opens java.base/java.time.temporal=ALL-UNNAMED --add-opens java.base/java.time.zone=ALL-UNNAMED --add-opens java.base/java.time=ALL-UNNAMED --add-opens java.base/java.util.concurrent.atomics=ALL-UNNAMED --add-opens java.base/java.util.concurrent.locks=ALL-UNNAMED --add-opens java.base/java.util.jar=ALL-UNNAMED --add-opens java.base/java.util.zip=ALL-UNNAMED --add-opens java.base/java.util=ALL-UNNAMED --add-opens java.base/jdk.internal.loader=ALL-UNNAMED --add-opens java.base/jdk.internal.misc=ALL-UNNAMED --add-opens java.base/jdk.internal.ref=ALL-UNNAMED --add-opens java.base/jdk.internal.reflect=ALL-UNNAMED --add-opens java.base/sun.nio.ch=ALL-UNNAMED --add-opens java.desktop/com.sun.imageio.plugins.png=ALL-UNNAMED --add-opens java.desktop/sun.awt.image=ALL-UNNAMED --add-opens java.desktop/sun.awt=ALL-UNNAMED --add-opens java.sql.rowset/javax.sql.rowset.serial=ALL-UNNAMED --add-opens jdk.dynalink/jdk.dynalink.beans=ALL-UNNAMED --add-opens jdk.naming.dns/com.sun.jndi.dns=ALL-UNNAMED,java.naming

more detailed infos here: https://github.com/GTNewHorizons/lwjgl3ify

Bear's GT6 default pack:  
https://bearsden.overminddl1.com/Downloads/Gregtech%206%20packs/Surviving%20GT6%20Season%203(cont.%20from%20Take%202)/
