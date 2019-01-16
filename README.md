
# git-local-info

## Badges

[![npm package](https://img.shields.io/npm/v/git-local-info.svg?style=flat-square)](https://www.npmjs.org/package/git-local-info) [![Build Status](https://travis-ci.org/ycjcl868/git-local-info.svg?branch=master)](https://travis-ci.org/ycjcl868/git-local-info) [![dependencies Status](https://david-dm.org/ycjcl868/git-local-info/status.svg)](https://david-dm.org/ycjcl868/git-local-info)

--------------------

## gitInfo

Retrieves repo information without relying on the `git` command.

### Usage

```
// install
$ npm install git-local-info -S
```

```javascript
import GitInfo from 'git-local-info';


const gitInfo = new GitInfo();

const result = gitInfo.getGitInfo;

// result is:
{
  /** The current branch */
  branch: string;
  /** The current repository url */
  repository: string;
  /** SHA of the current commit */
  sha: string;
  /** The committer of the current SHA */
  commit: ICommit;
  /** The commit message for the current SHA */
  rootDir: string;
}

```

### Params

new GitInfo(params);

```js
// params
{
  // default process.cwd()
  gitPath: process.cwd(),
  // default .git
  GIT_DIR: '.git',
}
```
