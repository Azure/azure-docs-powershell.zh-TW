---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagedApplication.md
ms.openlocfilehash: 30e3e7f7b6ace383a2c492f4dcc088f65dfea08b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914410"
---
# <span data-ttu-id="e93ba-101">New-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="e93ba-101">New-AzManagedApplication</span></span>

## <span data-ttu-id="e93ba-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e93ba-102">SYNOPSIS</span></span>
<span data-ttu-id="e93ba-103">建立 Azure 受管理的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e93ba-103">Creates an Azure managed application.</span></span>

## <span data-ttu-id="e93ba-104">語法</span><span class="sxs-lookup"><span data-stu-id="e93ba-104">SYNTAX</span></span>

```
New-AzManagedApplication -Name <String> -ResourceGroupName <String> -ManagedResourceGroupName <String>
 [-ManagedApplicationDefinitionId <String>] -Location <String> [-Parameter <String>] -Kind <ApplicationKind>
 [-Plan <Hashtable>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e93ba-105">描述</span><span class="sxs-lookup"><span data-stu-id="e93ba-105">DESCRIPTION</span></span>
<span data-ttu-id="e93ba-106">**New-AzManagedApplication** Cmdlet 會建立 Azure Managed 應用程式。</span><span class="sxs-lookup"><span data-stu-id="e93ba-106">The **New-AzManagedApplication** cmdlet creates an Azure Managed Application.</span></span>

## <span data-ttu-id="e93ba-107">例子</span><span class="sxs-lookup"><span data-stu-id="e93ba-107">EXAMPLES</span></span>

### <span data-ttu-id="e93ba-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="e93ba-108">Example 1</span></span>
```
PS C:\>New-AzManagedApplication -Name "myManagedApplication" -ResourceGroupName myRG -ManagedResourceGroupName myManagedRG -ManagedApplicationDefinitionId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Microsoft.Solutions/applicationDefinitions/myAppDef" -Location eastus2euap -Kind ServiceCatalog
```

<span data-ttu-id="e93ba-109">此命令會建立受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="e93ba-109">This command creates a managed application</span></span>

## <span data-ttu-id="e93ba-110">參數</span><span class="sxs-lookup"><span data-stu-id="e93ba-110">PARAMETERS</span></span>

### <span data-ttu-id="e93ba-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e93ba-111">-ApiVersion</span></span>
<span data-ttu-id="e93ba-112">設定時，表示要使用資源提供者 API 的版本。</span><span class="sxs-lookup"><span data-stu-id="e93ba-112">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e93ba-113">如果未指定，API 版本會自動判斷為最新可用。</span><span class="sxs-lookup"><span data-stu-id="e93ba-113">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e93ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e93ba-114">-DefaultProfile</span></span>
<span data-ttu-id="e93ba-115">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="e93ba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e93ba-116">-Kind</span><span class="sxs-lookup"><span data-stu-id="e93ba-116">-Kind</span></span>
<span data-ttu-id="e93ba-117">受管理的應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="e93ba-117">The managed application kind.</span></span>
<span data-ttu-id="e93ba-118">其中一個服務商場或 servicecatalog</span><span class="sxs-lookup"><span data-stu-id="e93ba-118">One of marketplace or servicecatalog</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Application.ApplicationKind
Parameter Sets: (All)
Aliases:
Accepted values: ServiceCatalog, MarketPlace

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e93ba-119">-位置</span><span class="sxs-lookup"><span data-stu-id="e93ba-119">-Location</span></span>
<span data-ttu-id="e93ba-120">資源位置。</span><span class="sxs-lookup"><span data-stu-id="e93ba-120">The resource location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e93ba-121">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e93ba-121">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="e93ba-122">受管理的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e93ba-122">The managed resource group name.</span></span>

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

### <span data-ttu-id="e93ba-123">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e93ba-123">-ManagedResourceGroupName</span></span>
<span data-ttu-id="e93ba-124">受管理的資源組名。</span><span class="sxs-lookup"><span data-stu-id="e93ba-124">The managed resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93ba-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="e93ba-125">-Name</span></span>
<span data-ttu-id="e93ba-126">受管理的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="e93ba-126">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93ba-127">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e93ba-127">-Parameter</span></span>
<span data-ttu-id="e93ba-128">受管理應用程式的 JSON 格式化參數字串。</span><span class="sxs-lookup"><span data-stu-id="e93ba-128">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="e93ba-129">這可以是檔案名或包含參數的 uri 路徑，或參數為字串。</span><span class="sxs-lookup"><span data-stu-id="e93ba-129">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="e93ba-130">-規劃</span><span class="sxs-lookup"><span data-stu-id="e93ba-130">-Plan</span></span>
<span data-ttu-id="e93ba-131">代表受管理應用程式計畫屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e93ba-131">A hash table which represents managed application plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e93ba-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="e93ba-132">-Pre</span></span>
<span data-ttu-id="e93ba-133">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="e93ba-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e93ba-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e93ba-134">-ResourceGroupName</span></span>
<span data-ttu-id="e93ba-135">資源組名。</span><span class="sxs-lookup"><span data-stu-id="e93ba-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93ba-136">-標記</span><span class="sxs-lookup"><span data-stu-id="e93ba-136">-Tag</span></span>
<span data-ttu-id="e93ba-137">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e93ba-137">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e93ba-138">-確認</span><span class="sxs-lookup"><span data-stu-id="e93ba-138">-Confirm</span></span>
<span data-ttu-id="e93ba-139">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="e93ba-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e93ba-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e93ba-140">-WhatIf</span></span>
<span data-ttu-id="e93ba-141">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e93ba-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e93ba-142">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e93ba-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e93ba-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e93ba-143">CommonParameters</span></span>
<span data-ttu-id="e93ba-144">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e93ba-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e93ba-145">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e93ba-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e93ba-146">輸入</span><span class="sxs-lookup"><span data-stu-id="e93ba-146">INPUTS</span></span>

### <span data-ttu-id="e93ba-147">System.String</span><span class="sxs-lookup"><span data-stu-id="e93ba-147">System.String</span></span>

### <span data-ttu-id="e93ba-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="e93ba-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e93ba-149">輸出</span><span class="sxs-lookup"><span data-stu-id="e93ba-149">OUTPUTS</span></span>

### <span data-ttu-id="e93ba-150">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e93ba-150">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e93ba-151">筆記</span><span class="sxs-lookup"><span data-stu-id="e93ba-151">NOTES</span></span>

## <span data-ttu-id="e93ba-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="e93ba-152">RELATED LINKS</span></span>
