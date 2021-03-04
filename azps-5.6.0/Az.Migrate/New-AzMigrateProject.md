---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 8b3a14c9e8416c1ffc9809d09d664b7809f53a1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909594"
---
# <span data-ttu-id="c28d1-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="c28d1-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="c28d1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c28d1-102">SYNOPSIS</span></span>
<span data-ttu-id="c28d1-103">建立新的遷移專案。</span><span class="sxs-lookup"><span data-stu-id="c28d1-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="c28d1-104">語法</span><span class="sxs-lookup"><span data-stu-id="c28d1-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c28d1-105">描述</span><span class="sxs-lookup"><span data-stu-id="c28d1-105">DESCRIPTION</span></span>
<span data-ttu-id="c28d1-106">建立新的遷移專案。</span><span class="sxs-lookup"><span data-stu-id="c28d1-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="c28d1-107">例子</span><span class="sxs-lookup"><span data-stu-id="c28d1-107">EXAMPLES</span></span>

### <span data-ttu-id="c28d1-108">範例 1：建立 (預設) </span><span class="sxs-lookup"><span data-stu-id="c28d1-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="c28d1-109">建立新遷移專案的方法。</span><span class="sxs-lookup"><span data-stu-id="c28d1-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="c28d1-110">參數</span><span class="sxs-lookup"><span data-stu-id="c28d1-110">PARAMETERS</span></span>

### <span data-ttu-id="c28d1-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="c28d1-111">-ETag</span></span>
<span data-ttu-id="c28d1-112">指定 V1 電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="c28d1-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="c28d1-113">-位置</span><span class="sxs-lookup"><span data-stu-id="c28d1-113">-Location</span></span>
<span data-ttu-id="c28d1-114">指定 V1 電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="c28d1-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="c28d1-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="c28d1-115">-Name</span></span>
<span data-ttu-id="c28d1-116">指定要遷移的專案名稱。</span><span class="sxs-lookup"><span data-stu-id="c28d1-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="c28d1-117">-屬性</span><span class="sxs-lookup"><span data-stu-id="c28d1-117">-Property</span></span>
<span data-ttu-id="c28d1-118">指定專案屬性。</span><span class="sxs-lookup"><span data-stu-id="c28d1-118">Specifies the project properties.</span></span>
<span data-ttu-id="c28d1-119">若要建構，請參閱 PROPERTY 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c28d1-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180901Preview.IMigrateProjectProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28d1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c28d1-120">-ResourceGroupName</span></span>
<span data-ttu-id="c28d1-121">指定資源組名。</span><span class="sxs-lookup"><span data-stu-id="c28d1-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="c28d1-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c28d1-122">-SubscriptionId</span></span>
<span data-ttu-id="c28d1-123">指定訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c28d1-123">Specifies the subscription id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c28d1-124">-確認</span><span class="sxs-lookup"><span data-stu-id="c28d1-124">-Confirm</span></span>
<span data-ttu-id="c28d1-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c28d1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c28d1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c28d1-126">-WhatIf</span></span>
<span data-ttu-id="c28d1-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c28d1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c28d1-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c28d1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c28d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c28d1-129">CommonParameters</span></span>
<span data-ttu-id="c28d1-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c28d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c28d1-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c28d1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c28d1-132">輸入</span><span class="sxs-lookup"><span data-stu-id="c28d1-132">INPUTS</span></span>

## <span data-ttu-id="c28d1-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c28d1-133">OUTPUTS</span></span>

## <span data-ttu-id="c28d1-134">筆記</span><span class="sxs-lookup"><span data-stu-id="c28d1-134">NOTES</span></span>

<span data-ttu-id="c28d1-135">別名</span><span class="sxs-lookup"><span data-stu-id="c28d1-135">ALIASES</span></span>

<span data-ttu-id="c28d1-136">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c28d1-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c28d1-137">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c28d1-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c28d1-138">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c28d1-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c28d1-139">屬性 <IMigrateProjectProperties> ：指定專案屬性。</span><span class="sxs-lookup"><span data-stu-id="c28d1-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="c28d1-140">`[ProvisioningState <ProvisioningState?>]`：部署要轉移專案的狀態。</span><span class="sxs-lookup"><span data-stu-id="c28d1-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="c28d1-141">`[RegisteredTool <String[]>]`：在遷移專案中，獲得或設定已登錄的工具清單。</span><span class="sxs-lookup"><span data-stu-id="c28d1-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="c28d1-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="c28d1-142">RELATED LINKS</span></span>

