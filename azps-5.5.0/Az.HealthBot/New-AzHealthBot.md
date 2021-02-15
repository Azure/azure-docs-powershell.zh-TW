---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/new-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/New-AzHealthBot.md
ms.openlocfilehash: dc39a7324f89e0a45efd4b631fb24a2e000d5e72
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129303"
---
# <span data-ttu-id="075f3-101">New-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="075f3-101">New-AzHealthBot</span></span>

## <span data-ttu-id="075f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="075f3-102">SYNOPSIS</span></span>
<span data-ttu-id="075f3-103">建立新的 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="075f3-103">Create a new HealthBot.</span></span>

## <span data-ttu-id="075f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="075f3-104">SYNTAX</span></span>

```
New-AzHealthBot -Name <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="075f3-105">說明</span><span class="sxs-lookup"><span data-stu-id="075f3-105">DESCRIPTION</span></span>
<span data-ttu-id="075f3-106">建立新的 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="075f3-106">Create a new HealthBot.</span></span>

## <span data-ttu-id="075f3-107">示例</span><span class="sxs-lookup"><span data-stu-id="075f3-107">EXAMPLES</span></span>

### <span data-ttu-id="075f3-108">範例1：建立新的 HealthBot</span><span class="sxs-lookup"><span data-stu-id="075f3-108">Example 1: Create new HealthBot</span></span>
```powershell
PS C:\> New-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest -Location eastus -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/29 8:19:14       6db4d6bb-6649-4dc2-84b7-0b5c6894031e Application                  Microsoft.Heal…
```

<span data-ttu-id="075f3-109">預設建立新的 HealthBot</span><span class="sxs-lookup"><span data-stu-id="075f3-109">Create new HealthBot By default</span></span>

## <span data-ttu-id="075f3-110">參數</span><span class="sxs-lookup"><span data-stu-id="075f3-110">PARAMETERS</span></span>

### <span data-ttu-id="075f3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="075f3-111">-AsJob</span></span>
<span data-ttu-id="075f3-112">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="075f3-112">Run the command as a job</span></span>

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

### <span data-ttu-id="075f3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="075f3-113">-DefaultProfile</span></span>
<span data-ttu-id="075f3-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="075f3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="075f3-115">-位置</span><span class="sxs-lookup"><span data-stu-id="075f3-115">-Location</span></span>
<span data-ttu-id="075f3-116">資源所在的地理位置</span><span class="sxs-lookup"><span data-stu-id="075f3-116">The geo-location where the resource lives</span></span>

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

### <span data-ttu-id="075f3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="075f3-117">-Name</span></span>
<span data-ttu-id="075f3-118">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="075f3-118">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="075f3-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="075f3-119">-NoWait</span></span>
<span data-ttu-id="075f3-120">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="075f3-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="075f3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="075f3-121">-ResourceGroupName</span></span>
<span data-ttu-id="075f3-122">使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="075f3-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="075f3-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="075f3-123">-Sku</span></span>
<span data-ttu-id="075f3-124">HealthBot SKU 的名稱</span><span class="sxs-lookup"><span data-stu-id="075f3-124">The name of the HealthBot SKU</span></span>

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

### <span data-ttu-id="075f3-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="075f3-125">-SubscriptionId</span></span>
<span data-ttu-id="075f3-126">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="075f3-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="075f3-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="075f3-127">-Tag</span></span>
<span data-ttu-id="075f3-128">資源標記。</span><span class="sxs-lookup"><span data-stu-id="075f3-128">Resource tags.</span></span>

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

### <span data-ttu-id="075f3-129">-確認</span><span class="sxs-lookup"><span data-stu-id="075f3-129">-Confirm</span></span>
<span data-ttu-id="075f3-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="075f3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="075f3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="075f3-131">-WhatIf</span></span>
<span data-ttu-id="075f3-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="075f3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="075f3-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="075f3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="075f3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="075f3-134">CommonParameters</span></span>
<span data-ttu-id="075f3-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="075f3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="075f3-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="075f3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="075f3-137">輸入</span><span class="sxs-lookup"><span data-stu-id="075f3-137">INPUTS</span></span>

## <span data-ttu-id="075f3-138">輸出</span><span class="sxs-lookup"><span data-stu-id="075f3-138">OUTPUTS</span></span>

### <span data-ttu-id="075f3-139">IHealthBot （HealthBot）。 Api20201208。</span><span class="sxs-lookup"><span data-stu-id="075f3-139">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="075f3-140">筆記</span><span class="sxs-lookup"><span data-stu-id="075f3-140">NOTES</span></span>

<span data-ttu-id="075f3-141">別名</span><span class="sxs-lookup"><span data-stu-id="075f3-141">ALIASES</span></span>

## <span data-ttu-id="075f3-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="075f3-142">RELATED LINKS</span></span>

