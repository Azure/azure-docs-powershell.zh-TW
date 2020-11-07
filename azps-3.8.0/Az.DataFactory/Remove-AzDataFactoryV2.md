---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2.md
ms.openlocfilehash: c396455804f6bb501fa6439fceffb0eb45875516
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956415"
---
# <span data-ttu-id="21aed-101">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="21aed-101">Remove-AzDataFactoryV2</span></span>

## <span data-ttu-id="21aed-102">摘要</span><span class="sxs-lookup"><span data-stu-id="21aed-102">SYNOPSIS</span></span>
<span data-ttu-id="21aed-103">移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="21aed-103">Removes a data factory.</span></span>

## <span data-ttu-id="21aed-104">句法</span><span class="sxs-lookup"><span data-stu-id="21aed-104">SYNTAX</span></span>

### <span data-ttu-id="21aed-105">ByFactoryName (預設) </span><span class="sxs-lookup"><span data-stu-id="21aed-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21aed-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="21aed-106">ByFactoryObject</span></span>
```
Remove-AzDataFactoryV2 [-InputObject] <PSDataFactory> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="21aed-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="21aed-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2 [-ResourceId] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21aed-108">說明</span><span class="sxs-lookup"><span data-stu-id="21aed-108">DESCRIPTION</span></span>
<span data-ttu-id="21aed-109">Remove-AzDataFactoryV2 Cmdlet 會移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="21aed-109">The Remove-AzDataFactoryV2 cmdlet removes a data factory.</span></span>

## <span data-ttu-id="21aed-110">示例</span><span class="sxs-lookup"><span data-stu-id="21aed-110">EXAMPLES</span></span>

### <span data-ttu-id="21aed-111">範例1：移除資料工廠</span><span class="sxs-lookup"><span data-stu-id="21aed-111">Example 1: Remove a data factory</span></span>
```
PS C:\> Remove-AzDataFactoryV2 -Name "WikiADF" -ResourceGroupName "ADF"
          Confirm
          Are you sure you want to remove data factory 'WikiADF' in resource group 'ADF'?
          [Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
          True
```

<span data-ttu-id="21aed-112">這個命令會從名為 [ADF] 的資源群組中移除名為 WikiADF 的資料工廠。</span><span class="sxs-lookup"><span data-stu-id="21aed-112">This command removes the data factory named WikiADF from the resource group named ADF.</span></span>
<span data-ttu-id="21aed-113">這個命令會傳回 $True 的值。</span><span class="sxs-lookup"><span data-stu-id="21aed-113">This command returns a value of $True.</span></span>

## <span data-ttu-id="21aed-114">參數</span><span class="sxs-lookup"><span data-stu-id="21aed-114">PARAMETERS</span></span>

### <span data-ttu-id="21aed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21aed-115">-DefaultProfile</span></span>
<span data-ttu-id="21aed-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="21aed-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21aed-117">-Force</span><span class="sxs-lookup"><span data-stu-id="21aed-117">-Force</span></span>
<span data-ttu-id="21aed-118">在不提示確認的情況下執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="21aed-118">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="21aed-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="21aed-119">-InputObject</span></span>
<span data-ttu-id="21aed-120">指定要移除的 DataFactory 物件。</span><span class="sxs-lookup"><span data-stu-id="21aed-120">Specifies the DataFactory object to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21aed-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="21aed-121">-Name</span></span>
<span data-ttu-id="21aed-122">指定要移除的資料工廠的名稱。</span><span class="sxs-lookup"><span data-stu-id="21aed-122">Specifies the name of the data factory to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21aed-123">-ResourceGroupName</span></span>
<span data-ttu-id="21aed-124">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="21aed-124">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="21aed-125">這個 Cmdlet 會從此參數指定的群組中移除資料工廠。</span><span class="sxs-lookup"><span data-stu-id="21aed-125">This cmdlet removes a data factory from the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21aed-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="21aed-126">-ResourceId</span></span>
<span data-ttu-id="21aed-127">Azure 資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="21aed-127">The Azure resource ID.</span></span>

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

### <span data-ttu-id="21aed-128">-確認</span><span class="sxs-lookup"><span data-stu-id="21aed-128">-Confirm</span></span>
<span data-ttu-id="21aed-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="21aed-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21aed-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21aed-130">-WhatIf</span></span>
<span data-ttu-id="21aed-131">顯示當 Cmdlet 執行但不執行 Cmdlet 時，會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="21aed-131">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="21aed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21aed-132">CommonParameters</span></span>
<span data-ttu-id="21aed-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="21aed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21aed-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="21aed-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21aed-135">輸入</span><span class="sxs-lookup"><span data-stu-id="21aed-135">INPUTS</span></span>

### <span data-ttu-id="21aed-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="21aed-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="21aed-137">System.object</span><span class="sxs-lookup"><span data-stu-id="21aed-137">System.String</span></span>

## <span data-ttu-id="21aed-138">輸出</span><span class="sxs-lookup"><span data-stu-id="21aed-138">OUTPUTS</span></span>

### <span data-ttu-id="21aed-139">System.void</span><span class="sxs-lookup"><span data-stu-id="21aed-139">System.Void</span></span>

## <span data-ttu-id="21aed-140">筆記</span><span class="sxs-lookup"><span data-stu-id="21aed-140">NOTES</span></span>
<span data-ttu-id="21aed-141">關鍵字： azure，azurerm，arm，資源，管理，管理員，資料，工廠</span><span class="sxs-lookup"><span data-stu-id="21aed-141">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="21aed-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="21aed-142">RELATED LINKS</span></span>

[<span data-ttu-id="21aed-143">AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="21aed-143">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="21aed-144">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="21aed-144">Set-AzDataFactoryV2</span></span>]()
