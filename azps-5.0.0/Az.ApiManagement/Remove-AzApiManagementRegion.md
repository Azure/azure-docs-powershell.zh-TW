---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 70816b054acc7667d2246ea72901c65890f9389e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94285693"
---
# Remove-AzApiManagementRegion

## 摘要
從 PsApiManagement 實例移除現有的部署區域。

## 句法

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
AzApiManagementRegion Cmdlet 會從已提供 type **PsApiManagementRegion ApiManagement** 的實例的 AdditionalRegions 集合中移除類型的實例， **並** 從 **的** 中移除的 **。**
這個 Cmdlet 不會自行修改部署，但會更新記憶體中 **PsApiManagement** 的實例。
若要更新 API 管理的部署，請將修改過的 **PsApiManagementInstance** 傳遞到 **AzApiManagement** 。

## 示例

### 範例1：從 PsApiManagement 實例中移除區域
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

這個命令會從 **PsApiManagement** 實例中移除名為「美國東部」的地區。

### 範例2：使用一系列命令從 PsApiManagement 實例中移除區域
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

這個第一個命令會從名為 Contoso 的資源群組（名為 ContosoApi）中取得 **PsApiManagement** 的實例。
然後，最後一個命令會從該實例移除名為 East 的地區，然後更新部署。

## 參數

### -ApiManagement
指定此 Cmdlet 移除其他部署區域的 **PsApiManagement** 實例。

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

### -DefaultProfile

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

### -位置
指定此 Cmdlet 移除之區域的位置。
指定新部署區域在 Api 管理服務支援區域之間的位置。
若要取得有效的位置，請使用 Cmdlet Get-AzResourceProvider ProviderNamespace "ApiManagement" |其中 {$ _。ResourceTypes [0]。ResourceTypeName-eq "service"} |Select-Object 位置

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### PsApiManagement 中的 ApiManagement。

### System.object

## 輸出

### PsApiManagement 中的 ApiManagement。

## 筆記

## 相關連結

[附加 AzApiManagementRegion](./Add-AzApiManagementRegion.md)

[更新-AzApiManagementRegion](./Update-AzApiManagementRegion.md)


