# thuthesis-github-actions

清华大学学位论文 LaTeX 模版 [thuthesis](https://github.com/tuna/thuthesis) 建议在最后提交时使用 Windows 编译以获得正确的字体。本项目提供使用 Github Actions 自动编译 thuthesis 的脚本。用户可以将本 repo 中的 `.github/workflows` 文件夹拷贝至自己的论文项目中并上传至 Github。此时，在 repo 的 Actions 菜单中可以看到 Github Actions 会自动编译项目（编译 thuthesis 提供的样例论文大致需要 8 分钟），并生成 `thesis.pdf` 和 `spine.pdf` 两个文件供下载，分别为论文本身和书脊。此后，每当用户将新的 commit push 到 repo 中时，Github 都会自动重新编译论文。

之所以要这样做而不是本地编译，是为了方便非 Windows 环境的用户在编译论文时使用正确的字体。实际上，学校提供了论文的 Word 模版，并在其中规定了字体。thuthesis 只有在 Windows 环境下编译才严格符合学校的规定。本脚本使用了 Github Actions 提供的 Windows 环境以生成字体正确的论文。

**注意：在 `.github/workflows/build.yml` 中，默认的论文主文件名为 `thuthesis-example.tex`（第75行），与 thuthesis 提供的默认文件名相同。然而，thuthesis 文档建议用户在写自己的论文时不要使用这一文件名，而是复制这一文件，并重新命名。这里假定用户没有采纳这一建议。这样，用户应当可以直接用这个脚本生成 thuthesis 的样例论文。如果用户采纳了 thuthesis 的建议，也请自行修改 `.github/workflows/build.yml` 中第75行的文件名，以编译正确的文件。（如果你不知道这里在说什么，大概率可以直接忽略。）**
