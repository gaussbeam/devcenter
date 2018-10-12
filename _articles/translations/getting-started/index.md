Bitriseはパワフルで多くの機能がありますが、使い方は簡単で直感的です！最初のビルドはサインアップから数分以内に行えます。さぁ、はじめよう！

## Bitriseにサインアップする

まずはじめにBiriseのアカウントが必要です。以下のいずれかの方法でサインアップしてください。

* [Email](/getting-started/signing-up/signing-up-with-email)
* [GitHub](/getting-started/signing-up/signing-up-with-github)
* [GitLab](/getting-started/signing-up/signing-up-with-gitlab)
* [Bitbucket](/getting-started/signing-up/signing-up-with-bitbucket)

いずれかのGitサービスプロバイダでサインアップする場合、BitriseアカウントとそのGitサービスが連携されます。連携されたアカウントを使用することで、Bitriseからリポジトリへのアクセス許可は簡単に行なうことができます。

サインアップが完了したら、サポートされた３つのGitサービスとBitriseアカウントを連携させることができます。例えば、GitHubアカウントでサインアップしたあとで、GitLab/Bitbucketのアカウントにも連携すると、BitriseはいずれのGitサービス上のリポジトリにもアクセスできるようになります。

## アプリを追加する

トップメニューバーの`+`をクリックしてドロップダウンメニューから`Add app`を選択するだけで、いつでも[アプリを追加する](/getting-started/adding-a-new-app/index)ことができます。

![アプリを追加する](/img/adding-a-new-app/add_new_app.png)

### プライバシー

アプリのプライバシー設定は**非公開**・**[公開](/getting-started/adding-a-new-app/public-apps)**のいずれかから選べます。

* 非公開設定のアプリは、あなたと組織のメンバーおよびチームのメンバーのみアクセスできます。
* 公開設定のアプリは、そのビルドのログと`bitrise.yml`を誰でも参照できます。

![アプリのプライバシー設定](/img/adding-a-new-app/app-privacy.png)

### リポジトリに接続する

以下のいずれかの方法で、ソースコードの場所を指定してください。

* [連携済みのGitHub/GitLab/Bitbucketアカウントのリポジトリに接続する](/getting-started/adding-a-new-app/connecting-a-repository). BitriseはGitサービス内の接続可能なリポジトリを自動で表示するため、選択するだけで接続できます。.
* 手動でソースコードの場所を指定する: `Other/Manual`オプションを選択し、**HTTPS git clone URL**をペーストしてください。
* [セルフホストされたGitLabインスタンス](getting-started/signing-up/self-hosted-gitlab)内のリポジトリも利用できます。

**なぜBitriseがGithub/Bitbucket/GitLabへの書き込み許可を必要とするのか？** GitHub/GitLab/Bitbucketアカウントとの連携の際には、Bitriseが以下の２つを行えるよう、書き込み許可が必要です。

* 選択されたリポジトリにSSHキーを追加する
* リポジトリにWebhookを登録する

### リポジトリへのアクセスを設定する

[選択されたリポジトリにアクセスするために、SSHキーを設定](/getting-started/adding-a-new-app/setting-up-ssh-keys)します。これは、非公開設定のアプリがリポジトリをクローンするために必要です。以下のいずれかの方法で設定できます。

* Bitriseが生成したSSHキーを自動で追加する
* Bitriseが生成した公開鍵をコピーする
* 自分で作成したSSHキーペア(秘密鍵はパスフレーズなしのRSAキーに設定)を使用する

![SSHキーの追加](/img/adding-a-new-app/bitrise_auto_add_ssh_key2.png)

公開設定のアプリはSSHキーを設定できません。

### プロジェクトを設定する

リポジトリへのアクセス設定が完了したら、使用したいリポジトリのブランチを入力し、 `Next`をクリックしてください。

![ブランチの選択](/img/adding-a-new-app/choose-branch.png)

Bitriseはリポジトリの検証と[プロジェクトの設定](/getting-started/adding-a-new-app/setting-up-configuration)を行います。検証に失敗した場合、手動でセットアップを行うことができます。

### Webhookを設定する

[Webhookの登録](/webhooks/index/)を行うと、リポジトリへプッシュされるたびにBitriseのビルドを開始することができます。Webhookの設定をスキップして、あとで設定することもできます。

## ビルドとワークフロー

アプリを追加すると、最初のビルドは自動で実行されます。これは、一連のステップであるワークフローを実行することを意味しています。ステップは所定の入出力変数により実行されるスクリプトのブロックを表すものであり、これこそがBitriseの中心にあるものです。新しいワークフローを作成したり、ワークフローをつなげることも可能です。また、ステップの入力を設定したり、ワークフローにステップを追加・削除することもできます。

* [The build process](/getting-started/builds-and-workflows)
* [Workflows](/getting-started/getting-started-workflows)
* [Steps](/getting-started/getting-started-steps)

## チームと組織

新しいアプリをセットアップしたら、[チームメンバーを招待](/team-management/index)することができます。Developer または Organization プランの場合、チームメンバーを無制限に招待できます！

Organization プランのメンバーであれば、[組織を作成](/team-management/organizations/creating-org)することもできます。 組織はチームを素早く、効率的に管理することができます。
