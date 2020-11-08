---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/remove-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Remove-AzActionRule.md
ms.openlocfilehash: 4462434bcda1045afcc8478bbd9c4b7a1718d478
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127946"
---
# <span data-ttu-id="3e951-101">Remove-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="3e951-101">Remove-AzActionRule</span></span>

## <span data-ttu-id="3e951-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e951-102">SYNOPSIS</span></span>
<span data-ttu-id="3e951-103">刪除動作規則</span><span class="sxs-lookup"><span data-stu-id="3e951-103">Deletes a action rule</span></span>

## <span data-ttu-id="3e951-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e951-104">SYNTAX</span></span>

### <span data-ttu-id="3e951-105">ByName (預設) </span><span class="sxs-lookup"><span data-stu-id="3e951-105">ByName (Default)</span></span>
```
Remove-AzActionRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e951-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3e951-106">ByResourceId</span></span>
```
Remove-AzActionRule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e951-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3e951-107">ByInputObject</span></span>
```
Remove-AzActionRule -InputObject <PSActionRule> [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e951-108">說明</span><span class="sxs-lookup"><span data-stu-id="3e951-108">DESCRIPTION</span></span>
<span data-ttu-id="3e951-109">**AzActionRule** Cmdlet 會刪除動作規則。</span><span class="sxs-lookup"><span data-stu-id="3e951-109">**Remove-AzActionRule** cmdlet deletes a action rule.</span></span>

## <span data-ttu-id="3e951-110">示例</span><span class="sxs-lookup"><span data-stu-id="3e951-110">EXAMPLES</span></span>

### <span data-ttu-id="3e951-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3e951-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzActionRule -ResourceGroupName "test-rg" -Name "ActionRuleName"
```

<span data-ttu-id="3e951-112">這個 Cmdlet 會刪除 [資源群組測試-rg] 中名稱為 ActionRuleName 的動作規則</span><span class="sxs-lookup"><span data-stu-id="3e951-112">This cmdlet deletes the action rule with name ActionRuleName in resource group test-rg</span></span>

## <span data-ttu-id="3e951-113">參數</span><span class="sxs-lookup"><span data-stu-id="3e951-113">PARAMETERS</span></span>

### <span data-ttu-id="3e951-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e951-114">-DefaultProfile</span></span>
<span data-ttu-id="3e951-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e951-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e951-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e951-116">-InputObject</span></span>
<span data-ttu-id="3e951-117">[動作規則] 資源</span><span class="sxs-lookup"><span data-stu-id="3e951-117">The action rule resource</span></span>

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

### <span data-ttu-id="3e951-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e951-118">-Name</span></span>
<span data-ttu-id="3e951-119">行動規則的名稱</span><span class="sxs-lookup"><span data-stu-id="3e951-119">Name of action rule</span></span>

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

### <span data-ttu-id="3e951-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e951-120">-PassThru</span></span>
<span data-ttu-id="3e951-121">PassThru 會傳回代表您正在使用之專案的物件。</span><span class="sxs-lookup"><span data-stu-id="3e951-121">PassThru returns an object representing the item with which you are working.</span></span> <span data-ttu-id="3e951-122">根據預設，這個 Cmdlet 不會產生任何輸出。</span><span class="sxs-lookup"><span data-stu-id="3e951-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3e951-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e951-123">-ResourceGroupName</span></span>
<span data-ttu-id="3e951-124">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3e951-124">Resource Group name</span></span>

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

### <span data-ttu-id="3e951-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3e951-125">-ResourceId</span></span>
<span data-ttu-id="3e951-126">依資源識別碼取得動作規則。</span><span class="sxs-lookup"><span data-stu-id="3e951-126">Get Action rule by resource id.</span></span>

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

### <span data-ttu-id="3e951-127">-確認</span><span class="sxs-lookup"><span data-stu-id="3e951-127">-Confirm</span></span>
<span data-ttu-id="3e951-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3e951-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e951-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e951-129">-WhatIf</span></span>
<span data-ttu-id="3e951-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e951-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e951-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e951-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e951-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e951-132">CommonParameters</span></span>
<span data-ttu-id="3e951-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e951-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e951-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3e951-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e951-135">輸入</span><span class="sxs-lookup"><span data-stu-id="3e951-135">INPUTS</span></span>

### <span data-ttu-id="3e951-136">AlertsManagement. OutputModels. PSActionRule</span><span class="sxs-lookup"><span data-stu-id="3e951-136">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="3e951-137">輸出</span><span class="sxs-lookup"><span data-stu-id="3e951-137">OUTPUTS</span></span>

### <span data-ttu-id="3e951-138">System.object</span><span class="sxs-lookup"><span data-stu-id="3e951-138">System.Boolean</span></span>

## <span data-ttu-id="3e951-139">筆記</span><span class="sxs-lookup"><span data-stu-id="3e951-139">NOTES</span></span>

## <span data-ttu-id="3e951-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e951-140">RELATED LINKS</span></span>
