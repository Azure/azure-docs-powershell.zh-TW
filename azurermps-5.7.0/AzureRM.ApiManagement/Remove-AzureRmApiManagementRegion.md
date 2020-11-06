---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 0376c80e769153c448cdc23d8465966026584fcf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93457511"
---
# Remove-AzureRmApiManagementRegion

## 摘要
從 PsApiManagement 實例移除現有的部署區域。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
AzureRmApiManagementRegion Cmdlet 會從已提供 type **PsApiManagementRegion ApiManagement** 的實例的 AdditionalRegions 集合中移除類型的實例， **並** 從 **的** 中移除的 **。**
這個 Cmdlet 不會自行修改部署，但會更新記憶體中 **PsApiManagement** 的實例。
若要更新 API 管理的部署，請將修改過的 **PsApiManagementInstance** 傳遞到 **update-AzureRmApiManagement** 。

## 示例

### 範例1：從 PsApiManagement 實例中移除區域
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

這個命令會從 **PsApiManagement** 實例中移除名為「美國東部」的地區。

### 範例2：使用一系列命令從 PsApiManagement 實例中移除區域
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

這個第一個命令會從名為 Contoso 的資源群組（名為 ContosoApi）中取得 **PsApiManagement** 的實例。
然後，最後一個命令會從該實例移除名為 East 的地區，然後更新部署。

## 參數

### -ApiManagement
指定此 Cmdlet 移除其他部署區域的 **PsApiManagement** 實例。

```yaml
Type: PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。
 
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

### -位置
指定此 Cmdlet 移除之區域的位置。

指定新部署區域在 Api 管理服務支援區域之間的位置。
若要取得有效的位置，請使用 Cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置

```yaml
Type: String
Parameter Sets: (All)
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

### PsApiManagement
形參 "ApiManagement" 接受管線中 "PsApiManagement" 類型的值

## 輸出

### PsApiManagement 中的 ApiManagement。

## 筆記

## 相關連結

[附加 AzureRmApiManagementRegion](./Add-AzureRmApiManagementRegion.md)

[更新-AzureRmApiManagementRegion](./Update-AzureRmApiManagementRegion.md)


