---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: 2d79857df255bb960c51b87c536013921f3b1c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101913906"
---
# Get-AzIotCentralApp

## 簡介
為一或多個 IoT 中心應用程式獲取屬性。

## 語法

### ListIotCentralAppsParameterSet (預設) 
```
Get-AzIotCentralApp [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InteractiveIotCentralParameterSet
```
Get-AzIotCentralApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceIdParameterSet
```
Get-AzIotCentralApp -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 描述
根據參數集，為特定 IoT 中心應用程式或資源群組或訂閱內的所有應用程式獲取中繼資料。 

## 例子

### 範例 1 取得特定的 IoT 中心應用程式。
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

為指定的 IoT 中心應用程式獲取中繼資料。

輸出範例：

ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name ： MyAppResourceName 類型 ： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： {[key， val]} Sku ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName ： MyAppSubdomain 範本 ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName

### 範例 2 在訂閱中取得 IoT 中心應用程式。
```powershell
PS C:\> Get-AzIotCentralApp
```

在目前的訂閱中，獲得所有 IoT 中心應用程式的中繼資料。

輸出範例：

ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name ： MyAppResourceName 類型 ： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： {[key， val]} Sku ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName ： MyAppSubdomain 範本 ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName

ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 名稱： MyAppResourceName2 類型： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： {[key， val]} SKU ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName ： MyAppSubdomain2 範本 ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName2

### 範例 3 在資源群組中取得 IoT 中心應用程式。
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

在提供的資源群組中，獲得所有 IoT 中心應用程式的中繼資料。

輸出範例：

ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName Name ： MyAppResourceName 類型 ： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： {[key， val]} Sku ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName ： MyAppSubdomain 範本 ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName

ResourceId ：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft .IoTCentral/IoTApps/MyAppResourceName2 名稱： MyAppResourceName2 類型： Microsoft.IoTCentral/IoTApps Location ： westus Tag ： {[key， val]} Sku ： Microsoft.Azure.Commands.IotCentral.models.PSIotCentralAppSkuInfo ApplicationId ： XXXXXXXX-XXXX-XXXX-XXXX-XXXX-XXXX-XXXXXXXXX DisplayName ： MyAppSubdomain2 範本 ： iotc-default@1.0.0 SubscriptionId ： XXXXXXXX-XXXX-XXXXXXXXX ResourceGroupName ： MyResourceGroupName

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

### -名稱
Iot 中心應用程式資源的名稱。

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
資源組的名稱。

```yaml
Type: System.String
Parameter Sets: ListIotCentralAppsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Iot Central Application Resource Id.

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.IotCentral.models.PSIotCentralApp

## 筆記

## 相關連結
