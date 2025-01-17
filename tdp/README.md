# TDP Kafka Notes

The version `2.8.2-TDP-0.1.0-SNAPSHOT` of Apache Livy is based on the branch [`2.8`](https://github.com/TOSIT-IO/kafka/tree/2.8).

## Making a release

```bash
cd kafka
./gradlew clean releaseTarGz
```

The command generates a `.tar.gz` file of the release at `./core/build/distributions/kafka_2.13-2.8.2-TDP-0.1.0-SNAPSHOT.tgz`.

## Testing

```bash
./gradlew cleanTest test
```

### Testing a single class

```bash
./gradlew core:test --tests ConnectionQuotasTest
```

### Test reports

HTML reports are generated at `build/reports/tests/test/index.html` in each package. To fetch all the test reports and copy them to `tdp/test-reports/`, run:

```bash
cd tdp
./bin/fetch-test-reports.sh
```

## Test notes

See [test-notes](./test-notes.md)
