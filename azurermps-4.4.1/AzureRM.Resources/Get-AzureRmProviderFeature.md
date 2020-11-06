---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2970E81E-A788-4829-B1FF-B522A91DE4B1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmProviderFeature.md
ms.openlocfilehash: 5e4802aff3c887a76cc376cac001ac20d9a98eea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452427"
---
# Get-AzureRmProviderFeature

## 摘要
取得 Azure 提供者功能的相關資訊。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### ListAvailableParameterSet (預設) 
```
Get-AzureRmProviderFeature [-ProviderNamespace <String>] [-ListAvailable]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetFeature
```
Get-AzureRmProviderFeature -ProviderNamespace <String> -FeatureName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmProviderFeature** Cmdlet 會取得 Azure 提供者功能的功能名稱、提供者名稱及註冊狀態。

## 示例

### 範例1：取得所有可用的功能
```
PS C:\>Get-AzureRmProviderFeature -ListAvailable
```

這個命令會取得所有可用的功能。

### 範例2：取得特定功能的相關資訊
```
PS C:\>Get-AzureRmProviderFeature -FeatureName "AllowPreReleaseRegions" -ProviderNamespace "Microsoft.Compute"
```

這個命令會取得指定提供者的功能，其名為 AllowPreReleaseRegions 之功能的資訊。

## 參數

### -功能
指定要取得的功能名稱。

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ListAvailable
表示此 Cmdlet 取得所有功能。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProviderNamespace
指定此 Cmdlet 取得提供者功能的命名空間。

```yaml
Type: System.String
Parameter Sets: ListAvailableParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetFeature
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

## 輸出

### [System.object]。清單 ' 1 [PSProviderFeature] SdkModels. 命令.]

## 筆記

## 相關連結

[Register-AzureRmProviderFeature](./Register-AzureRmProviderFeature.md)


