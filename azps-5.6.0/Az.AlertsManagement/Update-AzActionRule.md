---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 7dcbf947975719a30282037d592469a986990d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912509"
---
# <span data-ttu-id="6f46a-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="6f46a-101">Update-AzActionRule</span></span>

## <span data-ttu-id="6f46a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6f46a-102">SYNOPSIS</span></span>
<span data-ttu-id="6f46a-103">更新動作規則屬性。</span><span class="sxs-lookup"><span data-stu-id="6f46a-103">Updates action rule properties.</span></span>

## <span data-ttu-id="6f46a-104">語法</span><span class="sxs-lookup"><span data-stu-id="6f46a-104">SYNTAX</span></span>

### <span data-ttu-id="6f46a-105">ByNameSifiedPatch (預設) </span><span class="sxs-lookup"><span data-stu-id="6f46a-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f46a-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6f46a-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f46a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6f46a-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f46a-108">描述</span><span class="sxs-lookup"><span data-stu-id="6f46a-108">DESCRIPTION</span></span>
<span data-ttu-id="6f46a-109">**Update-AzActionRule** Cmdlet 會更新動作規則屬性 - 狀態和標籤。</span><span class="sxs-lookup"><span data-stu-id="6f46a-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="6f46a-110">例子</span><span class="sxs-lookup"><span data-stu-id="6f46a-110">EXAMPLES</span></span>

### <span data-ttu-id="6f46a-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="6f46a-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="6f46a-112">此 Cmdlet 會停用動作規則。</span><span class="sxs-lookup"><span data-stu-id="6f46a-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="6f46a-113">參數</span><span class="sxs-lookup"><span data-stu-id="6f46a-113">PARAMETERS</span></span>

### <span data-ttu-id="6f46a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f46a-114">-DefaultProfile</span></span>
<span data-ttu-id="6f46a-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6f46a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f46a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f46a-116">-InputObject</span></span>
<span data-ttu-id="6f46a-117">動作規則資源</span><span class="sxs-lookup"><span data-stu-id="6f46a-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f46a-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="6f46a-118">-Name</span></span>
<span data-ttu-id="6f46a-119">動作規則名稱</span><span class="sxs-lookup"><span data-stu-id="6f46a-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f46a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f46a-120">-ResourceGroupName</span></span>
<span data-ttu-id="6f46a-121">動作規則名稱</span><span class="sxs-lookup"><span data-stu-id="6f46a-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f46a-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f46a-122">-ResourceId</span></span>
<span data-ttu-id="6f46a-123">動作規則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="6f46a-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6f46a-124">-狀態</span><span class="sxs-lookup"><span data-stu-id="6f46a-124">-Status</span></span>
<span data-ttu-id="6f46a-125">動作規則狀態</span><span class="sxs-lookup"><span data-stu-id="6f46a-125">Action rule status</span></span>

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

### <span data-ttu-id="6f46a-126">-標記</span><span class="sxs-lookup"><span data-stu-id="6f46a-126">-Tag</span></span>
<span data-ttu-id="6f46a-127">動作規則標記</span><span class="sxs-lookup"><span data-stu-id="6f46a-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f46a-128">-確認</span><span class="sxs-lookup"><span data-stu-id="6f46a-128">-Confirm</span></span>
<span data-ttu-id="6f46a-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6f46a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f46a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f46a-130">-WhatIf</span></span>
<span data-ttu-id="6f46a-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6f46a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f46a-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6f46a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f46a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f46a-133">CommonParameters</span></span>
<span data-ttu-id="6f46a-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6f46a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f46a-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6f46a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f46a-136">輸入</span><span class="sxs-lookup"><span data-stu-id="6f46a-136">INPUTS</span></span>

### <span data-ttu-id="6f46a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6f46a-137">System.String</span></span>

### <span data-ttu-id="6f46a-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="6f46a-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="6f46a-139">輸出</span><span class="sxs-lookup"><span data-stu-id="6f46a-139">OUTPUTS</span></span>

### <span data-ttu-id="6f46a-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="6f46a-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="6f46a-141">筆記</span><span class="sxs-lookup"><span data-stu-id="6f46a-141">NOTES</span></span>

## <span data-ttu-id="6f46a-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="6f46a-142">RELATED LINKS</span></span>
