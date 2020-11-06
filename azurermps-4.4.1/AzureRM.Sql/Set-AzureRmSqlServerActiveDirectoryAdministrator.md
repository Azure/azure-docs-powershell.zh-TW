---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 60E0D10F-9B93-45A9-A1FF-5C943B8CA09C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerActiveDirectoryAdministrator.md
ms.openlocfilehash: 76d5c2fc90b4e0e518aa022a97c6b9ce369715db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450779"
---
# Set-AzureRmSqlServerActiveDirectoryAdministrator

## 摘要
為 SQL Server 置備 Azure AD 管理員。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Set-AzureRmSqlServerActiveDirectoryAdministrator [-DisplayName] <String> [[-ObjectId] <Guid>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 說明
AzureRmSqlServerActiveDirectoryAdministrator Cmdlet 會在目前的訂閱中，為 AzureSQL Server (Azure AD) 管理員 **設定** Azure Active Directory。

您一次只能提供一個系統管理員。

下列 Azure AD 的成員可設為 SQL Server 系統管理員：

- Azure AD 的原生成員 
- Azure AD 的聯合成員 
- 從其他屬於原生或同盟成員的 Azure 廣告匯入的成員 
- 已建立為安全性群組的 Azure AD 群組

Microsoft 帳戶（例如 Outlook.com、Hotmail.com 或 Live.com 網域中的帳戶）不受系統管理員支援。
其他來賓帳戶（例如 Gmail.com 或 Yahoo.com 網域中的帳戶）不受系統管理員支援。

我們建議您以系統管理員身分提供專用的 Azure AD 群組。

## 示例

### 範例1：為伺服器提供管理員群組
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" 
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

這個命令會為名為 Server01 的伺服器提供一個名為 Dba 的 Azure AD 管理員群組。
此伺服器與資源群組 ResourceGroup01 相關聯。

### 範例2：為伺服器提供管理員使用者
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "David Chew"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
resourcegroup01   server01   David Chew  11E95548-B179-4FE1-9AF4-ACA49D13ABB9
```

這個命令會將 Azure AD 使用者設為名為 Server01 的伺服器的管理員。

### 範例3：透過指定管理員群組的識別碼來提供該群組
```
PS C:\>Set-AzureRmSqlServerActiveDirectoryAdministrator -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DisplayName "DBAs" -ObjectId "40b79501-b343-44ed-9ce7-da4c8cc7353b"
ResourceGroupName ServerName DisplayName ObjectId 
----------------- ---------- ----------- -------- 
ResourceGroup01   Server01   DBAs        40b79501-b343-44ed-9ce7-da4c8cc7353b
```

這個命令會為名為 Server01 的伺服器提供一個名為 Dba 的 Azure AD 管理員群組。
命令會指定 *ObjectId* 參數的 ID。
這可確保即使群組的顯示名稱不是唯一的，命令也會成功。

## 參數

### -DisplayName
指定此 Cmdlet 所配之 Azure AD 管理員的顯示名稱。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
指定此 Cmdlet 所配之 Azure AD 管理員的唯一識別碼。
如果顯示名稱不是唯一的，您必須指定此參數的值。

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
指定指派給伺服器之資源群組的名稱。

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
指定此 Cmdlet 為其提供管理員的 SQL 伺服器名稱。

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
在執行 Cmdlet 之前提示您進行確認。

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
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

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

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### AzureSqlServerActiveDirectoryAdministratorModel 中的 [ServerActiveDirectoryAdministrator]

## 筆記

## 相關連結

[AzureRmSqlServerActiveDirectoryAdministrator](./Get-AzureRmSqlServerActiveDirectoryAdministrator.md)

[移除-AzureRmSqlServerActiveDirectoryAdministrator](./Remove-AzureRmSqlServerActiveDirectoryAdministrator.md)

[SQL 資料庫檔](https://docs.microsoft.com/azure/sql-database/)


