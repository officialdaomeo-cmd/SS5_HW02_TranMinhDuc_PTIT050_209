# Báo cáo Bài 2: Tái cấu trúc lịch sử commit bằng Interactive Rebase

## 1. Giao diện soạn thảo Interactive Rebase

Khi chạy lệnh `git rebase -i HEAD~4`, giao diện cấu hình commit hiển thị như sau:

```text
pick 96794d3 feat: khoi tao module auth
squash 26649d9 fix typo
squash 063687a adds utility functions
drop 8517025 add temp file for debug

# Rebase 3ffc0be..8517025 onto 3ffc0be (4 commands)
#
# Commands:
# p, pick <commit> = use commit
# r, reword <commit> = use commit, but edit the commit message
# e, edit <commit> = use commit, but stop for amending
# s, squash <commit> = use commit, but meld into previous commit
# f, fixup [-C | -c] <commit> = like "squash" but keep only the previous
#                    commit's log message, unless -C is used, in which case
#                    keep only this commit's message; -c is same as -C but
#                    opens the editor
# x, exec <command> = run command (the rest of the line) using shell
# b, break = stop here (continue rebase later with 'git rebase --continue')
# d, drop <commit> = remove commit
# l, label <label> = label current HEAD with a name
# t, reset <label> = reset HEAD to a label
# m, merge [-C <commit> | -c <commit>] <label> [# <oneline>]
```

Sau khi cấu hình, bước tiếp theo là chỉnh sửa thông điệp cho commit gộp:

```text
feat: hoan thien module authentication.

# Please enter the commit message for your changes. Lines starting
# with '#' will be ignored, and an empty message aborts the commit.
```

## 2. Kết quả Log lịch sử commit sạch sẽ

Sau khi hoàn tất quá trình rebase, kết quả chạy lệnh `git log --oneline` như sau:

```text
a6e80b7 feat: hoan thien module authentication.
3ffc0be initial commit
```
