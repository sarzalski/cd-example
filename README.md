### Example of versioning and dependency management

1. Deploy utils (it could be legacy code specific only for this project that changes very rare or etc)
```
cd $PROJECT_PATH/cd-utils
mvn clean deploy
```
2. Deploy snapshots
```
cd $PROJECT_PATH/cd-parent
mvn versions:set -DnewVersion=0.0.7-SNAPSHOT
mvn clean deploy
```
3. Deploy releases
```
cd $PROJECT_PATH/cd-parent
mvn versions:set -DnewVersion=0.0.7-FINAL
mvn clean deploy
```
