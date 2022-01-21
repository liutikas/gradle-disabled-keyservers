# Gradle signature verification keychain caching issue

## Repro steps

1. `./gradlew jar` <- build succeeds as expected
2. Modify `gradle/verification-metadata.xml` to uncomment `<key-servers enabled="false"/>`
3. `./gradlew jar`

## Expected

Build fails because we are missing keychains that are only available online

## Actual

Builds succeeds
