[![sclang_tests](https://github.com/madskjeldgaard/supercollider-github-action-example/actions/workflows/sclang_tests.yml/badge.svg)](https://github.com/madskjeldgaard/supercollider-github-action-example/actions/workflows/sclang_tests.yml)

# supercollider-github-action-example

A simple example of running SuperCollider tests in a github action on every push to a repo.

It uses [this docker image](https://hub.docker.com/r/capitalg/supercollider) to do it. 

You can define what it needs to run int the file [.github/scripts/run_tests.scd](.github/scripts/run_tests.scd), just make sure it exits with exit code 0 if the tests pass or any other number if it doesn't. 

If you need to install some quarks before then, then you can do that in the file [.github/scripts/install_quarks.scd](.github/scripts/install_quarks.scd). This is run in a seperate sclang process before running the above.
