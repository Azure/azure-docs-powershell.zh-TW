---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 2CE84C3A-EFC0-47FA-ACE5-687380D90A7D
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/enable-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Enable-AzTrafficManagerProfile.md
ms.openlocfilehash: ba578d800631304405ab1e0a4139a11d9f2a26dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100138143"
---
# Enable-AzTrafficManagerProfile

## 摘要
啟用流量管理器設定檔。

## 句法

### 區域
```
Enable-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 面向
```
Enable-AzTrafficManagerProfile -TrafficManagerProfile <TrafficManagerProfile>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**Enable-AzTrafficManagerProfile** Cmdlet 可啟用 Azure 流量管理器設定檔。
您可以使用管線或參數值來指定設定檔物件。
或者，您也可以使用 *Name* 和 *ResourceGroupName* 參數來指定設定檔。

## 示例

### 範例1：啟用由名稱指定的設定檔
```
PS C:\>Enable-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
```

這個命令會在 ResourceGroup11 中啟用名為 ContosoProfile 的設定檔。

### 範例2：使用管線啟用設定檔
```
PS C:\>Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" | Enable-AzTrafficManagerProfile
```

這個命令會在 ResourceGroup11 中取得名為 ContosoProfile 的設定檔。
然後，命令會使用管線運算子，將該設定檔傳遞到 **Enable-AzTrafficManagerProfile** Cmdlet。
該 Cmdlet 可啟用該設定檔。

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
若要取得 **TrafficManagerProfile** 物件，請使用 Get-AzTrafficManagerProfile Cmdlet。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### TrafficManagerProfile 中的 TrafficManager。

## 輸出

### System.object

## 筆記

## 相關連結

[Disable-AzTrafficManagerProfile](./Disable-AzTrafficManagerProfile.md)

[AzTrafficManagerProfile](./Get-AzTrafficManagerProfile.md)

[新-AzTrafficManagerProfile](./New-AzTrafficManagerProfile.md)

[移除-AzTrafficManagerProfile](./Remove-AzTrafficManagerProfile.md)

[Set-AzTrafficManagerProfile](./Set-AzTrafficManagerProfile.md)


