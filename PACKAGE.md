
```
jdeps --class-path '*' --multi-release base -recursive --ignore-missing-deps --print-module-deps umleditor.jar
```

-> `java.base,java.desktop,java.management,java.sql`

```
 jlink --add-modules java.base,java.desktop,java.management,java.sql --output umleditor-jre
```

```
jpackage --icon icon-umleditor-v2-128x128.icns --name umleditor --type dmg --input . --main-jar umleditor.jar -d output --runtime-image umleditor-jre --app-version 3.6.6
```