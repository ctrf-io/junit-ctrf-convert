# Convert JUnit XML to CTRF JSON

> Convert JUnit reports to CTRF reports

This package is useful if there isn't a CTRF reporter available for your test framework.

## Help us grow CTRF

⭐ **If you find this project useful, please consider following the [CTRF organisation](https://github.com/ctrf-io) and giving this repository a star** ⭐

**It means a lot to us and helps us grow this open source library.**

## Usage

```sh
npx junit-to-ctrf path/to/junit.xml
```

## Options

`-o`, `--output` <output>: Output directory and filename for the CTRF report. If not provided, defaults to ctrf/ctrf-report.json.

`-t`, `--tool` <toolName>: Tool name to include in the CTRF report.

`-u`, `--use-suite-name` <useSuiteName>: Use suite name in the test name, defaults to true.

`-e`, `--env` <envProperties>: Environment properties to include in the CTRF report. Accepts multiple properties in the format KEY=value.


## Examples

Convert a JUnit XML report to the default CTRF report location (ctrf/ctrf-report.json):

```sh
npx junit-to-ctrf path/to/junit.xml
```

### Specify Output File

Convert a JUnit XML report to a specified output file:

```sh
npx junit-to-ctrf path/to/junit.xml -o path/to/output/ctrf-report.json
```

### Include Tool Name

Convert a JUnit XML report and include a tool name in the CTRF report:

```sh
npx junit-to-ctrf path/to/junit.xml -t ExampleTool
```

### Include Environment Properties

Convert a JUnit XML report and include environment properties in the CTRF report:

```sh
npx junit-to-ctrf path/to/junit.xml -e appName=MyApp buildName=MyBuild
```

See [CTRF schema](https://www.ctrf.io/docs/schema/environment) for possible environment properties

### Exclude Suite Name

```sh
npx junit-to-ctrf path/to/junit.xml -u false
```

### Full Command

Combine all options in a single command:

```sh
npx junit-to-ctrf path/to/junit.xml -o path/to/output/ctrf-report.json -t ExampleTool -e appName=MyApp buildName=MyBuild
```

## What is CTRF?

CTRF is a universal JSON test report schema that addresses the lack of a standardized format for JSON test reports.

**Consistency Across Tools:** Different testing tools and frameworks often produce reports in varied formats. CTRF ensures a uniform structure, making it easier to understand and compare reports, regardless of the testing tool used.

**Language and Framework Agnostic:** It provides a universal reporting schema that works seamlessly with any programming language and testing framework.

**Facilitates Better Analysis:** With a standardized format, programatically analyzing test outcomes across multiple platforms becomes more straightforward.

## Support Us

If you find this project useful, consider giving it a GitHub star ⭐ It means a lot to us.
