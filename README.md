# Workshop

这里是一些workshop准备工作的相关东西。

## 用户相关

### 配置密码

修改`aws/cloudformation.yml`中的`PasswordPrefix`参数，将来生成的用户将以此为前缀生成对应的密码，密码的格式为`PasswordPrefix#NN`，`NN`为用户的序号。比如配置的`PasswordPrefix`参数为`Password@2018`，对应的用户`workshop01`的密码将为`Password@2018#01`。

### 生成/修改用户

执行`./auto/setup-users`，这将生成16个IAM具有`poweruser`权限的用户，用户名为`workshop##`，`##`对应数字`01-16`

### 删除用户

执行`./auto/delete-users`

