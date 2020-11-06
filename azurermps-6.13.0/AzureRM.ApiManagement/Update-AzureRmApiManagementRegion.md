---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: ed26538e54cef189837bd36bf9e6f561df3541f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93445776"
---
# Update-AzureRmApiManagementRegion

## 摘要
更新 PsApiManagement 實例中的現有部署區域。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 說明
**AzureRmApiManagementRegion** Cmdlet 會在所提供實例的 AdditionalRegions 物件集合中，更新 ApiManagement **類型的** **AdditionalRegions** 物件 **PsApiManagementRegion** 中的一個現有實例。 ApiManagement. PsApiManagement..。
這個 Cmdlet 不會部署任何內容，但會更新記憶體中 **PsApiManagement** 的實例。
若要更新 API 管理的部署，請使用已修改的 **PsApiManagementInstance** 到 Update-AzureRmApiManagementDeployment Cmdlet。

## 示例

## 參數

### -ApiManagement
指定要在其中更新現有部署區域的 **PsApiManagement** 實例。

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -容量
指定部署區域的新 SKU 容量值。

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -位置
指定要更新之部署區域的位置。
指定新部署區域在 Api 管理服務支援區域之間的位置。
若要取得有效的位置，請使用 Cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Sku
指定部署區域的新層級值。
有效值為：
- 人員
- 標準
- 佳

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualNetwork
指定部署區域的虛擬網路配置。
傳遞 $null 將會移除該區域的虛擬網路設定。

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### PsApiManagement 中的 ApiManagement。
參數： ApiManagement (ByValue) 

### System.object

### PsApiManagementSku 中的 ApiManagement。

### System.object

### PsApiManagementVirtualNetwork 中的 ApiManagement。

## 輸出

### PsApiManagement 中的 ApiManagement。

## 筆記

## 相關連結

[附加 AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[移除-AzureRmApiManagementRegion](./Remove-AzureRmApiManagementRegion.md)

[更新-AzureRmApiManagementDeployment](./Update-AzureRmApiManagementDeployment.md)
