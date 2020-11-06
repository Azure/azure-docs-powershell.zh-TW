---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroup.md
ms.openlocfilehash: 73defde38ab34bc81adf904d5139308dfd556f79
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448256"
---
# Get-AzureRmResourceGroup

## 摘要
取得資源群組。

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 句法

### GetByResourceGroupName (預設) 
```
Get-AzureRmResourceGroup [-Name <String>] [-Location <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupId
```
Get-AzureRmResourceGroup [-Location <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 說明
**AzureRmResourceGroup** Cmdlet 會在目前的訂閱中取得 Azure 資源群組。
您可以取得所有資源群組，或是依名稱或其他屬性來指定資源群組。
根據預設，這個 Cmdlet 會取得目前訂閱中的所有資源群組。
如需有關 Azure 資源和 Azure 資源群組的詳細資訊，請參閱 New-AzureRmResourceGroup Cmdlet。

## 示例

### 範例1：依名稱取得資源群組
```
PS C:\>Get-AzureRmResourceGroup -Name "EngineerBlog"
```

這個命令會在您的訂閱中取得名為 EngineerBlog 的 Azure 資源群組。

### 範例2：取得資源群組的所有標籤
```
PS C:\>(Get-AzureRmResourceGroup -Name "ContosoRG").Tags
```

這個命令會取得名為 ContosoRG 的資源群組，並顯示與該群組相關聯的標籤。

### 範例3：依位置顯示資源群組
```
PS C:\> Get-AzureRmResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### 範例4：顯示特定位置中所有資源群組的名稱
```
PS C:\> Get-AzureRmResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### 範例5：顯示其名稱以 Web 內容開頭的資源群組
```
PS C:\> Get-AzureRmResourceGroup | Where ResourceGroupName -like WebServer*
```

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
Position: Named
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
Position: Named
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
這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。 如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。

## 輸入

### 所有

## 輸出

### PSResourceGroup 中的 ResourceManagement

## 筆記

## 相關連結

[新-AzureRmResourceGroup](./New-AzureRmResourceGroup.md)

[移除-AzureRmResourceGroup](./Remove-AzureRmResourceGroup.md)

[Set-AzureRmResourceGroup](./Set-AzureRmResourceGroup.md)


