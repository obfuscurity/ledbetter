# Ledbetter

Ledbetter is a simple script for gathering Nagios alert statistics and submitting them to Graphite. It writes all statistics to the `nagios.problems` metrics namespace within Graphite.

## Installation

Clone the GitHub repository and use Bundler to install the gem dependencies.

```
$ git clone https://github.com/github/ledbetter.git
$ bundle install
```

## Usage

Ledbetter requires a number of environment variables for runtime configuration. The following example demonstrates how to run it manually from the command line, but you would typically run it as a cron job.

```
$ export NAGIOS_URL=http://nagios.foo.com/cgi-bin/nagios3
$ export NAGIOS_USER=foo
$ export NAGIOS_PASS=bar
$ export CARBON_URL=carbon://localhost:2003
$ bundle exec ruby ledbetter.rb
```

Optionally you can set `VERBOSE=1` to also print statistics to `stdout`.

## License 

Ledbetter is distributed under the MIT license.

