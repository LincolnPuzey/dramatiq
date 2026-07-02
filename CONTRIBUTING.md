# Contributing

First off, thank you for considering to contribute!
There are several ways to contribute to Dramatiq,
even small things like reporting bugs help us out.

## Features

We consider Dramatiq to be mostly feature-complete, and try to avoid adding new features were possible.

Dramatiq has been designed to be extensible and pluggable by using custom classes.
For example, custom Middleware classes can add new functionality,
and custom Broker and ResultBackend classes can make Dramatiq work with different backend services. 

Rather than adding new features to Dramatiq, see if you can achieve your desired functionality with a custom class.
If you think it might be useful to others, consider publishing it as a package on PyPI.
We would be happy to promote your package in our documentation.

If achieving your functionality is impossible with a custom class, or you _really_ think it belongs
in Dramatiq, then [start a discussion][discussion board] and describe what you are trying to achieve.
We will try to help you out, maybe we need to 

Pull Requests opened for features that haven't been discussed beforehand, are likely to be closed.
Please don't waste your time.


## Other Issues

For other issues, such as bugs, documentation improvements, typos, etc. please open
issues or pull requests as appropriate.

### Opening Bug Reports

When you open a bug report make sure you include the full stack trace and
that you list all pertinent information (operating system, message
broker, Python implementation) as part of the issue description.
Please include a minimal, reproducible test case with every bug
report.

Filling in the GitHub Bug Report template is the best to ensure you have provided all this information.

### Working On Open Issues

Any issues labeled with https://github.com/Bogdanp/dramatiq/labels/bug 
or https://github.com/Bogdanp/dramatiq/labels/needs%20investigation
are good candidates to work on, by reproducing the bug, investigating what is going on,
and either reporting your findings in the issue, or working on a fix.
Sometimes just reproducing a bug in your environment helps us.

## Code

[Start a discussion][discussion board] before attempting to make a contribution. Any
contribution that doesn't fit my design goals for the project will be
rejected so it's always better to start a discussion first!

By submitting contributions, you disavow any rights or claims to any
changes submitted to the Dramatiq project and assign the copyright of
those changes to CLEARTYPE SRL.  If you cannot or do not want to
reassign those rights, you shouldn't submit a PR.  Instead, you should
open an issue and let someone else do that work.

### Local Development

To set up a development environment, it is recommended to:

1. Clone the repository (or your fork of it).
2. Create and active a virtual environment.
3. Install dramatiq in editable mode with all optional extras: `pip install -e ".[all]"`.
4. Install the development dependencies `pip install --group dev`.

### Pull Requests

* Make sure any code changes are covered by tests.
* Run [black], [isort] and [flake8] on any modified files.
* Run [mypy] to check type correctness.
* If this is your first contribution, add yourself to the [CONTRIBUTORS] file.
* If your branch is behind master, [rebase] on top of it.

Run the test suite with `tox`.  The tests require running [RabbitMQ],
[Redis] and [Memcached] servers.

[CONTRIBUTORS]: https://github.com/Bogdanp/dramatiq/blob/master/CONTRIBUTORS.md
[RabbitMQ]: https://www.rabbitmq.com/
[Redis]: https://redis.io
[Memcached]: https://memcached.org/
[isort]: https://github.com/timothycrosley/isort
[black]: https://github.com/psf/black
[flake8]: https://flake8.pycqa.org/en/latest/
[mypy]: https://mypy.readthedocs.io/en/stable/getting_started.html
[rebase]: https://github.com/edx/edx-platform/wiki/How-to-Rebase-a-Pull-Request
[discussion board]: https://groups.io/g/dramatiq-users
