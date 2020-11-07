---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 975DD42E-61B6-437B-884D-C15A8DB7A667
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/set-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Set-AzTrafficManagerProfile.md
ms.openlocfilehash: d8f4b5e069ef273dedc8e2e5a1f929d1649aefdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93793263"
---
# Set-AzTrafficManagerProfile

## 摘要
更新流量管理器設定檔。

## 句法

```
Set-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzTrafficManagerProfile** Cmdlet 會更新 Azure 流量管理器設定檔。
這個 Cmdlet 會從本機設定檔物件更新設定檔的設定。
您可以使用 *TrafficManagerProfile* 參數或使用管線來指定設定檔物件。

您可以使用 Get-AzTrafficManagerProfile Cmdlet 來取得代表設定檔的局部物件。
在本機修改物件，然後使用 [ **設定] AzTrafficManagerProfile** 來認可您的變更。

## 示例

### 範例1：更新設定檔
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" 
PS C:\> $TrafficManagerProfile.ProfileStatus = Disabled
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

第一個命令會使用 Get-AzTrafficManagerProfile Cmdlet 來取得 Azure 流量管理器設定檔。
該命令會將設定檔儲存在本機 $TrafficManagerProfile 變數中。

第二個命令會在本機變更該設定檔。
這個命令會停用設定檔。

第三個命令會更新名為 ContosoProfile 的流量管理器設定檔，以符合 $TrafficManagerProfile 中的本機值。

## 參數

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。

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

### -TrafficManagerProfile
指定本機 **TrafficManagerProfile** 物件。
這個 Cmdlet 會更新流量管理器，以符合這個本機物件。

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### TrafficManagerProfile 中的 TrafficManager。

## 輸出

### TrafficManagerProfile 中的 TrafficManager。

## 筆記

## 相關連結

[附加 AzTrafficManagerEndpointConfig](./Add-AzTrafficManagerEndpointConfig.md)

[AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[新-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[移除-AzTrafficManagerEndpointConfig](./Remove-AzTrafficManagerEndpointConfig.md)

[移除-AzTrafficManagerProfile](./Remove-AzTrafficManagerProfile.md)


