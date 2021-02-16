---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 66AC5120-80B1-46F2-AA51-132BF361602E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzADApplication.md
ms.openlocfilehash: a4d1831114db40295e30b30e0fb12621caff2c89
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398847"
---
# Get-AzADApplication

## 簡介
列出現有的 Azure Active Directory 應用程式。

## 語法

### EmptyParameterSet (預設) 
```
Get-AzADApplication [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### ApplicationObjectIdParameterSet
```
Get-AzADApplication -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Get-AzADApplication -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### SearchStringParameterSet
```
Get-AzADApplication -DisplayNameStartWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzADApplication -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationIdentifierUriParameterSet
```
Get-AzADApplication -IdentifierUri <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## 描述
列出現有的 Azure Active Directory 應用程式。
應用程式查找可以由 ObjectId、ApplicationId、IdentifierUri 或 DisplayName 完成。
如果沒有提供參數，它會在租使用者下抓取所有應用程式。

## 例子

### 範例 1 - 列出所有應用程式

```
PS C:\> Get-AzADApplication
```

列出租使用者下的所有應用程式。

### 範例 2 - 使用分頁功能列出應用程式

```
PS C:\> Get-AzADApplication -First 100
```

列出租使用者下前 100 個應用程式。

### 範例 3 - 根據識別碼 URI 取得應用程式

```
PS C:\> Get-AzADApplication -IdentifierUri http://mySecretApp1
```

將識別碼為 uri 的應用程式當做 http://mySecretApp1 ""。

### 範例 4 - 根據物件識別碼取得應用程式

```
PS C:\> Get-AzADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69
```

使用物件識別碼為 '39e64ec6-569b-4030-8e1c-c3c519a05d69'的應用程式。

## 參數

### -ApplicationId
要抓取的應用程式之應用程式識別碼。

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisplayName
應用程式的顯示名稱。

```yaml
Type: System.String
Parameter Sets: DisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisplayNameStartWith
從顯示名稱開始抓取所有應用程式。

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -第一個
要返回的物件數量上限。

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdentifierUri
要抓取之應用程式的唯一識別碼 Uri。

```yaml
Type: System.String
Parameter Sets: ApplicationIdentifierUriParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeTotalCount
報告資料集中的物件數目。 目前，此參數沒有任何影響。

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

### -ObjectId
要抓取之應用程式的物件識別碼。

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -略過
忽略前 N 個物件，然後獲得其餘的物件。

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。

## 輸入

### System.Guid

### System.String

## 輸出

### Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication

## 筆記

## 相關連結

[Remove-AzADAppCredential](./Remove-AzADAppCredential.md)

[New-AzADAppCredential](./New-AzADAppCredential.md)

[Get-AzADAppCredential](./Get-AzADAppCredential.md)

[Remove-AzADApplication](./Remove-AzADApplication.md)


[New-AzADApplication](./New-AzADApplication.md)

