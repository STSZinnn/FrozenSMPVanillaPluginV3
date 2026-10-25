PUNCH SNOWBALL + INFINITE TNT + FREEZING WIND CHARGE v1.4
Minecraft Paper 1.21.11, Java 21

HOW TO UPDATE GITHUB
1. Your old .github/workflows/build.yml still works; do NOT reupload it.
2. On GitHub replace src/main/java/com/example/punchsnowball/PunchSnowballPlugin.java
3. Replace src/main/resources/plugin.yml and config.yml
4. Update build.gradle.kts version if desired (1.4.0), commit changes.
5. Actions > Build plugin > Run workflow > download artifact ZIP > extract JAR.
6. Stop server, remove old JAR, add new JAR to plugins/, start server.

COMMANDS (OP by default)
/givesnowball [player]
/givetnt [player]
/givewindcharge [player]
/punchreload

CUSTOM WIND CHARGE
Infinite throws, 20-second cooldown (all wind charges of that material share
vanilla cooldown). Hitting a PLAYER directly immobilizes them for 3 seconds,
prevents placing/breaking blocks, item use and consumption, attacks and swings,
and shows powder-snow freezing overlay and ice particles. Hitting terrain does
not freeze nearby players. Other players can still attack the frozen player.

LIMITATION: Bukkit/Paper cannot fully disable the *local* camera or mouse on a
vanilla client. Server-side PlayerMoveEvent corrections enforce direction but
view may visibly twitch briefly. Exact client-level lock needs a client mod.

All gameplay values are in plugins/PunchSnowball/config.yml after first start;
edit there and /punchreload to apply without rebuilding.

NOTE: Project source; this ZIP is not the compiled JAR. Compile using GitHub
Actions. v1.4 has not been tested in a running Paper server.
