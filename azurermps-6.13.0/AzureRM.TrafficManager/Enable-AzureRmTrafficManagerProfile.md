---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/enable-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Enable-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: f7ac75789e4020d3d0e645e5dac8ef2430795eb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450142"
---
# Enable-AzureRmTrafficManagerProfile

## 摘要
啟用流量管理器設定檔。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 區域
```
Enable-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 面向
```
Enable-AzureRmTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**Enable-AzureRmTrafficManagerProfile** Cmdlet 可啟用 Azure 流量管理器設定檔。
您可以使用管線或參數值來指定設定檔物件。
或者，您也可以使用 *Name* 和 *ResourceGroupName* 參數來指定設定檔。

## 示例

### 範例1：啟用由名稱指定的設定檔
```
PS C:\>Enable-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

這個命令會在 ResourceGroup11 中啟用名為 ContosoProfile 的設定檔。

### 範例2：使用管線啟用設定檔
```
PS C:\>Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzureRmTrafficManagerProfile
```

這個命令會在 ResourceGroup11 中取得名為 ContosoProfile 的設定檔。
然後，命令會使用管線運算子，將該設定檔傳遞到 **Enable-AzureRmTrafficManagerProfile** Cmdlet。
該 Cmdlet 可啟用該設定檔。

## 參數

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

### -名稱
指定此 Cmdlet 啟用的流量管理器設定檔名稱。

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定資源群組的名稱。
這個 Cmdlet 可在此參數指定的群組中啟用流量管理器設定檔。

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerProfile
指定要啟用的 **TrafficManagerProfile** 物件。
若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzureRmTrafficManagerProfile Cmdlet。

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: Object
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

### TrafficManagerProfile （）
這個 Cmdlet 接受 **TrafficManagerProfile** 物件。

## 輸出

### System.object

## 筆記

## 相關連結

[Disable-AzureRmTrafficManagerProfile](./Disable-AzureRmTrafficManagerProfile.md)

[AzureRmTrafficManagerProfile](./Get-AzureRmTrafficManagerProfile.md)

[新-AzureRmTrafficManagerProfile](./New-AzureRmTrafficManagerProfile.md)

[移除-AzureRmTrafficManagerProfile](./Remove-AzureRmTrafficManagerProfile.md)

[Set-AzureRmTrafficManagerProfile](./Set-AzureRmTrafficManagerProfile.md)


