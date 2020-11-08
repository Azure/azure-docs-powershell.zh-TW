---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azmanagementgroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzManagementGroupDeploymentTemplate.md
ms.openlocfilehash: 536d8f0d7f92e4ca880998293d74d0fc2f1617f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94126870"
---
# Save-AzManagementGroupDeploymentTemplate

## 摘要
將部署範本儲存至檔案。

## 句法

### SaveByDeploymentName (預設) 
```
Save-AzManagementGroupDeploymentTemplate -ManagementGroupId <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SaveByDeploymentObject
```
Save-AzManagementGroupDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 說明
AzManagementGroupDeploymentTemplate Cmdlet 會將部署範本 **儲存**  到管理群組上部署的 JSON 檔案。

## 示例

### 範例1
```powershell
PS C:\> Save-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -DeploymentName "TestDeployment"
```

這個命令會從 TestDeployment 取得部署範本，並將它儲存為目前目錄中的 JSON 檔案。

### 範例2：取得部署並儲存其範本
```
PS C:\>Get-AzManagementGroupDeploymentTemplate -ManagementGroupId "myMG" -Name "RolesDeployment" | Save-AzManagementGroupDeploymentTemplate
```

這個命令會取得管理群組 "myMG" 的部署 "RolesDeployment"，並儲存其範本。

## 參數

### -ApiVersion
設定時，會指出要使用的資源提供者 API 版本。
如果未指定，API 版本會自動決定為最新的可用。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentName
部署名稱。

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentObject
部署物件。

```yaml
Type: PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Force
不要要求確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementGroupId
管理群組識別碼。

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
範本檔案的輸出路徑。

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -預先
設定時，表示 Cmdlet 應該使用預發行 API 版本，以便自動判斷要使用的版本。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -確認
在執行 Cmdlet 之前提示您進行確認。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
顯示在執行 Cmdlet 時會發生什麼情況。
未執行 Cmdlet。

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment

## 輸出

### PSTemplatePath 中的 SdkModels （）

## 筆記

## 相關連結
