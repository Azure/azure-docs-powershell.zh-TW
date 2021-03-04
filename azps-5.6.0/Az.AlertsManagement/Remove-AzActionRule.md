---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 7e34a37e0375c90fb5d36ce37c821c3b2c2fd69a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904158"
---
# <span data-ttu-id="395e9-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="395e9-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="395e9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="395e9-102">SYNOPSIS</span></span>
<span data-ttu-id="395e9-103">刪除動作規則</span><span class="sxs-lookup"><span data-stu-id="395e9-103">Deletes a action rule</span></span>

## <span data-ttu-id="395e9-104">語法</span><span class="sxs-lookup"><span data-stu-id="395e9-104">SYNTAX</span></span>

### <span data-ttu-id="395e9-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="395e9-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="395e9-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="395e9-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="395e9-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="395e9-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="395e9-108">描述</span><span class="sxs-lookup"><span data-stu-id="395e9-108">DESCRIPTION</span></span>
<span data-ttu-id="395e9-109">**Remove-AzActionRule** Cmdlet 會刪除動作規則。</span><span class="sxs-lookup"><span data-stu-id="395e9-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="395e9-110">例子</span><span class="sxs-lookup"><span data-stu-id="395e9-110">EXAMPLES</span></span>

### <span data-ttu-id="395e9-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="395e9-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="395e9-112">此 Cmdlet 會刪除資源群組 test-rg 中名稱為 ActionRuleName 的動作規則</span><span class="sxs-lookup"><span data-stu-id="395e9-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="395e9-113">參數</span><span class="sxs-lookup"><span data-stu-id="395e9-113">PARAMETERS</span></span>

### <span data-ttu-id="395e9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395e9-114">-DefaultProfile</span></span>
<span data-ttu-id="395e9-115">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="395e9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="395e9-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="395e9-116">-InputObject</span></span>
<span data-ttu-id="395e9-117">動作規則資源</span><span class="sxs-lookup"><span data-stu-id="395e9-117">The action rule resource</span></span>

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

### <span data-ttu-id="395e9-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="395e9-118">-Name</span></span>
<span data-ttu-id="395e9-119">動作規則的名稱</span><span class="sxs-lookup"><span data-stu-id="395e9-119">Name of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395e9-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="395e9-120">-PassThru</span></span>
<span data-ttu-id="395e9-121">PassThru 會傳回代表您處理之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="395e9-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="395e9-122">根據預設，此 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="395e9-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="395e9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="395e9-123">-ResourceGroupName</span></span>
<span data-ttu-id="395e9-124">資源組名</span><span class="sxs-lookup"><span data-stu-id="395e9-124">Resource Group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395e9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="395e9-125">-ResourceId</span></span>
<span data-ttu-id="395e9-126">依資源識別碼取得動作規則。</span><span class="sxs-lookup"><span data-stu-id="395e9-126">Get Action rule by resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395e9-127">-確認</span><span class="sxs-lookup"><span data-stu-id="395e9-127">-Confirm</span></span>
<span data-ttu-id="395e9-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="395e9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="395e9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="395e9-129">-WhatIf</span></span>
<span data-ttu-id="395e9-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="395e9-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="395e9-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="395e9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="395e9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395e9-132">CommonParameters</span></span>
<span data-ttu-id="395e9-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="395e9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395e9-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="395e9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395e9-135">輸入</span><span class="sxs-lookup"><span data-stu-id="395e9-135">INPUTS</span></span>

### <span data-ttu-id="395e9-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="395e9-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="395e9-137">輸出</span><span class="sxs-lookup"><span data-stu-id="395e9-137">OUTPUTS</span></span>

### <span data-ttu-id="395e9-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="395e9-138">System.Boolean</span></span>

## <span data-ttu-id="395e9-139">筆記</span><span class="sxs-lookup"><span data-stu-id="395e9-139">NOTES</span></span>

## <span data-ttu-id="395e9-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="395e9-140">RELATED LINKS</span></span>
