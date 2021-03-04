---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: E1461540-DEAE-43C3-83DF-7DF3FE8D4EC0
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorygateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryGateway.md
ms.openlocfilehash: eb9100bf4843d7213d2fbb89ac1827ba7ee1e509
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903270"
---
# <span data-ttu-id="6d3dc-101">Remove-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6d3dc-101">Remove-AzDataFactoryGateway</span></span>

## <span data-ttu-id="6d3dc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6d3dc-102">SYNOPSIS</span></span>
<span data-ttu-id="6d3dc-103">從 Azure Data Factory 移除閘道。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-103">Removes a gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="6d3dc-104">語法</span><span class="sxs-lookup"><span data-stu-id="6d3dc-104">SYNTAX</span></span>

### <span data-ttu-id="6d3dc-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="6d3dc-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryGateway [-DataFactoryName] <String> [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d3dc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="6d3dc-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryGateway [-DataFactory] <PSDataFactory> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d3dc-107">描述</span><span class="sxs-lookup"><span data-stu-id="6d3dc-107">DESCRIPTION</span></span>
<span data-ttu-id="6d3dc-108">**Remove-AzDataFactoryGateway** Cmdlet 會從 Azure Data Factory 移除指定的閘道。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-108">The **Remove-AzDataFactoryGateway** cmdlet removes the specified gateway from Azure Data Factory.</span></span>

## <span data-ttu-id="6d3dc-109">例子</span><span class="sxs-lookup"><span data-stu-id="6d3dc-109">EXAMPLES</span></span>

### <span data-ttu-id="6d3dc-110">範例 1：移除閘道</span><span class="sxs-lookup"><span data-stu-id="6d3dc-110">Example 1: Remove a gateway</span></span>
```
PS C:\>Remove-AzDataFactoryGateway -Name "ContosoGateway" -DataFactoryName "WikiADF" -ResourceGroupName "ADF"
Confirm
Are you sure you want to remove gateway 'ContosoGateway' in data factory 'WikiADF'? 
 [Y] Yes  [N] No  [S] Suspend  [?] Help (default is Y): Y
True
```

<span data-ttu-id="6d3dc-111">此命令會從名為 WikiADF 的資料工廠移除名為 ContosoGateway 的閘道。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-111">This command removes the gateway named ContosoGateway from the data factory named WikiADF.</span></span>

## <span data-ttu-id="6d3dc-112">參數</span><span class="sxs-lookup"><span data-stu-id="6d3dc-112">PARAMETERS</span></span>

### <span data-ttu-id="6d3dc-113">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="6d3dc-113">-DataFactory</span></span>
<span data-ttu-id="6d3dc-114">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-114">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="6d3dc-115">此 Cmdlet 會從此參數指定的資料工廠移除閘道。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-115">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3dc-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="6d3dc-116">-DataFactoryName</span></span>
<span data-ttu-id="6d3dc-117">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-117">Specifies the name of a data factory.</span></span>
<span data-ttu-id="6d3dc-118">此 Cmdlet 會從此參數指定的資料工廠移除閘道。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-118">This cmdlet removes a gateway from the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3dc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d3dc-119">-DefaultProfile</span></span>
<span data-ttu-id="6d3dc-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6d3dc-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6d3dc-121">-強制</span><span class="sxs-lookup"><span data-stu-id="6d3dc-121">-Force</span></span>
<span data-ttu-id="6d3dc-122">表示此 Cmdlet 會移除閘道，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-122">Indicates that this cmdlet removes a gateway without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="6d3dc-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="6d3dc-123">-Name</span></span>
<span data-ttu-id="6d3dc-124">指定要移除的閘道名稱。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-124">Specifies the name of the gateway to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3dc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d3dc-125">-ResourceGroupName</span></span>
<span data-ttu-id="6d3dc-126">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-126">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="6d3dc-127">此 Cmdlet 會移除屬於此參數指定之群組的閘道。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-127">This cmdlet removes a gateway that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d3dc-128">-確認</span><span class="sxs-lookup"><span data-stu-id="6d3dc-128">-Confirm</span></span>
<span data-ttu-id="6d3dc-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3dc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d3dc-130">-WhatIf</span></span>
<span data-ttu-id="6d3dc-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d3dc-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d3dc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d3dc-133">CommonParameters</span></span>
<span data-ttu-id="6d3dc-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d3dc-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6d3dc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d3dc-136">輸入</span><span class="sxs-lookup"><span data-stu-id="6d3dc-136">INPUTS</span></span>

### <span data-ttu-id="6d3dc-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6d3dc-137">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="6d3dc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6d3dc-138">System.String</span></span>

## <span data-ttu-id="6d3dc-139">輸出</span><span class="sxs-lookup"><span data-stu-id="6d3dc-139">OUTPUTS</span></span>

### <span data-ttu-id="6d3dc-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6d3dc-140">System.Boolean</span></span>

## <span data-ttu-id="6d3dc-141">筆記</span><span class="sxs-lookup"><span data-stu-id="6d3dc-141">NOTES</span></span>
* <span data-ttu-id="6d3dc-142">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="6d3dc-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6d3dc-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="6d3dc-143">RELATED LINKS</span></span>

[<span data-ttu-id="6d3dc-144">Get-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6d3dc-144">Get-AzDataFactoryGateway</span></span>](./Get-AzDataFactoryGateway.md)

[<span data-ttu-id="6d3dc-145">New-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6d3dc-145">New-AzDataFactoryGateway</span></span>](./New-AzDataFactoryGateway.md)

[<span data-ttu-id="6d3dc-146">Set-AzDataFactoryGateway</span><span class="sxs-lookup"><span data-stu-id="6d3dc-146">Set-AzDataFactoryGateway</span></span>](./Set-AzDataFactoryGateway.md)


