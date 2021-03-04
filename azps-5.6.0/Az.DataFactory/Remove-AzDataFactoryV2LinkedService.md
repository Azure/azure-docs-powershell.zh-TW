---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/remove-azdatafactoryv2linkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2LinkedService.md
ms.openlocfilehash: 87a50c69449437401ff26b76b87cf0f334ab8d71
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101907894"
---
# <span data-ttu-id="212be-101">Remove-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="212be-101">Remove-AzDataFactoryV2LinkedService</span></span>

## <span data-ttu-id="212be-102">簡介</span><span class="sxs-lookup"><span data-stu-id="212be-102">SYNOPSIS</span></span>
<span data-ttu-id="212be-103">從 Data Factory 移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="212be-103">Removes a linked service from Data Factory.</span></span>

## <span data-ttu-id="212be-104">語法</span><span class="sxs-lookup"><span data-stu-id="212be-104">SYNTAX</span></span>

### <span data-ttu-id="212be-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="212be-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2LinkedService [-Name] <String> [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="212be-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="212be-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2LinkedService [-InputObject] <PSLinkedService> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="212be-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="212be-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2LinkedService [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="212be-108">描述</span><span class="sxs-lookup"><span data-stu-id="212be-108">DESCRIPTION</span></span>
<span data-ttu-id="212be-109">Cmdlet Remove-AzDataFactoryV2LinkedService Azure Data Factory 移除連結的服務。</span><span class="sxs-lookup"><span data-stu-id="212be-109">The Remove-AzDataFactoryV2LinkedService cmdlet removes a linked service from Azure Data Factory.</span></span>

## <span data-ttu-id="212be-110">例子</span><span class="sxs-lookup"><span data-stu-id="212be-110">EXAMPLES</span></span>

### <span data-ttu-id="212be-111">範例 1：移除連結的服務</span><span class="sxs-lookup"><span data-stu-id="212be-111">Example 1: Remove a linked service</span></span>
```
PS C:\> Remove-AzDataFactoryV2LinkedService -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "LinkedServiceTest"
          Confirm
          Are you sure you want to remove linked service 'LinkedServiceTest' in data factory 'WikiADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="212be-112">此命令會從名為 WikiADF 的資料工廠移除名為 LinkedServiceTest 的連結服務。</span><span class="sxs-lookup"><span data-stu-id="212be-112">This command removes the linked service named LinkedServiceTest from the data factory named WikiADF.</span></span>
<span data-ttu-id="212be-113">此命令會返回 $True。</span><span class="sxs-lookup"><span data-stu-id="212be-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="212be-114">參數</span><span class="sxs-lookup"><span data-stu-id="212be-114">PARAMETERS</span></span>

### <span data-ttu-id="212be-115">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="212be-115">-DataFactoryName</span></span>
<span data-ttu-id="212be-116">指定資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="212be-116">Specifies the name of a data factory.</span></span>
<span data-ttu-id="212be-117">此 Cmdlet 會從此參數指定的資料工廠移除連結服務。</span><span class="sxs-lookup"><span data-stu-id="212be-117">This cmdlet removes a linked service from the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="212be-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="212be-118">-DefaultProfile</span></span>
<span data-ttu-id="212be-119">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="212be-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="212be-120">-強制</span><span class="sxs-lookup"><span data-stu-id="212be-120">-Force</span></span>
<span data-ttu-id="212be-121">執行 Cmdlet 而不提示確認。</span><span class="sxs-lookup"><span data-stu-id="212be-121">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="212be-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="212be-122">-InputObject</span></span>
<span data-ttu-id="212be-123">指定要移除的 LinkedService 物件。</span><span class="sxs-lookup"><span data-stu-id="212be-123">Specifies the LinkedService object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="212be-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="212be-124">-Name</span></span>
<span data-ttu-id="212be-125">指定要移除的連結服務名稱。</span><span class="sxs-lookup"><span data-stu-id="212be-125">Specifies the name of the linked service to remove.</span></span>
<span data-ttu-id="212be-126">連結服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="212be-126">Name of the linked service.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: LinkedServiceName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212be-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="212be-127">-ResourceGroupName</span></span>
<span data-ttu-id="212be-128">指定 Azure 資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="212be-128">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="212be-129">此 Cmdlet 會從此參數指定的群組移除連結服務。</span><span class="sxs-lookup"><span data-stu-id="212be-129">This cmdlet removes a linked service from the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="212be-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="212be-130">-ResourceId</span></span>
<span data-ttu-id="212be-131">要移除之連結服務的 Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="212be-131">The Azure resource ID of the linked service to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="212be-132">-確認</span><span class="sxs-lookup"><span data-stu-id="212be-132">-Confirm</span></span>
<span data-ttu-id="212be-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="212be-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212be-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="212be-134">-WhatIf</span></span>
<span data-ttu-id="212be-135">顯示如果 Cmdlet 執行，但不執行 Cmdlet 會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="212be-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="212be-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="212be-136">CommonParameters</span></span>
<span data-ttu-id="212be-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="212be-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="212be-138">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="212be-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="212be-139">輸入</span><span class="sxs-lookup"><span data-stu-id="212be-139">INPUTS</span></span>

### <span data-ttu-id="212be-140">Microsoft.Azure.Commands.DataFactoryV2.models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="212be-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSLinkedService</span></span>

### <span data-ttu-id="212be-141">System.String</span><span class="sxs-lookup"><span data-stu-id="212be-141">System.String</span></span>

## <span data-ttu-id="212be-142">輸出</span><span class="sxs-lookup"><span data-stu-id="212be-142">OUTPUTS</span></span>

### <span data-ttu-id="212be-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="212be-143">System.Void</span></span>

## <span data-ttu-id="212be-144">筆記</span><span class="sxs-lookup"><span data-stu-id="212be-144">NOTES</span></span>
<span data-ttu-id="212be-145">關鍵字：azure、azurerm、arm、resource、management、manager、data、azure</span><span class="sxs-lookup"><span data-stu-id="212be-145">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="212be-146">相關連結</span><span class="sxs-lookup"><span data-stu-id="212be-146">RELATED LINKS</span></span>

[<span data-ttu-id="212be-147">Get-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="212be-147">Get-AzDataFactoryV2LinkedService</span></span>]()

[<span data-ttu-id="212be-148">Set-AzDataFactoryV2LinkedService</span><span class="sxs-lookup"><span data-stu-id="212be-148">Set-AzDataFactoryV2LinkedService</span></span>]()

