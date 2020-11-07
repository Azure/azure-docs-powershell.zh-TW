---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/en-us/powershell/module/az.iotcentral/get-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Get-AzIotCentralApp.md
ms.openlocfilehash: a58be60e10be53c1251d8efac5d5fc1551182043
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787593"
---
# Get-AzIotCentralApp

## 摘要
取得一或多個 IoT 中央應用程式的屬性。

## 句法

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

## 說明
根據參數集，取得特定 IoT 中央應用程式的中繼資料，或是資源群組或訂閱中的所有應用程式。 

## 示例

### 範例1取得特定的 IoT 中央應用程式。
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

取得指定 IoT 中央應用程式的中繼資料。

範例輸出：

ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 ： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain （不適用）

### 範例2在訂閱中取得 IoT 中央應用程式。
```powershell
PS C:\> Get-AzIotCentralApp
```

取得目前訂閱中所有 IoT 中央應用程式的中繼資料。

範例輸出：

ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 ： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain （不適用）

ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName2/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName2 名稱： MyAppResourceName2 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku：： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱2子域： IoTCentral 範本： iotc-default@1.0.0 訂閱： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain2

### 範例3在 [資源群組] 中取得 IoT 中央應用程式。
```powershell
PS C:\> Get-AzIotCentralApp -ResourceGroupName "MyResourceGroupName"
```

取得所提供之資源群組中所有 IoT 中心應用程式的中繼資料。

範例輸出：

ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName 名稱： MyAppResourceName 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱子域： IoTCentral 範本： iotc-default@1.0.0 ： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain （不適用）

ResourceId：/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroupName/providers/Microsoft。IoTCentral/IoTApps/MyAppResourceName2 名稱： MyAppResourceName2 類型： Microsoft. IoTCentral/IoTApps Location： westus 標記： {[key，val]} Sku：： ApplicationId： XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX DisplayName： [我的自訂顯示名稱2子域： IoTCentral 範本： iotc-default@1.0.0 訂閱： xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx-Xxxx PSIotCentralAppSkuInfo： MyAppSubdomain2

## 參數

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

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
資源群組的名稱。

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
Iot 中心應用程式資源識別碼。

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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### System.object

## 輸出

### PSIotCentralApp 中的 IotCentral。

## 筆記

## 相關連結
