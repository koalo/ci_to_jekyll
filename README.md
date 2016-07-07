# CI to Jekyll
Publish continous integration results (e.g. from Travis CI) as Jekyll blog (e.g. GitHub Pages)

1. Create an orphan branch, e.g. named gh-pages, where the results will be published to.
2. Copy the ci_to_jekyll.py script to the branch in which you will generate the results.
3. Let your continous integration scripts generate the results in a new dedicated directory.
4. Furthermore, let it generate an index file (e.g. index.md) that references and summarizes the result files and put it in the result directory, too.
5. Run the ci_to_jekyll.py script. The only required parameter is the path of the result directory.
6. The script will commit the content of the result directory as well as the index file to the gh-pages branch.
7. Push the jekyll branch (might be implemented by the script itself in the future).
8. Repeat from 3.
