---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: e64fdd0300f2ccad4c3904d472563bbc30374b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452408"
---
# Get-AzureRmResourceGroupDeployment

## 摘要
取得資源群組中的部署。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### 已設定部署名稱參數。  (預設) 
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 已設定部署識別碼參數。
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmResourceGroupDeployment** Cmdlet 會取得 Azure 資源群組中的部署。
指定 *Name* 或 *Id* 參數來篩選結果。
根據預設， **AzureRmResourceGroupDeployment 會取得** 指定資源群組的所有部署。

Azure 資源是使用者管理的 Azure 實體，例如資料庫伺服器、資料庫或網站。
Azure 資源群組是一個以單位形式部署的 Azure 資源集合。

部署是使資源群組中的資源可供使用的作業。
如需有關 Azure 資源和 Azure 資源群組的詳細資訊，請參閱 New-AzureRmResourceGroup Cmdlet。

您可以使用此 Cmdlet 進行追蹤。
針對調試，請將此 Cmdlet 與 Get-AzureRmLog Cmdlet 搭配使用。

## 示例

### 範例1：取得資源群組的所有部署
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

這個命令會取得 ContosoLabsRG 資源群組的所有部署。
[輸出] 會顯示使用圖庫範本之 WordPress 博客的部署。

### 範例2：依名稱取得部署
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

這個命令會取得 ContosoLabsRG 資源群組的 DeployWebsite01 部署。
您可以使用 **新的 AzureRmResourceGroup** 或 **AzureRmResourceGroupDeployment** Cmdlet，在建立部署時指派名稱。
如果您沒有指派名稱，則 Cmdlet 會根據用來建立部署的範本，提供預設名稱。

### 範例3：取得所有資源群組的部署
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

這個命令會使用 Get-AzureRmResourceGroup Cmdlet 來取得訂閱中的所有資源群組。
命令會使用管線運算子，將資源群組傳遞至目前的 Cmdlet。
目前的 Cmdlet 會取得訂閱中所有資源群組的所有部署，並將結果傳遞給 Format-Table Cmdlet，以顯示其 **ResourceGroupName** 、 **DeploymentName** 和 **ProvisioningState** 屬性值。

## 參數

### -ApiVersion
指定資源提供者支援的 API 版本。
您可以指定不同于預設版本的版本。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -識別碼
指定要取得之資源群組部署的 ID。

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
指定要取得之部署的名稱。
不允許通配字元。

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -預先
表示此 Cmdlet 會在自動決定要使用哪個版本時，考慮預發行 API 版本。

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
指定資源群組的名稱。
此 Cmdlet 會取得此參數指定之資源群組的部署。
不允許通配字元。
這個參數是必要的，而且您只能在每個命令中指定一個資源群組。

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSResourceGroupDeployment 中的 ResourceManagement。
這個 Cmdlet 會傳回資源群組部署。

## 筆記

## 相關連結

[AzureRmResourceGroup](./Get-AzureRmResourceGroup.md)

[新-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[新-AzureRmResourceGroupDeployment](./New-AzureRmResourceGroupDeployment.md)

[移除-AzureRmResourceGroupDeployment](./Remove-AzureRmResourceGroupDeployment.md)

[停止 AzureRmResourceGroupDeployment](./Stop-AzureRmResourceGroupDeployment.md)

[Test-AzureRmResourceGroupDeployment](./Test-AzureRmResourceGroupDeployment.md)


