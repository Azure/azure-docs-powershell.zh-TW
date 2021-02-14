---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigrateproject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateProject.md
ms.openlocfilehash: 32c4799f574e94eecee1f7ebf810c2f27bc5eccf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140679"
---
# <span data-ttu-id="83210-101">New-AzMigrateProject</span><span class="sxs-lookup"><span data-stu-id="83210-101">New-AzMigrateProject</span></span>

## <span data-ttu-id="83210-102">摘要</span><span class="sxs-lookup"><span data-stu-id="83210-102">SYNOPSIS</span></span>
<span data-ttu-id="83210-103">建立新的 [遷移專案]。</span><span class="sxs-lookup"><span data-stu-id="83210-103">Creates a new Migrate project.</span></span>

## <span data-ttu-id="83210-104">句法</span><span class="sxs-lookup"><span data-stu-id="83210-104">SYNTAX</span></span>

```
New-AzMigrateProject -Location <String> -Name <String> -ResourceGroupName <String> [-ETag <String>]
 [-Property <IMigrateProjectProperties>] [-SubscriptionId <String>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83210-105">說明</span><span class="sxs-lookup"><span data-stu-id="83210-105">DESCRIPTION</span></span>
<span data-ttu-id="83210-106">建立新的 [遷移專案]。</span><span class="sxs-lookup"><span data-stu-id="83210-106">Creates a new Migrate project.</span></span>

## <span data-ttu-id="83210-107">示例</span><span class="sxs-lookup"><span data-stu-id="83210-107">EXAMPLES</span></span>

### <span data-ttu-id="83210-108">範例1：建立 (預設) </span><span class="sxs-lookup"><span data-stu-id="83210-108">Example 1: Create (Default)</span></span>
```powershell
PS C:\> New-AzMigrateProject -SubscriptionId xxx-xxx-xxx -ResourceGroupName kuchaturimpkocrg1 -Name kuchaturimpkocrg1pwshp14 -Location "centralus"

ETag Location  Name                     Type
---- --------  ----                     ----
     centralus kuchaturimpkocrg1pwshp14 Microsoft.Migrate/MigrateProjects

```

<span data-ttu-id="83210-109">方法來建立新的 [遷移專案]。</span><span class="sxs-lookup"><span data-stu-id="83210-109">Method to create a new migrate project.</span></span>

## <span data-ttu-id="83210-110">參數</span><span class="sxs-lookup"><span data-stu-id="83210-110">PARAMETERS</span></span>

### <span data-ttu-id="83210-111">-ETag</span><span class="sxs-lookup"><span data-stu-id="83210-111">-ETag</span></span>
<span data-ttu-id="83210-112">指定 VMware 電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="83210-112">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="83210-113">-位置</span><span class="sxs-lookup"><span data-stu-id="83210-113">-Location</span></span>
<span data-ttu-id="83210-114">指定 VMware 電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="83210-114">Specifies the VMware machine name.</span></span>

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

### <span data-ttu-id="83210-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="83210-115">-Name</span></span>
<span data-ttu-id="83210-116">指定 [遷移專案名稱]。</span><span class="sxs-lookup"><span data-stu-id="83210-116">Specifies the migrate project name.</span></span>

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

### <span data-ttu-id="83210-117">-屬性</span><span class="sxs-lookup"><span data-stu-id="83210-117">-Property</span></span>
<span data-ttu-id="83210-118">指定專案屬性。</span><span class="sxs-lookup"><span data-stu-id="83210-118">Specifies the project properties.</span></span>
<span data-ttu-id="83210-119">若要構造，請參閱屬性屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="83210-119">To construct, see NOTES section for PROPERTY properties and create a hash table.</span></span>

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

### <span data-ttu-id="83210-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83210-120">-ResourceGroupName</span></span>
<span data-ttu-id="83210-121">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="83210-121">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="83210-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83210-122">-SubscriptionId</span></span>
<span data-ttu-id="83210-123">指定訂閱 id。</span><span class="sxs-lookup"><span data-stu-id="83210-123">Specifies the subscription id.</span></span>

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

### <span data-ttu-id="83210-124">-確認</span><span class="sxs-lookup"><span data-stu-id="83210-124">-Confirm</span></span>
<span data-ttu-id="83210-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="83210-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83210-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83210-126">-WhatIf</span></span>
<span data-ttu-id="83210-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="83210-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83210-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="83210-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83210-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83210-129">CommonParameters</span></span>
<span data-ttu-id="83210-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="83210-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83210-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="83210-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83210-132">輸入</span><span class="sxs-lookup"><span data-stu-id="83210-132">INPUTS</span></span>

## <span data-ttu-id="83210-133">輸出</span><span class="sxs-lookup"><span data-stu-id="83210-133">OUTPUTS</span></span>

## <span data-ttu-id="83210-134">筆記</span><span class="sxs-lookup"><span data-stu-id="83210-134">NOTES</span></span>

<span data-ttu-id="83210-135">別名</span><span class="sxs-lookup"><span data-stu-id="83210-135">ALIASES</span></span>

<span data-ttu-id="83210-136">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="83210-136">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83210-137">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="83210-137">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83210-138">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="83210-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83210-139">屬性 <IMigrateProjectProperties> ：指定專案屬性。</span><span class="sxs-lookup"><span data-stu-id="83210-139">PROPERTY <IMigrateProjectProperties>: Specifies the project properties.</span></span>
  - <span data-ttu-id="83210-140">`[ProvisioningState <ProvisioningState?>]`： [遷移專案] 的預配狀態。</span><span class="sxs-lookup"><span data-stu-id="83210-140">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of the migrate project.</span></span>
  - <span data-ttu-id="83210-141">`[RegisteredTool <String[]>]`：取得或設定在 [遷移] 專案中註冊的工具清單。</span><span class="sxs-lookup"><span data-stu-id="83210-141">`[RegisteredTool <String[]>]`: Gets or sets the list of tools registered with the migrate project.</span></span>

## <span data-ttu-id="83210-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="83210-142">RELATED LINKS</span></span>

