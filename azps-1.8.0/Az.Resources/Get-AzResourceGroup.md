---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 81a4780fb4b4b2249c135104ab3d939d71a93684
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93620872"
---
# Get-AzResourceGroup

## 摘要
取得資源群組。

## 句法

### GetByResourceGroupName (預設) 
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupId
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzResourceGroup** Cmdlet 會在目前的訂閱中取得 Azure 資源群組。
您可以取得所有資源群組，或是依名稱或其他屬性來指定資源群組。
根據預設，這個 Cmdlet 會取得目前訂閱中的所有資源群組。
如需有關 Azure 資源和 Azure 資源群組的詳細資訊，請參閱 New-AzResourceGroup Cmdlet。

## 示例

### 範例1：依名稱取得資源群組
```
PS C:\>Get-AzResourceGroup -Name "EngineerBlog"
```

這個命令會在您的訂閱中取得名為 EngineerBlog 的 Azure 資源群組。

### 範例2：取得資源群組的所有標籤
```
PS C:\>(Get-AzResourceGroup -Name "ContosoRG").Tags
```

這個命令會取得名為 ContosoRG 的資源群組，並顯示與該群組相關聯的標籤。

### 範例3：依位置顯示資源群組
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### 範例4：顯示特定位置中所有資源群組的名稱
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### 範例5：顯示其名稱以 Web 內容開頭的資源群組
```
PS C:\> Get-AzResourceGroup | Where ResourceGroupName -like WebServer*
```

### 範例6：依名稱取得資源群組
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog*"
```

這個命令會在您的訂閱中取得以 "EngineerBlog" 開頭的 Azure 資源群組。

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

### -DefaultProfile
用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱

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
指定要取得之資源群組的識別碼。
不允許通配字元。

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -位置
指定要取得之資源群組的位置。

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -名稱
指定要取得之資源群組的名稱。 這個參數支援字串開頭和/或結尾的萬用字元。

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
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

### -Tag
[標記 hashtable] 來篩選資源群組的依據。

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。

## 輸入

### System.object

### [System.object] 集合. Hashtable

## 輸出

### PSResourceGroup 中的 SdkModels （）

## 筆記

## 相關連結

[新-AzResourceGroup](./New-AzResourceGroup.md)

[移除-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)


