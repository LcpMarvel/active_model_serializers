![Commit Strip
http://www.commitstrip.com/en/2014/05/07/the-truth-behind-open-source-apps/](docs/how-open-source-maintained.jpg)

## Common issues and resolutions

- Using `grape-active_model_serializers`, or any non-Rails server. See
    [issue](https://github.com/rails-api/active_model_serializers/issues/1258).

## How can I help?

### Filing an issue

Everyone is encouraged to open issues that are affecting you:
bugs, ideas, documentation, performance problems – everything helps!

#### Before

1. The first place to start is by looking at our [GitHub Issues](https://github.com/rails-api/active_model_serializers/issues).

  - Check if your issue has already reported.
  - If you find an existing issue report, feel free to add further information to that report.


#### Writing

If possible, please include the following information when [reporting an
issue](https://github.com/rails-api/active_model_serializers/issues/new):

- ActiveModelSerializers version (0.8.x, 0.9.x, 0.10.x, commit ref).
- What are you using ActiveModelSerializers with? Rails? Grape? Other? Which versions?
- If you are not running the latest version (please check), and you cannot update it,
  please specify in your report why you can't update to the latest version.
- Operating system type + version
- Ruby version with patch level.  And if you're using rvm, rbenv, etc.
  - Include your ruby -e "puts RUBY_DESCRIPTION".
- Clearly-written steps to reproduce the issue (i.e. "Show me how to show myself." ), including:
  - What were you doing? Include code if possible.
    - Command line parameters used, if any.
    - RubyGems code in your Gemfile, if any. Gemfile.lock, if possible
    - Any configuration you've made
  - What did you expect to happen?
  - What happened? Include as much information as possible.
    - Nature of reported defect (e.g. user name missing, not "It doesn't work."). Is it intermittent?
    - The best help here is a failing test.
    - Then the steps to reproduce and/or a gist or repository that demonstrates the defect.
    - Then examples of the code you were using.
    - Any error messages (including stacktrace, i.e. ""Show me the error.")
  - Things you've tried.
  - A pull request for your fix would be great.  Code should have tests.
  - Link to source code, if available

Please make sure only to include one issue per report.
If you encounter multiple, unrelated issues, please report them as such.

Simon Tatham has written an excellent on article on
[How to Report Bugs Effectively](http://www.chiark.greenend.org.uk/~sgtatham/bugs.html)
which is well worth reading, although it is not specific to ActiveModelSerializers.



1. What have you tried?

Include as much sample code as you can to help us reproduce the issue. (Inline, repo link, or gist, are fine. A failing test would help the most.)

This is extremely important for narrowing down the cause of your problem.

Thanks!

Sometimes an issue will be closed by a maintainer for various reasons.  In some cases, this is
an invitation to make a better case for your issue or be able to reproduce a bug, and
its being close is just an opportunity to help out some more, and then re-open.

#### After

Thanks to everyone involved!

If you get help, sharing it back in the form of a pull-request or making an issue to document
what you've found is *extremely* helpful.

If you solve your issue, stop working on it, or realize the problem was something else,
please share that in a comment to an issue and close it.  That way, everyone can learn and
we don't have closing issues without a clear resolution. Even if it's just a stackoverflow link :)
And please don't forget to stay involved in the issue until it is closed! Thanks to all!

### Writing code and comments

- We are actively working to identify tasks under the label [**Good for New
  Contributors**](https://github.com/rails-api/active_model_serializers/labels/Good%20for%20New%20Contributors).
  Some bugs are expressly not good for new contributors, so don't expect 100% overlap between the two.
  - [Changelog
      Missing](https://github.com/rails-api/active_model_serializers/issues?q=label%3A%22Changelog+Missing%22+is%3Aclosed) is
    an easy way to help out.

- If you want to work on new feature development, look for the label [**Feature**](https://github.com/rails-api/active_model_serializers/labels/Feature).

- We are also encouraging comments to substantial changes (larger than bugfixes and simple features) under an
  "RFC" (Request for Comments) process before we start active development.
   Look for the [**RFC**](https://github.com/rails-api/active_model_serializers/labels/RFC) label.

## Issue Labeling

ActiveModelSerializers uses a subset of [StandardIssueLabels](https://github.com/wagenet/StandardIssueLabels) for Github Issues. You can [see our labels here](https://github.com/rails-api/active_model_serializers/labels).

## Submitting a pull request (PR)

1. The vast majority of development is happening under the `master` branch, currently slated for release as `0.10.x`.
  This is where we would suggest you start.
1. Fixing bugs is extraordinarily helpful and requires the least familiarity with ActiveModelSerializer.
  Look for issues labeled [**Needs Bug Verification**](https://github.com/rails-api/active_model_serializers/labels/Needs%20Bug%20Verification) and [**Bug**](https://github.com/rails-api/active_model_serializers/labels/bug).
1. Adding or fixing documenation is also fantastic!

To fetch & test the library for development, do:

1. Fork the repository ( https://github.com/rails-api/active_model_serializers/fork )
1. `git clone https://github.com/{whoami}/active_model_serializers.git`
1. `cd active_model_serializers`
1. `bundle`
  - To test against a particular rails version, 4.0 is usually the most buggy, set then
      RAILS_VERSION environment variable as described in the [.travis.yml](.travis.yml).
      e.g. `export RAILS_VERSION=4.0`.
1. Create your PR branch (`git checkout -b my-helpful-pr`)
1. Write tests for your feature, or regression tests highlighting a bug.
  This is important so AcitveModel Serializers doesn't break it in a future version unintentionally.
1. Write the feature itself, or fix your bug
1. `bundle exec rake`
1. Commit your changes (`git commit -am 'Add some feature'`)
  - Use well-described, small (atomic) commits.
1. Push to the branch (`git push origin my-helpful-pr`)
1. Create a new Pull Request
  - Include links to any relevant github issues.
  - *Don't* change the VERSION file.
  - Extra Credit: [Confirm it runs and tests pass on the rubies specified in the travis
    config](.travis.yml). A maintainer will otherwise confirm it runs on these.

1. *Bonus Points** Update [CHANGELOG.md](https://github.com/rails-api/active_model_serializers/blob/master/CHANGELOG.md)
  with a brief description of any breaking changes, fixes, features, or
  miscellaneous changes under the proper version section.
1. Iterate on feedback given by the community (fix syntax, modify bits of code, add
tests), pushing the new commits to the PR each time

Remember to [squash your commits] and rebase off `master`.

#### How maintainers handle pull requests:

- If the tests pass and the pull request looks good, a maintainer will merge it.
- If the pull request needs to be changed,
  - you can change it by updating the branch you generated the pull request from
    - either by adding more commits, or
    - by force pushing to it
  - A maintainer can make any changes themselves and manually merge the code in.

### Commit Messages

- [A Note About Git Commit Messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
 - [http://stopwritingramblingcommitmessages.com/](http://stopwritingramblingcommitmessages.com/)
 - [ThoughtBot style guide](https://github.com/thoughtbot/guides/tree/master/style#git)

### About Pull Requests (PR's)

- [All Your Open Source Code Are Belong To Us](http://www.benjaminfleischer.com/2013/07/30/all-your-open-source-code-are-belong-to-us/)
  - [Using Pull Requests](https://help.github.com/articles/using-pull-requests)
  - [Github pull requests made easy](http://www.element84.com/github-pull-requests-made-easy.html)
  - [Exercism Git Workflow](http://help.exercism.io/git-workflow.html).
  - [Level up your Git](http://rakeroutes.com/blog/deliberate-git/)

### Running tests

#### Running with Rake

The easiest way to run the unit tests is through Rake. The default task runs
the entire test suite for all classes. For more information, checkout the
full array of rake tasks with "rake -T"

Rake can be found at http://docs.seattlerb.org/rake/.

To run a single test suite

   rake test TEST=path/to/test.rb

or

   ruby -I test path/to/test.rb

which can be further narrowed down to one test:

   rake test TEST=path/to/test.rb TESTOPTS="--name=test_something"
