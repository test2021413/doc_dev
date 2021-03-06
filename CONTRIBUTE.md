# CONTRIBUTE

[中文版本](CONTRIBUTE_CH.md)

## Guidance
Thank you for your interest in contributing to EduNLP! 
Before you begin writing code, it is important that you share your intention to contribute with the team, 
based on the type of contribution:

1. You want to propose a new feature and implement it.
    * Post about your intended feature in an issue, 
    and we shall discuss the design and implementation. 
    Once we agree that the plan looks good, go ahead and implement it.
2. You want to implement a feature or bug-fix for an outstanding issue.
    * Search for your issue in the [EduNLP issue list](https://github.com/bigdata-ustc/EduNLP/issues).
    * Pick an issue and comment that you'd like to work on the feature or bug-fix.
    * If you need more context on a particular issue, please ask and we shall provide.

Once you implement and test your feature or bug-fix, 
please submit a Pull Request to [EduNLP](https://github.com/bigdata-ustc/EduNLP):

1. Fork this repository to your branch.
2. Modify the code. Note that we strongly recommend that you comply with our [commit format specifications](CONTRIBUTE.md#About-Commit).
3. Pass code tests and make the test coverage reach 100%. [An example](tests/test_sif).
4. Submit a Pull Request to [EduNLP](https://github.com/bigdata-ustc/EduNLP). Note that we provide a standard template of Pull Request [here](https://github.com/bigdata-ustc/EduNLP/pull/1). Please fill in the information carefully.

The followings are some helpful guidelines for different types contribution:
 
### Add new dataset

If you want to add the data analysis or a new dataset, please submit a Pull Request to [EduData](https://github.com/bigdata-ustc/EduData).

#### Docs Format

Numpy docs format is used:

```
function

    Parameters
    ----------
    Variable 1: type <int, float>, optional or not
       description
    Variable 2: type <int, float>, optional or not
       description
    ...

    Returns
    -------
    Variable: type <int, float>
       description

    See Also (Optional)
    --------
    Similar to function():

    Examples (Optional)
    --------
    >>> For example:
        ...
```

### About Commit

#### commit format

```
[<type>](<scope>) <subject>
```

#### type
- `feat`：New feature。
- `fix/to`：Fix bugs, either found in Q&A or found in your own use.
   - `fix`：Generating diff and fixes the problem automatically. **Suitable for one submit to fix the problem directly**.
   - `to`：Generating only **diff** but does not automatically fix the problem. **Suitable for multiple submissions**. Use `fix` when the final fix problem is committed.
- `docs`：Documentation.
- `style`：Format (do not affect code execution).
- `refactor`：Refactoring (not new features or bug fix).
- `perf`：Optimize related issues, such as code performance, user experience.
- `test`：Add test unit.
- `chore`：Build process or auxiliary tools change.
- `revert`：Roll back to the previous version.
- `merge`：Code merge.
- `sync`：Synchronizing the bug of main or branch。
- `arch`: Engineering documents or tools change.

##### scope (optional)

Scope is used to describe the impact of the commit, such as **the data layer**, **the control layer**, **the view layer**, and so on, depending on the project.

For example, in Angular, it can be location, browser, compile, compile, rootScope, ngHref, ngClick, ngView, and so on. If your changes affect more than one scope, you can use `*` instead.

##### subject (mandatory)

A subject is a short description of the purpose of the commit, not more than 50 characters.

There is no period or other punctuation at the end.

#### Example

- **[docs] update the README.md**

```sh
git commit -m "[docs] update the README.md"
```

## FAQ

Q: I have carefully tested the code in my local system (all testing passed) but still failed in online CI?
 
A: There are two possible reasons: 
1. the online CI system is different from your local system;
2. there are some network error causing the downloading test failed, which you can find in the CI log.

For the second reason, all you need to do is to retry the test. 

