---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubJob.md
ms.openlocfilehash: daacefe94d694a6d6288e4c1ccd0f6b05ad1e582
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449342"
---
# Get-AzureRmIotHubJob

## 摘要
取得 IotHub 工作的相關資訊。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Get-AzureRmIotHubJob [-ResourceGroupName] <String> [-Name] <String> [[-JobId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
取得 IotHub 工作的相關資訊。
當您使用 New-AzureRmIotHubExportDevices 或 New-AzureRmIotHubImportDevices 命令 initialted 匯入或匯出作業時，就會建立 IotHub 工作。
您可以依作業識別碼列出所有作業或篩選作業。

## 示例

### 範例1列出所有工作
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub"
```

取得名為 "myiothub" 的 IotHub 的所有工作

### 範例2取得特定工作
```
PS C:\> Get-AzureRmIotHubJob -ResourceGroupName "myresourcegroup" -Name "myiothub" -JobId 3630fc31-4caa-43e8-a232-ea0577221cb2
```

取得名為 "3630fc31-4caa-43e8-a232-ea0577221cb2" 的 IotHub 的工作相關資訊 [myiothub "

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -作業 Id
作業識別碼。 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
IoT 中樞的名稱。 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
資源群組名稱

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### PSIotHubJobResponse （IotHub.）。
\` \[ \[ PSIotHubJobResponse、IotHub = 1.0.0.0、Culture = 中性、PublicKeyToken = null、Culture = 中立、版本 = 1.0.0.0、Culture = 中性、PublicKeyToken = null\]\]

## 筆記

## 相關連結

