---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100141795"
---
# <span data-ttu-id="99894-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="99894-101">Update-AzActionRule</span></span>

## <span data-ttu-id="99894-102">摘要</span><span class="sxs-lookup"><span data-stu-id="99894-102">SYNOPSIS</span></span>
<span data-ttu-id="99894-103">更新動作規則屬性。</span><span class="sxs-lookup"><span data-stu-id="99894-103">Updates action rule properties.</span></span>

## <span data-ttu-id="99894-104">句法</span><span class="sxs-lookup"><span data-stu-id="99894-104">SYNTAX</span></span>

### <span data-ttu-id="99894-105">ByNameSimplifiedPatch (預設) </span><span class="sxs-lookup"><span data-stu-id="99894-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99894-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="99894-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99894-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="99894-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99894-108">說明</span><span class="sxs-lookup"><span data-stu-id="99894-108">DESCRIPTION</span></span>
<span data-ttu-id="99894-109">**更新-AzActionRule** Cmdlet 會更新動作規則屬性-狀態和標籤。</span><span class="sxs-lookup"><span data-stu-id="99894-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="99894-110">示例</span><span class="sxs-lookup"><span data-stu-id="99894-110">EXAMPLES</span></span>

### <span data-ttu-id="99894-111">範例1</span><span class="sxs-lookup"><span data-stu-id="99894-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="99894-112">這個 Cmdlet 會停用動作規則。</span><span class="sxs-lookup"><span data-stu-id="99894-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="99894-113">參數</span><span class="sxs-lookup"><span data-stu-id="99894-113">PARAMETERS</span></span>

### <span data-ttu-id="99894-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99894-114">-DefaultProfile</span></span>
<span data-ttu-id="99894-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="99894-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99894-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99894-116">-InputObject</span></span>
<span data-ttu-id="99894-117">[動作規則] 資源</span><span class="sxs-lookup"><span data-stu-id="99894-117">The action rule resource</span></span>

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

### <span data-ttu-id="99894-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="99894-118">-Name</span></span>
<span data-ttu-id="99894-119">動作規則名稱</span><span class="sxs-lookup"><span data-stu-id="99894-119">Action rule name</span></span>

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

### <span data-ttu-id="99894-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99894-120">-ResourceGroupName</span></span>
<span data-ttu-id="99894-121">動作規則名稱</span><span class="sxs-lookup"><span data-stu-id="99894-121">Action rule name</span></span>

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

### <span data-ttu-id="99894-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99894-122">-ResourceId</span></span>
<span data-ttu-id="99894-123">行動規則的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="99894-123">The resource id of action rule</span></span>

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

### <span data-ttu-id="99894-124">-狀態</span><span class="sxs-lookup"><span data-stu-id="99894-124">-Status</span></span>
<span data-ttu-id="99894-125">動作規則狀態</span><span class="sxs-lookup"><span data-stu-id="99894-125">Action rule status</span></span>

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

### <span data-ttu-id="99894-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="99894-126">-Tag</span></span>
<span data-ttu-id="99894-127">動作規則標記</span><span class="sxs-lookup"><span data-stu-id="99894-127">Action rule tags</span></span>

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

### <span data-ttu-id="99894-128">-確認</span><span class="sxs-lookup"><span data-stu-id="99894-128">-Confirm</span></span>
<span data-ttu-id="99894-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="99894-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99894-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99894-130">-WhatIf</span></span>
<span data-ttu-id="99894-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="99894-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99894-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="99894-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99894-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99894-133">CommonParameters</span></span>
<span data-ttu-id="99894-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="99894-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99894-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="99894-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99894-136">輸入</span><span class="sxs-lookup"><span data-stu-id="99894-136">INPUTS</span></span>

### <span data-ttu-id="99894-137">System.object</span><span class="sxs-lookup"><span data-stu-id="99894-137">System.String</span></span>

### <span data-ttu-id="99894-138">AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="99894-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="99894-139">輸出</span><span class="sxs-lookup"><span data-stu-id="99894-139">OUTPUTS</span></span>

### <span data-ttu-id="99894-140">AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="99894-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="99894-141">筆記</span><span class="sxs-lookup"><span data-stu-id="99894-141">NOTES</span></span>

## <span data-ttu-id="99894-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="99894-142">RELATED LINKS</span></span>
