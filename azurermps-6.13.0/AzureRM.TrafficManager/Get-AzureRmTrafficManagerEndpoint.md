---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 4556C345-55D0-431C-B980-219D5ED14E5F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/get-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Get-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 335cb4308a64811fdc99b0bafe6660ee69c9b9d3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449685"
---
# Get-AzureRmTrafficManagerEndpoint

## 摘要
取得流量管理器設定檔的端點。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 區域
```
Get-AzureRmTrafficManagerEndpoint -Name <String> -Type <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 面向
```
Get-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmTrafficManagerEndpoint** Cmdlet 會取得 Azure 流量管理器設定檔的端點。

您可以在本機修改這個物件，然後使用 Set-AzureRmTrafficManagerEndpoint Cmdlet 將變更套用至設定檔。
使用 *Name* 和 *Type* 參數指定端點。
您可以使用 *ProfileName* 和 *ResourceGroupName* 參數來指定流量管理器設定檔，或指定 **TrafficManagerProfile** 物件。
或者，您也可以使用管線來傳遞這個值。

## 示例

### 範例1：取得端點
```
PS C:\>$TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
```

這個命令會從名為 [ResourceGroup11] 的資源群組中，從名為 [ContosoProfile] 的設定檔中取得名為 contoso 的 Azure 端點，然後將該物件儲存在 $TrafficManagerEndpoint 變數中。

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
指定此 Cmdlet 所取得之流量管理器端點的名稱。

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

### -ProfileName
指定此 Cmdlet 所取得之流量管理器端點的名稱。

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
這個 Cmdlet 會在此參數指定的群組中取得流量管理器端點。

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

### -TrafficManagerEndpoint
指定此 Cmdlet 取得的流量管理器端點。

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -類型
指定此 Cmdlet 新增至流量管理器設定檔的端點類型。
有效值為： 

- AzureEndpoints
- ExternalEndpoints
- NestedEndpoints

```yaml
Type: System.String
Parameter Sets: Fields
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### TrafficManagerEndpoint 中的 TrafficManager。
形參 "TrafficManagerEndpoint" 接受管線中 "TrafficManagerEndpoint" 類型的值

## 輸出

### TrafficManagerEndpoint 中的 TrafficManager。

## 筆記

## 相關連結

[Disable-AzureRmTrafficManagerEndpoint](./Disable-AzureRmTrafficManagerEndpoint.md)

[Enable-AzureRmTrafficManagerEndpoint](./Enable-AzureRmTrafficManagerEndpoint.md)

[新-AzureRmTrafficManagerEndpoint](./New-AzureRmTrafficManagerEndpoint.md)

[移除-AzureRmTrafficManagerEndpoint](./Remove-AzureRmTrafficManagerEndpoint.md)

[Set-AzureRmTrafficManagerEndpoint](./Set-AzureRmTrafficManagerEndpoint.md)


