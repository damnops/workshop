# Workshop

这里是一些workshop准备工作的相关东西。

## 用户相关

### 获取上课用户列表

从报名表单中导出报名结果后执行`./auto/get-userlist FILENAME NUMBER`脚本，`NUMBER`为需要选出的人数。

### 配置密码

修改`auto/set-env-vars`中的`PASSWORD_PREFIX`参数，将来生成的用户将以此为前缀生成对应的密码，密码的格式为`PasswordPrefix#NN`，`NN`为用户的序号。比如配置的`PasswordPrefix`参数为`Password@2019`，对应的用户`workshopuser01`的密码将为`Password@2019#01`。

### 生成/修改用户

执行`./auto/setup-users NUMBER`，这将生成`NUMBER`个IAM具有`poweruser`权限的用户，用户名为`workshopuser##`，`##`对应数字，如果有需要请修改脚本`auto/create-template`中的`ManagedPolicyArns`参数。

### 删除用户

执行`./auto/delete-users`

### Tags

配置文件`aws/deployment/users/tags.yml`中可以给stack设置所需的**tag**，遵循key/value格式即可。

## 号码条
上传了一个numbers.pdf的文件，里面有01到20个号码，pull下来，大家可以打印出来给Workshop的各位学员。
