# Reproduction header not regenerating rules_xcodeproj

```
bazel run //:xcodeproj

bazel build //:lib  # all good

xed Repro.xcodeproj

# run lib target in Xcode

# uncomment first line of gen_header.sh

bazel build //:lib  # now fails

# run lib target in Xcode
# still works, even with static_assert(false); now in the header!
```
