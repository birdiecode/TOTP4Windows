# TOTP4Windows

TOTP Аутентификация для Windows.

## Установка

1. переместите `TOTP.ps1` в `C:/Windows/System32`
2. создание TOTP секрета. Генерация случайной строки из симвалов `ABCDEFGHIJKLMNOPQRSTUVWXYZ234567` и длинной `20` симвалов
3. найти с переменную `$secretTOTP` и вставить секрет
4. найти с переменную `$userTOTP` и вставить логин пользователья
5. найти с переменную `$passwordNoTOTP` и вставить пароль который будет установливаться при остановки службы
6. Открыть консоль от прав администратора и выполнить команды
```
Set-ExecutionPolicy Unrestricted
./TOTP.ps1 -Setup
./TOTP.ps1 -Start
```

## ресурсы что я использовал

[PowerShell Service](http://jf.larvoire.free.fr/progs/PSService.ps1)
[Convert-Base32ToByte](https://www.powershellgallery.com/packages/SecurityFever/2.4.0/Content/Helpers%5CCommon%5CConvert-Base32ToByte.ps1)
[Get-TimeBasedOneTimePassword](https://www.powershellgallery.com/packages/SecurityFever/2.4.0/Content/Functions%5CCommon%5CGet-TimeBasedOneTimePassword.ps1)
