---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maintenance.dll-Help.xml
Module Name: Az.Maintenance
online version: https://docs.microsoft.com/powershell/module/az.maintenance/remove-azconfigurationassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maintenance/Maintenance/help/Remove-AzConfigurationAssignment.md
ms.openlocfilehash: c2470d35802c07a7de0041cd68111adfa65646f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910477"
---
# <span data-ttu-id="2596a-101">Remove-AzConfigurationAssignment</span><span class="sxs-lookup"><span data-stu-id="2596a-101">Remove-AzConfigurationAssignment</span></span>

## <span data-ttu-id="2596a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2596a-102">SYNOPSIS</span></span>
<span data-ttu-id="2596a-103">取消註冊資源的組配置。</span><span class="sxs-lookup"><span data-stu-id="2596a-103">Unregister configuration for resource.</span></span>

## <span data-ttu-id="2596a-104">語法</span><span class="sxs-lookup"><span data-stu-id="2596a-104">SYNTAX</span></span>

```
Remove-AzConfigurationAssignment [-ResourceGroupName] <String> [-ProviderName] <String>
 [-ResourceParentType <String>] [-ResourceParentName <String>] [-ResourceType] <String>
 [-ResourceName] <String> -ConfigurationAssignmentName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2596a-105">描述</span><span class="sxs-lookup"><span data-stu-id="2596a-105">DESCRIPTION</span></span>
<span data-ttu-id="2596a-106">取消註冊資源的組配置。</span><span class="sxs-lookup"><span data-stu-id="2596a-106">Unregister configuration for resource.</span></span>

## <span data-ttu-id="2596a-107">例子</span><span class="sxs-lookup"><span data-stu-id="2596a-107">EXAMPLES</span></span>

### <span data-ttu-id="2596a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="2596a-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzConfigurationAssignment -ResourceGroupName smdtest$location -ResourceParentType hostGroups -ResourceParentName smddhg$location -ResourceType hosts -ResourceName smddh$location -ProviderName Microsoft.Compute -ConfigurationAssignmentName $maintenanceConfigurationName

Remove-AzConfigurationAssignment operation
This cmdlet will remove the specified resource.  Do you want to continue?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

<span data-ttu-id="2596a-109">取消註冊資源的組配置。</span><span class="sxs-lookup"><span data-stu-id="2596a-109">Unregister configuration for resource.</span></span>

## <span data-ttu-id="2596a-110">參數</span><span class="sxs-lookup"><span data-stu-id="2596a-110">PARAMETERS</span></span>

### <span data-ttu-id="2596a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2596a-111">-AsJob</span></span>
<span data-ttu-id="2596a-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2596a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2596a-113">-ConfigurationAssignmentName</span><span class="sxs-lookup"><span data-stu-id="2596a-113">-ConfigurationAssignmentName</span></span>
<span data-ttu-id="2596a-114">組組指派名稱。</span><span class="sxs-lookup"><span data-stu-id="2596a-114">The configuration assignment name.</span></span>

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

### <span data-ttu-id="2596a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2596a-115">-DefaultProfile</span></span>
<span data-ttu-id="2596a-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2596a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2596a-117">-強制</span><span class="sxs-lookup"><span data-stu-id="2596a-117">-Force</span></span>
<span data-ttu-id="2596a-118">強制移除而不確認。</span><span class="sxs-lookup"><span data-stu-id="2596a-118">Force remove without confirmation.</span></span>

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

### <span data-ttu-id="2596a-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2596a-119">-PassThru</span></span>
<span data-ttu-id="2596a-120">會返回移除作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="2596a-120">Returns the status of the Remove operation.</span></span> <span data-ttu-id="2596a-121">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="2596a-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2596a-122">-ProviderName</span><span class="sxs-lookup"><span data-stu-id="2596a-122">-ProviderName</span></span>
<span data-ttu-id="2596a-123">資源提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="2596a-123">The resource provider Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2596a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2596a-124">-ResourceGroupName</span></span>
<span data-ttu-id="2596a-125">資源組名。</span><span class="sxs-lookup"><span data-stu-id="2596a-125">The resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2596a-126">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2596a-126">-ResourceName</span></span>
<span data-ttu-id="2596a-127">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2596a-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2596a-128">-ResourceParentName</span><span class="sxs-lookup"><span data-stu-id="2596a-128">-ResourceParentName</span></span>
<span data-ttu-id="2596a-129">父資源名稱。</span><span class="sxs-lookup"><span data-stu-id="2596a-129">The parent resource name.</span></span>

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

### <span data-ttu-id="2596a-130">-ResourceParentType</span><span class="sxs-lookup"><span data-stu-id="2596a-130">-ResourceParentType</span></span>
<span data-ttu-id="2596a-131">父資源類型。</span><span class="sxs-lookup"><span data-stu-id="2596a-131">The parent resource type.</span></span>

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

### <span data-ttu-id="2596a-132">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2596a-132">-ResourceType</span></span>
<span data-ttu-id="2596a-133">資源類型。</span><span class="sxs-lookup"><span data-stu-id="2596a-133">The resource type.</span></span>

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

### <span data-ttu-id="2596a-134">-確認</span><span class="sxs-lookup"><span data-stu-id="2596a-134">-Confirm</span></span>
<span data-ttu-id="2596a-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="2596a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2596a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2596a-136">-WhatIf</span></span>
<span data-ttu-id="2596a-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2596a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2596a-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2596a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2596a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2596a-139">CommonParameters</span></span>
<span data-ttu-id="2596a-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2596a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2596a-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2596a-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2596a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="2596a-142">INPUTS</span></span>

### <span data-ttu-id="2596a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="2596a-143">System.String</span></span>

## <span data-ttu-id="2596a-144">輸出</span><span class="sxs-lookup"><span data-stu-id="2596a-144">OUTPUTS</span></span>

### <span data-ttu-id="2596a-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2596a-145">System.Boolean</span></span>

## <span data-ttu-id="2596a-146">筆記</span><span class="sxs-lookup"><span data-stu-id="2596a-146">NOTES</span></span>

## <span data-ttu-id="2596a-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="2596a-147">RELATED LINKS</span></span>
