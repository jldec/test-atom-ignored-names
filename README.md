Atom find-and-replace [Issue #621](https://github.com/atom/find-and-replace/issues/621)

This problem seems to occur when there are  ignored directories which are not at the root E.g. a node_modules directory in a subdirectory.

- ignored names config contains `.git, node_modules`
- using Atom v1.3.1 on OS-X 10.11.1

```
git clone https://github.com/jldec/test-atom-ignored-names.git
cd test-atom-ignored-names
cd test
npm install
cd ..
atom .
```

search for `glob` using `Find in project`
- with nothing in the File/directory pattern field, 3 results are returned
- with `test` in the File/directory pattern field, lots of results from `test/node_modules` are returned
