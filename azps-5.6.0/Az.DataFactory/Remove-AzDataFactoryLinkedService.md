---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 9425D38D-5978-421F-A438-4463068C4628
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactorylinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryLinkedService.md
ms.openlocfilehash: 28b2b5b1e2370e78c77178e3ee07056bacf1a896
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906933"
---
# <span data-ttu-id="b2096-101">Remove-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="b2096-101">Remove-AzDataFactoryLinkedService</span></span>

## <span data-ttu-id="b2096-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b2096-102">SYNOPSIS</span></span>
<span data-ttu-id="b2096-103">從 Azure Data Factory 移除連結服務。</span><span class="sxs-lookup"><span data-stu-id="b2096-103">Removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="b2096-104">語法</span><span class="sxs-lookup"><span data-stu-id="b2096-104">SYNTAX</span></span>

### <span data-ttu-id="b2096-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="b2096-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactoryName] <String> [-Name] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b2096-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b2096-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryLinkedService [-Force] [-DataFactory] <PSDataFactory> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2096-107">描述</span><span class="sxs-lookup"><span data-stu-id="b2096-107">DESCRIPTION</span></span>
<span data-ttu-id="b2096-108">**Remove-AzDataFactoryLinkedService** Cmdlet 會從 Azure Data Factory 移除連結服務。</span><span class="sxs-lookup"><span data-stu-id="b2096-108">The **Remove-AzDataFactoryLinkedService** cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="b2096-109">例子</span><span class="sxs-lookup"><span data-stu-id="b2096-109">EXAMPLES</span></span>

### <span data-ttu-id="b2096-110">範例 1：移除連結的服務</span><span class="sxs-lookup"><span data-stu-id="b2096-110">Example 1: Remove a linked service</span></span>
```
PS C:\>Remove-AzDataFactoryLinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
Confirm
Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
True
```

<span data-ttu-id="b2096-111">此命令會從名為 WikiADF 的資料工廠移除名為 LinkedServiceTest 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="b2096-111">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="b2096-112">此命令會返回 $True。</span><span class="sxs-lookup"><span data-stu-id="b2096-112">This command returns a value of $True.</span></span>

## <span data-ttu-id="b2096-113">參數</span><span class="sxs-lookup"><span data-stu-id="b2096-113">PARAMETERS</span></span>

### <span data-ttu-id="b2096-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b2096-114">-DataFactory</span></span>
<span data-ttu-id="b2096-115">指定 **PSDataFactory** 物件。</span><span class="sxs-lookup"><span data-stu-id="b2096-115">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b2096-116">此 Cmdlet 會從此參數指定的資料工廠移除連結服務。</span><span class="sxs-lookup"><span data-stu-id="b2096-116">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b2096-117">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b2096-117">-DataFactoryName</span></span>
<span data-ttu-id="b2096-118">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2096-118">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b2096-119">此 Cmdlet 會從此參數指定的資料工廠移除連結服務。</span><span class="sxs-lookup"><span data-stu-id="b2096-119">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b2096-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2096-120">-DefaultProfile</span></span>
<span data-ttu-id="b2096-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b2096-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2096-122">-強制</span><span class="sxs-lookup"><span data-stu-id="b2096-122">-Force</span></span>
<span data-ttu-id="b2096-123">表示此 Cmdlet 會移除連結的服務，而不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b2096-123">Indicates that this cmdlet removes a linked service without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="b2096-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="b2096-124">-Name</span></span>
<span data-ttu-id="b2096-125">指定要移除的連結服務名稱。</span><span class="sxs-lookup"><span data-stu-id="b2096-125">Specifies the name of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b2096-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2096-126">-ResourceGroupName</span></span>
<span data-ttu-id="b2096-127">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b2096-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b2096-128">此 Cmdlet 會從此參數指定的群組移除連結服務。</span><span class="sxs-lookup"><span data-stu-id="b2096-128">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b2096-129">-確認</span><span class="sxs-lookup"><span data-stu-id="b2096-129">-Confirm</span></span>
<span data-ttu-id="b2096-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b2096-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2096-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2096-131">-WhatIf</span></span>
<span data-ttu-id="b2096-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b2096-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2096-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b2096-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2096-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2096-134">CommonParameters</span></span>
<span data-ttu-id="b2096-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b2096-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2096-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b2096-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2096-137">輸入</span><span class="sxs-lookup"><span data-stu-id="b2096-137">INPUTS</span></span>

### <span data-ttu-id="b2096-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b2096-138">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b2096-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b2096-139">System.String</span></span>

## <span data-ttu-id="b2096-140">輸出</span><span class="sxs-lookup"><span data-stu-id="b2096-140">OUTPUTS</span></span>

### <span data-ttu-id="b2096-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="b2096-141">System.Void</span></span>

## <span data-ttu-id="b2096-142">筆記</span><span class="sxs-lookup"><span data-stu-id="b2096-142">NOTES</span></span>
* <span data-ttu-id="b2096-143">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="b2096-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b2096-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="b2096-144">RELATED LINKS</span></span>

[<span data-ttu-id="b2096-145">Get-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="b2096-145">Get-AzDataFactoryLinkedService</span></span>](./Get-AzDataFactoryLinkedService.md)

[<span data-ttu-id="b2096-146">New-AzDataFactoryLinkedService</span><span class="sxs-lookup"><span data-stu-id="b2096-146">New-AzDataFactoryLinkedService</span></span>](./New-AzDataFactoryLinkedService.md)


