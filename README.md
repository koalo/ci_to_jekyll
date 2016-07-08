# CI to Jekyll
Publish continous integration results (e.g. from Travis CI) as Jekyll blog (e.g. GitHub Pages)

1. Create an orphan branch, e.g. named gh-pages, where the results will be published to.
2. Setup a way to [push without typing in a password](https://blog.ionelmc.ro/2015/07/11/publishing-to-github-pages-from-travis-ci/).
2. Copy the ci_to_jekyll.py script to the branch in which you will generate the results.
3. Let your continous integration scripts generate the results in a new dedicated directory.
4. Furthermore, let it generate an index file (e.g. index.md) that references and summarizes the result files and put it in the result directory, too.
5. Run the ci_to_jekyll.py script. The only required parameter is the path of the result directory.
6. The script will commit the content of the result directory as well as the index file to the gh-pages branch and pushes it to the remote.
8. Repeat from 3.
