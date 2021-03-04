---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/new-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
ms.openlocfilehash: b9c4e4cd55f81449497b0d397574c3eeec64d2d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917229"
---
# <span data-ttu-id="09097-101">New-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="09097-101">New-AzHealthBot</span></span>

## <span data-ttu-id="09097-102">簡介</span><span class="sxs-lookup"><span data-stu-id="09097-102">SYNOPSIS</span></span>
<span data-ttu-id="09097-103">建立新 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="09097-103">Create a new HealthBot.</span></span>

## <span data-ttu-id="09097-104">語法</span><span class="sxs-lookup"><span data-stu-id="09097-104">SYNTAX</span></span>

```
New-AzHealthBot -Name <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="09097-105">描述</span><span class="sxs-lookup"><span data-stu-id="09097-105">DESCRIPTION</span></span>
<span data-ttu-id="09097-106">建立新 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="09097-106">Create a new HealthBot.</span></span>

## <span data-ttu-id="09097-107">例子</span><span class="sxs-lookup"><span data-stu-id="09097-107">EXAMPLES</span></span>

### <span data-ttu-id="09097-108">範例 1：建立新 HealthBot</span><span class="sxs-lookup"><span data-stu-id="09097-108">Example 1: Create new HealthBot</span></span>
```powershell
PS C:\> New-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest -Location eastus -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/29 8:19:14       6db4d6bb-6649-4dc2-84b7-0b5c6894031e Application                  Microsoft.Heal…
```

<span data-ttu-id="09097-109">根據預設，建立新 HealthBot</span><span class="sxs-lookup"><span data-stu-id="09097-109">Create new HealthBot By default</span></span>

## <span data-ttu-id="09097-110">參數</span><span class="sxs-lookup"><span data-stu-id="09097-110">PARAMETERS</span></span>

### <span data-ttu-id="09097-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="09097-111">-AsJob</span></span>
<span data-ttu-id="09097-112">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="09097-112">Run the command as a job</span></span>

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

### <span data-ttu-id="09097-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09097-113">-DefaultProfile</span></span>
<span data-ttu-id="09097-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="09097-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09097-115">-位置</span><span class="sxs-lookup"><span data-stu-id="09097-115">-Location</span></span>
<span data-ttu-id="09097-116">資源所在地的地理位置</span><span class="sxs-lookup"><span data-stu-id="09097-116">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="09097-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="09097-117">-Name</span></span>
<span data-ttu-id="09097-118">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="09097-118">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09097-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="09097-119">-NoWait</span></span>
<span data-ttu-id="09097-120">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="09097-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="09097-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09097-121">-ResourceGroupName</span></span>
<span data-ttu-id="09097-122">使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="09097-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="09097-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="09097-123">-Sku</span></span>
<span data-ttu-id="09097-124">HealthBot SKU 的名稱</span><span class="sxs-lookup"><span data-stu-id="09097-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09097-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="09097-125">-SubscriptionId</span></span>
<span data-ttu-id="09097-126">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="09097-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="09097-127">-標記</span><span class="sxs-lookup"><span data-stu-id="09097-127">-Tag</span></span>
<span data-ttu-id="09097-128">資源標記。</span><span class="sxs-lookup"><span data-stu-id="09097-128">Resource tags.</span></span>

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

### <span data-ttu-id="09097-129">-確認</span><span class="sxs-lookup"><span data-stu-id="09097-129">-Confirm</span></span>
<span data-ttu-id="09097-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="09097-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09097-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09097-131">-WhatIf</span></span>
<span data-ttu-id="09097-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="09097-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09097-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="09097-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09097-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09097-134">CommonParameters</span></span>
<span data-ttu-id="09097-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="09097-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09097-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09097-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09097-137">輸入</span><span class="sxs-lookup"><span data-stu-id="09097-137">INPUTS</span></span>

## <span data-ttu-id="09097-138">輸出</span><span class="sxs-lookup"><span data-stu-id="09097-138">OUTPUTS</span></span>

### <span data-ttu-id="09097-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="09097-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="09097-140">筆記</span><span class="sxs-lookup"><span data-stu-id="09097-140">NOTES</span></span>

<span data-ttu-id="09097-141">別名</span><span class="sxs-lookup"><span data-stu-id="09097-141">ALIASES</span></span>

## <span data-ttu-id="09097-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="09097-142">RELATED LINKS</span></span>

