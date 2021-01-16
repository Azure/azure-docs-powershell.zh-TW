---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98282944"
---
# Get-AzTenantDeployment

## 摘要
在租使用者範圍中取得部署

## 句法

### GetByDeploymentName (預設) 
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetByDeploymentId
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzTenantDeployment** Cmdlet 會取得租使用者範圍內的部署。
指定 *Name* 或 *Id* 參數來篩選結果。
根據預設， **AzTenantDeployment 會取得** 租使用者範圍內的所有部署。

## 示例

### 範例1：取得租使用者範圍內的所有部署
```
PS C:\>Get-AzTenantDeployment
```

這個命令會取得目前租使用者範圍內的所有部署。

### 範例2：依名稱取得部署
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

這個命令會在目前的租使用者範圍內取得「Deploy01」部署。
您可以在使用 **新的 AzTenantDeployment** Cmdlet 建立部署時，將名稱指派給部署。
如果您沒有指派名稱，則 Cmdlet 會根據用來建立部署的範本，提供預設名稱。

### 範例3：依識別碼取得部署
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

這個命令會在租使用者範圍中取得「Deploy01」部署。

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

### -識別碼
部署的完全限定資源識別碼。
範例：/providers/Microsoft.Resources/deployments/{deploymentName}

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -名稱
部署的名稱。

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -預先
設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。

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

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### 所有

## 輸出

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## 筆記

## 相關連結
