---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 4DC26C26-6162-4A15-BFCB-4D2B6B52DD81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmADServicePrincipal.md
ms.openlocfilehash: 983d5049d0ac58671b3d0766b6b4bcf3f05d4d76
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448939"
---
# Get-AzureRmADServicePrincipal

## 摘要
篩選 active directory 服務主體。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### EmptyParameterSet (預設) 
```
Get-AzureRmADServicePrincipal [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>]
 [-First <UInt64>] [<CommonParameters>]
```

### SearchStringParameterSet
```
Get-AzureRmADServicePrincipal -DisplayNameBeginsWith <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### DisplayNameParameterSet
```
Get-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ObjectIdParameterSet
```
Get-AzureRmADServicePrincipal -ObjectId <Guid> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationIdParameterSet
```
Get-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### ApplicationObjectParameterSet
```
Get-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### SPNParameterSet
```
Get-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>]
 [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## 說明
篩選 active directory 服務主體。

## 示例

### 範例 1-清單廣告服務原則

```
PS C:\> Get-AzureRmADServicePrincipal
```

列出租使用者中的所有廣告服務主體。

### 範例 2-使用分頁來列出廣告服務主體

```
PS C:\> Get-AzureRmADServicePrincipal -First 100
```

列出租使用者中的第一個 100 AD 服務主體。

### 範例3：依 SPN 列出服務主體

```
PS C:\> Get-AzureRmADServicePrincipal -ServicePrincipalName 36f81fc3-b00f-48cd-8218-3879f51ff39f
```

列出 SPN 為「36f81fc3-b00f-48cd-8218-3879f51ff39f」的服務主體。

### 範例4：依搜尋字串列出服務主體

```
PS C:\> Get-AzureRmADServicePrincipal -SearchString "Web"
```

列出顯示名稱以 "Web" 開頭的所有廣告服務主體。

### 範例5：依管道列出服務主體

```
PS C:\> Get-AzureRmADApplication -ObjectId 39e64ec6-569b-4030-8e1c-c3c519a05d69 | Get-AzureRmADServicePrincipal
```

取得物件 id 為 "39e64ec6-569b-4030-8e1c-c3c519a05d69" 的 AD 應用程式，並將其管道至 Get-AzureRmADServicePrincipal Cmdlet，以列出該應用程式的所有服務主體。

## 參數

### -ApplicationId
服務主體應用程式識別碼。

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

### -ApplicationObject
要檢索其服務主體的應用程式物件。

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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

### -DisplayName
服務主體顯示名稱。

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

### -DisplayNameBeginsWith
服務主體搜尋字串。

```yaml
Type: System.String
Parameter Sets: SearchStringParameterSet
Aliases: SearchString

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -優先
要傳回的物件數目上限。

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

### -IncludeTotalCount
報告資料集中的物件數目。 這個參數目前不會執行任何動作。

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
服務主體的物件識別碼。

```yaml
Type: System.Guid
Parameter Sets: ObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
服務的 SPN。

```yaml
Type: System.String
Parameter Sets: SPNParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -略過
忽略前 N 個物件，然後取得剩餘的物件。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

### Guid.empty

### Microsoft.Azure.Graph.RBAC.Version1_6 PSADApplication
參數： ApplicationObject (ByValue) 

## 輸出

### Microsoft.Azure.Graph.RBAC.Version1_6 PSADServicePrincipal

## 筆記

## 相關連結

[新-AzureRmADServicePrincipal](./New-AzureRmADServicePrincipal.md)

[Set-AzureRmADServicePrincipal](./Set-AzureRmADServicePrincipal.md)

[移除-AzureRmADServicePrincipal](./Remove-AzureRmADServicePrincipal.md)

[AzureRmADApplication](./Get-AzureRmADApplication.md)

[AzureRmADSpCredential](./Get-AzureRmADSpCredential.md)

