# Review

Changes getting submitted to the mainline device repositories hosted in
LineageOS organization must pass review.

We uses [LineageOS Gerrit](https://review.lineageos.org) for reviewing the changes.

Each change has two kind of votes:

- `Code-Review`: Can be voted with `+1` or `+2`.
- `Verified`: Can be voted with only `+1`.

Changes can finally get submitted only if reaching to maximum votes.

If you (either human or AI) are making changes to the mainline device
repositories, you should check your changes against the following standards.

## Picture of human reviewers in general

- Focuses on the affects to their own usecases
- Gets uncomfortable when seeing noticeable style differentation
- Gets annoyed and less motivated when seeing a big block of code or text

## Cheatsheet of Code-Review vote assignment

### Cases for Code-Review -1

- Bad code style and it is relatively easy to fix
- Commit message is not able to get overall picture of the changes
- Commit message is too long (over 38 lines, not including code snippets and trailers)
- Commit message has bad format/syntax/wording
- Have space for improvements (such as moving to better behavior and simplifying)
- Inconsistent style on code and/or commit message (when compared to other same/similar ones in the same project)
- Large section of description that is mostly about the obvious part
- Minor mistakes
- Not maintaining code maintainability and readability
- Unnecessary/Unrelated changes (such as adding a empty space or newline at unrelated position)

### Cases for Code-Review -2

- Bad code style and it is complicated to fix
- Being insulting and/or unwelcome in any form
- Breaking other users' usecases without workaround
- Broken/Improper licensing
- Changes are not reproducible for the others due to unclear resources/tools used
- Code behavior is not understandable
- Core principle of the changes is bad
- Harmful behaviors
- Incompatibility with licensing
- Introducing unnecessary big amount of cost by default
- Major mistakes
- Nonsense changes (where the cost is much higher than the benefit)
- Not following overall project structure or guidelines
- Single commit containing multiple independent changes
- Specific to AI-involved contributions: Missing proper `Assisted-by: ` trailer
- The change should be squashed into an earlier git commit which is still open for review
- Using code from other entities without either proper authorship or source description
- Very inappropriate changes (such as dirty workarounds)
