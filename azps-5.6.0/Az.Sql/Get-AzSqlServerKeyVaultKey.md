---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 523192b1632bf6ed67dff170b2ac94374c443299
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913709"
---
# Get-AzSqlServerKeyVaultKey

## 簡介
獲得 SQL 伺服器的 Key Vault 鍵。

## 語法

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 描述
此Get-AzSqlServerKeyVaultKey Cmdlet 會獲得 SQL 伺服器上 Key Vault 鍵的資訊。
您可以提供 KeyId 來查看伺服器上的所有金鑰，或查看特定金鑰。

## 例子

### 範例 1：取得所有 Key Vault 鍵
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

此命令會獲得 SQL 伺服器上所有 Key Vault 鍵。
ResourceGroupName ： ContosoResourceGroup ServerName ： ContosoServer ServerKeyName ： contoso_contosokey_01234567890123456789012345678901 Type ： AzureKeyVault Uri ： https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint ： 112233445677899001122334455667788900 CreationDate ： 1/1/2017 12：00：00 AM 資源GroupName ： ContosoResourceGroup ServerName ： ContosoServer ServerKeyName ： contoso_contosokey2_01234567890123456789012345678901 Type ： AzureKeyVault Uri ： https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint ： 0099876654332110098877665543221 CreationDate ： 1/1/2017 12：00：00 AM

### 範例 2：取得特定的金鑰庫金鑰
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

此命令會獲得具有 Id ' '的 Key Vault 鍵，然後將 https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 它儲存在$MyServerKeyVaultKey變數。
您可以檢查資料$MyServerKeyVaultKey以取得金鑰庫的詳細資訊。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyId
Azure 金鑰庫 KeyId。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源組的名稱

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
Azure Sql Server 名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -確認
執行 Cmdlet 之前，提示您確認。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示 Cmdlet 執行時會發生什麼情況。
不會執行 Cmdlet。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel

## 筆記

## 相關連結

[SQL 資料庫檔](https://docs.microsoft.com/azure/sql-database/)
