## 前段

このリポジトリをcloneするため、gitをインストール

1. **gitのインストール**  
    以下のコマンドを実行して、gitをインストールします。

    ```bash
    sudo apt update
    sudo apt install -y git
    ```

2. **インストール確認**  
    以下のコマンドでgitが正しくインストールされたか確認します。

    ```bash
    git --version
    ```

    上記コマンドを実行すると、インストールされたgitのバージョンが表示されます。

3. **SSHを使用したリポジトリのクローン**  
    SSHを使用してリポジトリをクローンする場合、以下のコマンドを実行します。

    ```bash
    git clone git@github.com:haneimo/childpc-setup.git
    ```

## Ansible Clientのインストール方法

1. **必要なパッケージのインストール**  
    以下のコマンドを実行して、Ansibleをインストールするための依存パッケージをインストールします。

    ```bash
    sudo apt update
    sudo apt install -y software-properties-common
    ```

2. **Ansibleリポジトリの追加**  
    Ansible公式リポジトリを追加します。

    ```bash
    sudo add-apt-repository --yes --update ppa:ansible/ansible
    ```

3. **Ansibleのインストール**  
    Ansibleをインストールします。

    ```bash
    sudo apt install -y ansible
    ```

4. **インストール確認**  
    以下のコマンドでインストールが成功したか確認します。

    ```bash
    ansible --version
    ```

以上でAnsible Clientのインストールは完了です。



## ローカルのLubuntuにリポジトリをクローンしてsetup.ymlを適用する手順

1. **リポジトリのクローン**  
    以下のコマンドを実行して、このリポジトリをローカルのLubuntu環境にクローンします。

    ```bash
    git clone https://github.com/your-username/childpc-setup.git
    cd childpc-setup
    ```

2. **setup.ymlの実行**  
    ローカル環境で実行する場合、インベントリファイルを省略して以下のコマンドを実行できます。

    ```bash
    ansible-playbook -i localhost, -c local setup.yml --ask-become-pass
    ```

4. **適用結果の確認**  
    コマンドの出力を確認し、エラーがないことを確認してください。

以上でローカルのLubuntuにリポジトリをクローンし、setup.ymlを適用する手順は完了です。
