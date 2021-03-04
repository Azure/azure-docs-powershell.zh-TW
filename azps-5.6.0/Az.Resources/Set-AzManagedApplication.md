---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azmanagedapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzManagedApplication.md
ms.openlocfilehash: a2acea388b34b23d4977fa65ae6e6e6d4702525b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908766"
---
# <span data-ttu-id="f9c3e-101">Set-AzManagedApplication</span><span class="sxs-lookup"><span data-stu-id="f9c3e-101">Set-AzManagedApplication</span></span>

## <span data-ttu-id="f9c3e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f9c3e-102">SYNOPSIS</span></span>
<span data-ttu-id="f9c3e-103">更新受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="f9c3e-103">Updates managed application</span></span>

## <span data-ttu-id="f9c3e-104">語法</span><span class="sxs-lookup"><span data-stu-id="f9c3e-104">SYNTAX</span></span>

### <span data-ttu-id="f9c3e-105">SetByNameAndResourceGroup (預設) </span><span class="sxs-lookup"><span data-stu-id="f9c3e-105">SetByNameAndResourceGroup (Default)</span></span>
```
Set-AzManagedApplication -Name <String> -ResourceGroupName <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9c3e-106">SetById</span><span class="sxs-lookup"><span data-stu-id="f9c3e-106">SetById</span></span>
```
Set-AzManagedApplication -Id <String> [-ManagedResourceGroupName <String>]
 [-ManagedApplicationDefinitionId <String>] [-Parameter <String>] [-Kind <String>] [-Plan <Hashtable>]
 [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9c3e-107">描述</span><span class="sxs-lookup"><span data-stu-id="f9c3e-107">DESCRIPTION</span></span>
<span data-ttu-id="f9c3e-108">**Set-AzManagedApplication** Cmdlet 會更新受管理的應用程式</span><span class="sxs-lookup"><span data-stu-id="f9c3e-108">The **Set-AzManagedApplication** cmdlet updates managed applications</span></span>

## <span data-ttu-id="f9c3e-109">例子</span><span class="sxs-lookup"><span data-stu-id="f9c3e-109">EXAMPLES</span></span>

### <span data-ttu-id="f9c3e-110">範例 1：更新受管理的應用程式定義描述</span><span class="sxs-lookup"><span data-stu-id="f9c3e-110">Example 1: Update managed application definition description</span></span>
```
PS C:\>Set-AzManagedApplication -ResourceId "/subscriptions/mySubId/resourcegroups/myRG/Microsoft.Solutions/applications/myApp" -Description "Updated description here"
```

<span data-ttu-id="f9c3e-111">此命令會更新受管理的應用程式描述</span><span class="sxs-lookup"><span data-stu-id="f9c3e-111">This command updates the managed application description</span></span>

## <span data-ttu-id="f9c3e-112">參數</span><span class="sxs-lookup"><span data-stu-id="f9c3e-112">PARAMETERS</span></span>

### <span data-ttu-id="f9c3e-113">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f9c3e-113">-ApiVersion</span></span>
<span data-ttu-id="f9c3e-114">設定時，表示要使用資源提供者 API 的版本。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-114">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="f9c3e-115">如果未指定，API 版本會自動判斷為最新可用。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-115">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="f9c3e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9c3e-116">-DefaultProfile</span></span>
<span data-ttu-id="f9c3e-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9c3e-118">-Id</span><span class="sxs-lookup"><span data-stu-id="f9c3e-118">-Id</span></span>
<span data-ttu-id="f9c3e-119">完整受管理的應用程式識別碼，包括訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-119">The fully qualified managed application Id, including the subscription.</span></span> <span data-ttu-id="f9c3e-120">例如/subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9c3e-120">e.g. /subscriptions/{subscriptionId}/resourcegroups/{resourceGroupName</span></span>

```yaml
Type: System.String
Parameter Sets: SetById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9c3e-121">-Kind</span><span class="sxs-lookup"><span data-stu-id="f9c3e-121">-Kind</span></span>
<span data-ttu-id="f9c3e-122">受管理的應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-122">The managed application kind.</span></span>
<span data-ttu-id="f9c3e-123">其中一個服務商場或 servicecatalog</span><span class="sxs-lookup"><span data-stu-id="f9c3e-123">One of marketplace or servicecatalog</span></span>

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

### <span data-ttu-id="f9c3e-124">-ManagedApplicationDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f9c3e-124">-ManagedApplicationDefinitionId</span></span>
<span data-ttu-id="f9c3e-125">受管理的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-125">The managed resource group name.</span></span>

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

### <span data-ttu-id="f9c3e-126">-ManagedResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9c3e-126">-ManagedResourceGroupName</span></span>
<span data-ttu-id="f9c3e-127">受管理的資源組名。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-127">The managed resource group name.</span></span>

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

### <span data-ttu-id="f9c3e-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9c3e-128">-Name</span></span>
<span data-ttu-id="f9c3e-129">受管理的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-129">The managed application name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9c3e-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f9c3e-130">-Parameter</span></span>
<span data-ttu-id="f9c3e-131">受管理應用程式的 JSON 格式化參數字串。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-131">The JSON formatted string of parameters for managed application.</span></span>
<span data-ttu-id="f9c3e-132">這可以是檔案名或包含參數的 uri 路徑，或參數為字串。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-132">This can either be a path to a file name or uri containing the parameters, or the parameters as string.</span></span>

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

### <span data-ttu-id="f9c3e-133">-規劃</span><span class="sxs-lookup"><span data-stu-id="f9c3e-133">-Plan</span></span>
<span data-ttu-id="f9c3e-134">代表受管理應用程式計畫屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-134">A hash table which represents managed application plan properties.</span></span>

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

### <span data-ttu-id="f9c3e-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="f9c3e-135">-Pre</span></span>
<span data-ttu-id="f9c3e-136">設定之後，表示當系統自動決定要使用哪個版本時，Cmdlet 應該使用測試版 API 版本。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-136">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f9c3e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9c3e-137">-ResourceGroupName</span></span>
<span data-ttu-id="f9c3e-138">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-138">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9c3e-139">-標記</span><span class="sxs-lookup"><span data-stu-id="f9c3e-139">-Tag</span></span>
<span data-ttu-id="f9c3e-140">代表資源標記的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-140">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="f9c3e-141">-確認</span><span class="sxs-lookup"><span data-stu-id="f9c3e-141">-Confirm</span></span>
<span data-ttu-id="f9c3e-142">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9c3e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9c3e-143">-WhatIf</span></span>
<span data-ttu-id="f9c3e-144">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9c3e-145">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9c3e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9c3e-146">CommonParameters</span></span>
<span data-ttu-id="f9c3e-147">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f9c3e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9c3e-148">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f9c3e-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9c3e-149">輸入</span><span class="sxs-lookup"><span data-stu-id="f9c3e-149">INPUTS</span></span>

### <span data-ttu-id="f9c3e-150">System.String</span><span class="sxs-lookup"><span data-stu-id="f9c3e-150">System.String</span></span>

### <span data-ttu-id="f9c3e-151">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f9c3e-151">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f9c3e-152">輸出</span><span class="sxs-lookup"><span data-stu-id="f9c3e-152">OUTPUTS</span></span>

### <span data-ttu-id="f9c3e-153">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f9c3e-153">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f9c3e-154">筆記</span><span class="sxs-lookup"><span data-stu-id="f9c3e-154">NOTES</span></span>

## <span data-ttu-id="f9c3e-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9c3e-155">RELATED LINKS</span></span>
