

<svg aria-hidden="true" focusable="false" role="img" class="octicon octicon-mark-github" viewBox="0 0 16 16" width="32" height="32" fill="currentColor" style="display:inline-block;user-select:none;vertical-align:text-;overflow:visible"><path d="M8 0c4.42 0 8 3.58 8 8a8.013 8.013 0 0 1-5.45 7.59c-.4.08-.55-.17-.55-.38 0-.27.01-1.13.01-2.2 0-.75-.25-1.23-.54-1.48 1.78-.2 3.65-.88 3.65-3.95 0-.88-.31-1.59-.82-2.15.08-.2.36-1.02-.08-2.12 0 0-.67-.22-2.2.82-.64-.18-1.32-.27-2-.27-.68 0-1.36.09-2 .27-1.53-1.03-2.2-.82-2.2-.82-.44 1.1-.16 1.92-.08 2.12-.51.56-.82 1.28-.82 2.15 0 3.06 1.86 3.75 3.64 3.95-.23.2-.44.55-.51 1.07-.46.21-1.61.55-2.33-.66-.15-.24-.6-.83-1.23-.82-.67.01-.27.38.01.53.34.19.73.9.82 1.13.16.45.68 1.31 2.69.94 0 .67.01 1.3.01 1.49 0 .21-.15.45-.55.38A7.995 7.995 0 0 1 0 8c0-4.42 3.58-8 8-8Z"></path></svg> <span display="flex" justify-content="center" ><a href = "https://docs.github.com/zh">GitHub 文档</a></span>

# 生成新的 SSH

1. 打开Git Bash。

2. 粘贴以下文本，将示例中使用的电子邮件替换为 GitHub 电子邮件地址。

   ```shell
   ssh-keygen -t ed25519 -C "your_email@example.com"
   ```

   注意：如果你使用的是不支持 Ed25519 算法的旧系统，请使用以下命令：

   ```shell
    ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```

   这将以提供的电子邮件地址为标签创建新 SSH 密钥。

   ```shell
   > Generating public/private ALGORITHM key pair.
   ```

   当系统提示您“Enter a file in which to save the key（输入要保存密钥的文件）”时，可以按 Enter 键接受默认文件位置。 请注意，如果以前创建了 SSH 密钥，则 ssh-keygen 可能会要求重写另一个密钥，在这种情况下，我们建议创建自定义命名的 SSH 密钥。 为此，请键入默认文件位置，并将 id_ALGORITHM 替换为自定义密钥名称。

   ```powershell
   > Enter file in which to save the key (/c/Users/YOU/.ssh/id_ALGORITHM):[Press enter]
   ```

3. 在提示符下，键入安全密码。 有关详细信息，请参阅“[使用 SSH 密钥密码](https://docs.github.com/zh/authentication/connecting-to-github-with-ssh/working-with-ssh-key-passphrases)”。

   ```shell
   > Enter passphrase (empty for no passphrase): [Type a passphrase]
   > Enter same passphrase again: [Type passphrase again]
   ```