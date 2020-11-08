---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970720"
---
# <span data-ttu-id="e9ee4-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="e9ee4-101">Update-AzActionRule</span></span>

## <span data-ttu-id="e9ee4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e9ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="e9ee4-103">更新動作規則屬性。</span><span class="sxs-lookup"><span data-stu-id="e9ee4-103">Updates action rule properties.</span></span>

## <span data-ttu-id="e9ee4-104">句法</span><span class="sxs-lookup"><span data-stu-id="e9ee4-104">SYNTAX</span></span>

### <span data-ttu-id="e9ee4-105">ByNameSimplifiedPatch (預設) </span><span class="sxs-lookup"><span data-stu-id="e9ee4-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9ee4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e9ee4-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e9ee4-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e9ee4-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9ee4-108">說明</span><span class="sxs-lookup"><span data-stu-id="e9ee4-108">DESCRIPTION</span></span>
<span data-ttu-id="e9ee4-109">**更新-AzActionRule** Cmdlet 會更新動作規則屬性-狀態和標籤。</span><span class="sxs-lookup"><span data-stu-id="e9ee4-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="e9ee4-110">示例</span><span class="sxs-lookup"><span data-stu-id="e9ee4-110">EXAMPLES</span></span>

### <span data-ttu-id="e9ee4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="e9ee4-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="e9ee4-112">這個 Cmdlet 會停用動作規則。</span><span class="sxs-lookup"><span data-stu-id="e9ee4-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="e9ee4-113">參數</span><span class="sxs-lookup"><span data-stu-id="e9ee4-113">PARAMETERS</span></span>

### <span data-ttu-id="e9ee4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9ee4-114">-DefaultProfile</span></span>
<span data-ttu-id="e9ee4-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e9ee4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9ee4-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9ee4-116">-InputObject</span></span>
<span data-ttu-id="e9ee4-117">[動作規則] 資源</span><span class="sxs-lookup"><span data-stu-id="e9ee4-117">The action rule resource</span></span>

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

### <span data-ttu-id="e9ee4-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="e9ee4-118">-Name</span></span>
<span data-ttu-id="e9ee4-119">動作規則名稱</span><span class="sxs-lookup"><span data-stu-id="e9ee4-119">Action rule name</span></span>

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

### <span data-ttu-id="e9ee4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9ee4-120">-ResourceGroupName</span></span>
<span data-ttu-id="e9ee4-121">動作規則名稱</span><span class="sxs-lookup"><span data-stu-id="e9ee4-121">Action rule name</span></span>

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

### <span data-ttu-id="e9ee4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9ee4-122">-ResourceId</span></span>
<span data-ttu-id="e9ee4-123">行動規則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="e9ee4-123">The resource id of action rule</span></span>

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

### <span data-ttu-id="e9ee4-124">-狀態</span><span class="sxs-lookup"><span data-stu-id="e9ee4-124">-Status</span></span>
<span data-ttu-id="e9ee4-125">動作規則狀態</span><span class="sxs-lookup"><span data-stu-id="e9ee4-125">Action rule status</span></span>

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

### <span data-ttu-id="e9ee4-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="e9ee4-126">-Tag</span></span>
<span data-ttu-id="e9ee4-127">動作規則標記</span><span class="sxs-lookup"><span data-stu-id="e9ee4-127">Action rule tags</span></span>

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

### <span data-ttu-id="e9ee4-128">-確認</span><span class="sxs-lookup"><span data-stu-id="e9ee4-128">-Confirm</span></span>
<span data-ttu-id="e9ee4-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e9ee4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9ee4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9ee4-130">-WhatIf</span></span>
<span data-ttu-id="e9ee4-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e9ee4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9ee4-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e9ee4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9ee4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9ee4-133">CommonParameters</span></span>
<span data-ttu-id="e9ee4-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e9ee4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9ee4-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e9ee4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9ee4-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e9ee4-136">INPUTS</span></span>

### <span data-ttu-id="e9ee4-137">System.object</span><span class="sxs-lookup"><span data-stu-id="e9ee4-137">System.String</span></span>

### <span data-ttu-id="e9ee4-138">AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="e9ee4-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="e9ee4-139">輸出</span><span class="sxs-lookup"><span data-stu-id="e9ee4-139">OUTPUTS</span></span>

### <span data-ttu-id="e9ee4-140">AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="e9ee4-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="e9ee4-141">筆記</span><span class="sxs-lookup"><span data-stu-id="e9ee4-141">NOTES</span></span>

## <span data-ttu-id="e9ee4-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="e9ee4-142">RELATED LINKS</span></span>
