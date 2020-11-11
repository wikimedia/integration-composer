# integration/composer.git

This repository holds Composer and its dependencies. It is meant to safely
deploy Composer on the Wikimedia cluster since:

1) we can NOT download from third parties
2) there is no Debian package for Composer (until Debian Stretch, which has 1.2.2)

## How to update

Use https://getcomposer.org/ itself!

Bump the version in composer.json then refresh it:

    $ composer update

To review the list of packages currently installed:

    $ composer show --installed

REVIEW THE DIFF!

    $ git diff

If it looks sane, add and commit for review:

    $ git add vendor
    $ git commit -m 'Updating Composer to vX.X.X'
    $ git push refs/for/master

Then ask for review.
