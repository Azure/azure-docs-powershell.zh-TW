---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: eb79b6a46f2eaadfc6a42159706c37017cdac8d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911318"
---
# Get-AzResourceGroupDeployment

## 簡介
在資源群組中進行部署。

## 語法

### GetByResourceGroupDeploymentName (預設) 
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupDeploymentId
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 描述
**Get-AzResourceGroupDeployment** Cmdlet 取得 Azure 資源群組中的部署。
指定 *名稱* 或 *Id* 參數以篩選結果。
根據預設 **，Get-AzResourceGroupDeployment 會** 取得指定資源群組的所有部署。
Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫或網站。
Azure 資源群組是部署為一個單位的 Azure 資源集合。
部署是一項作業，可讓資源群組中的資源可供使用。
有關 Azure 資源與 Azure 資源群組的資訊，請參閱 New-AzResourceGroup Cmdlet。
您可以使用此 Cmdlet 進行追蹤。
如要進行比對，請使用此 Cmdlet Get-AzLog Cmdlet。

## 例子

### 範例 1：取得資源群組的所有部署
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

此命令會獲得 ContosoLabsRG 資源群組的所有部署。
輸出顯示使用圖庫範本之 WordPress 部落格的部署。

### 範例 2：根據名稱取得部署
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

此命令會獲得 ContosoLabsRG 資源群組的 DeployWebsite01 部署。
您可以使用 **New-AzResourceGroup** 或 **New-AzResourceGroupDeployment** Cmdlet 為部署指派名稱。
如果您沒有指派名稱，Cmdlet 會根據用來建立部署的範本提供預設名稱。

### 範例 3：取得所有資源群組的部署
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

此命令會使用 Cmdlet，在訂閱中Get-AzResourceGroup群組。
該命令會使用管線運算子，將資源群組傳遞至目前的 Cmdlet。
目前的 Cmdlet 會取得訂閱中所有資源群組的所有部署，並且將結果傳遞至 Format-Table Cmdlet 以顯示 **其 ResourceGroupName、DeploymentName** 和 **ProvisioningState** 屬性值。

## 參數

### -DefaultProfile
用於與 Azure 通訊的認證、帳戶、租使用者和訂閱

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

### -Id
指定要取得的資源群組部署識別碼。

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要取得之部署的名稱。
不允許萬用字元。

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮測試版 API 版本。

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
指定資源組的名稱。
Cmdlet 會針對此參數指定的資源群組獲得部署。
不允許萬用字元。
此參數為必填項，而且每個命令中只能指定一個資源群組。

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。 詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)

## 輸入

### System.String

## 輸出

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment

## 筆記

## 相關連結

[Get-AzResourceGroup](./Get-AzResourceGroup.md)

[New-AzResourceGroup](./New-AzResourceGroup.md)

[New-AzResourceGroupDeployment](./New-AzResourceGroupDeployment.md)

[Remove-AzResourceGroupDeployment](./Remove-AzResourceGroupDeployment.md)

[Stop-AzResourceGroupDeployment](./Stop-AzResourceGroupDeployment.md)

[Test-AzResourceGroupDeployment](./Test-AzResourceGroupDeployment.md)


