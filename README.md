# Workshop

这里是一些workshop准备工作的相关东西。

## 用户相关

### 配置密码

修改`aws/deployment/users/cloudformation.yml`中的`PasswordPrefix`参数，将来生成的用户将以此为前缀生成对应的密码，密码的格式为`PasswordPrefix#NN`，`NN`为用户的序号。比如配置的`PasswordPrefix`参数为`Password@2018`，对应的用户`workshop01`的密码将为`Password@2018#01`。

### 生成/修改用户

执行`./auto/setup-users`，这将生成16个IAM具有`poweruser`权限的用户，用户名为`workshop##`，`##`对应数字`01-16`

### 删除用户

执行`./auto/delete-users`

### Tags

配置文件`aws/deployment/users/tags.yml`中可以给stack设置所需的**tag**，遵循key/value格式即可。

## SSH

如需要给EC2机器配置登录使用的SSH key，请在Console或者其他相关配置中使用`workshop`，对应的私钥为`aws/keys/workshop.pem`

## 号码条
上传了一个NumbersForPrinting.docx的文件，里面有01到20个号码，pull下来，大家可以打印出来给Workshop的各位学员。
