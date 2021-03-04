---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: cd540965b4de64b5fbdc5158faedf00f7a3516b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915154"
---
# Get-AzStorageAccountKey

## 簡介
取得 Azure 儲存空間帳戶的便捷鍵。

## 語法

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
**Get-AzStorageAccountKey** Cmdlet 會取得 Azure 儲存體帳戶的便捷鍵。

## 例子

### 範例 1：取得儲存空間帳戶的便捷鍵
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

此命令會獲得指定 Azure 儲存空間帳戶的金鑰。

### 範例 2：取得儲存空間帳戶的特定便捷鍵
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### 範例 3：列出儲存空間帳戶的便捷鍵，包括 Kerberos 鍵 (啟用 Active Directory 時) 
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

此命令會獲得指定 Azure 儲存空間帳戶的金鑰。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。

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

### -ListKerbKey
列出指定儲存 (啟用 active directory 時) Kerberos 鍵。
針對 Azure Active Directory 網域服務 (Azure AD DS) 或 Active Directory 網域服務 (AD DS) ，每個儲存帳戶都產生 Kerberos 金鑰。 它是用來做為代表儲存帳戶之網域服務所登錄之身分識別的密碼。 Kerberos 金鑰不提供存取權限，無法針對儲存帳戶執行任何控制項或資料面讀取或寫入作業。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定此 Cmdlet 會獲得金鑰的儲存空間帳戶名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定包含儲存空間帳戶的資源組名。

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

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.String

## 輸出

### Microsoft.Azure.management.storage.models.StorageAccountKey

## 筆記

## 相關連結

[New-AzStorageAccountKey](./New-AzStorageAccountKey.md)


