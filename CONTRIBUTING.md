[PouchDB](http://pouchdb.com/) - The Javascript Database that Syncs
==================================================

Welcome, so you are thinking about contributing to PouchDB? awesome, this is a great place to start.

Guide to Contributions
--------------------------------------

  * Almost all Pull Requests for features or bug fixes will need tests
  * Looking for something to work on? look for bugs marked [goodfirstbug](https://github.com/daleharvey/pouchdb/issues?labels=goodfirstbug&page=1&state=open)
  * We follow [Felix's Node.js Style Guide](http://nodeguide.com/style.html)
  * Almost all Pull Requests for features or bug fixes will need tests (seriously, its really important)
  * Before opening a pull request run `$ grunt test` to lint test the changes and run node tests. Preferably run the browser tests as well.
  * Commit messages should follow the following style:

```
(#99) - A brief one line description < 50 chars

Followed by further explanation if needed, this should be wrapped at
around 72 characters. Most commits should reference an existing
issue
```

Dependencies
--------------------------------------

PouchDB needs the following to be able to build and test your build, if you havent installed them then best to do do so now, we will wait.

  * [Node.js](http://nodejs.org/)
  * [CouchDB](http://couchdb.apache.org/)

Building PouchDB
--------------------------------------

All dependancies installed? great, now building PouchDB itself is a breeze:

    $ cd pouchdb
    $ npm install
    $ npm run build

You will now have various distributions of PouchDB in your `dist` folder, congratulations.

Running PouchDB Tests
--------------------------------------

The PouchDB test suite expects an instance of CouchDB running in Admin Party on http://127.0.0.1:5984, you can override this by passing a flag with the CouchDB host (and basic auth credentials if needed)

    $ ./bin/dev-server -remote=http://user:pass@myname.host.com

### Node Tests

Run all tests with:

    $ npm test

### Browser Tests

    $ npm build
    $ npm run dev-server
    # Now visit http://127.0.0.1:8000/tests/test.html in your browser
    # add ?testFiles=test.basics.js to run single test file

Git Essentials
--------------------------------------

Workflows can vary, but here is a very simple workflow for contributing a bug fix:

    $ git clone git@github.com:myfork/pouchdb.git
    $ git remote add pouchdb https://github.com/daleharvey/pouchdb.git

    $ git checkout -b 121-issue-keyword master
    # Write tests + code
    $ git add src/afile.js
    $ git commit -m "(#121) - A brief description of what I changed"
    $ git push origin 121-issue-keyword

Building PouchDB Documentation
--------------------------------------

The source for the website http://pouchdb.com is stored inside the `docs` directory of the PouchDB repository, you can make changes and submit pull requests as with any other patch. To build and view the website locally you will need to install [jekyll](http://jekyllrb.com/) then:

    $ cd docs
    $ jekyll -w serve

You should now find the documentation at http://127.0.0.1:4000

Questions?
----------

If you have any questions, please feel free to ask on the
[PouchDB Mailing List](https://groups.google.com/forum/#!forum/pouchdb) or in #pouchdb on irc.freenode.net.

Committers!
--------------

With great power comes great responsibility yada yada yada:

 * Code is peer reviewed, you should (almost) never push your own code.
 * Please dont accidently force push to master.
 * Cherry Pick / Rebase commits, dont use the big green button.
 * Ensure reviewed code follows the above contribution guidelines, if it doesnt feel free to ammend and make note.
 * Please try to watch when Pull Requests are made and review and / or commit them in a timely manner.
 * Thanks, you are all awesome human beings.
