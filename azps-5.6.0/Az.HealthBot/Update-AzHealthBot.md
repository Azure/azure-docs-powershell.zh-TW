---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/update-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
ms.openlocfilehash: a0dc204bb6dc1a91031a87fd113c525f282f090e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917225"
---
# <span data-ttu-id="373bb-101">Update-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="373bb-101">Update-AzHealthBot</span></span>

## <span data-ttu-id="373bb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="373bb-102">SYNOPSIS</span></span>
<span data-ttu-id="373bb-103">修補 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="373bb-103">Patch a HealthBot.</span></span>

## <span data-ttu-id="373bb-104">語法</span><span class="sxs-lookup"><span data-stu-id="373bb-104">SYNTAX</span></span>

### <span data-ttu-id="373bb-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="373bb-105">UpdateExpanded (Default)</span></span>
```
Update-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="373bb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="373bb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzHealthBot -InputObject <IHealthBotIdentity> [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="373bb-107">描述</span><span class="sxs-lookup"><span data-stu-id="373bb-107">DESCRIPTION</span></span>
<span data-ttu-id="373bb-108">修補 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="373bb-108">Patch a HealthBot.</span></span>

## <span data-ttu-id="373bb-109">例子</span><span class="sxs-lookup"><span data-stu-id="373bb-109">EXAMPLES</span></span>

### <span data-ttu-id="373bb-110">範例 1：更新 HealthBot by Resourcegroupname 和 Name</span><span class="sxs-lookup"><span data-stu-id="373bb-110">Example 1: update HealthBot by Resourcegroupname and Name</span></span>
```powershell
PS C:\> update-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot -Sku S1

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="373bb-111">更新 HealthBot by Resourcegroupname 和 Name</span><span class="sxs-lookup"><span data-stu-id="373bb-111">update HealthBot by Resourcegroupname and Name</span></span>

### <span data-ttu-id="373bb-112">範例 2：更新 HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="373bb-112">Example 2: update HealthBot by InputObject</span></span>
```powershell
PS C:\> $getHealth = Get-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot
Update-AzHealthBot -InputObject $getHealth -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="373bb-113">更新 HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="373bb-113">update HealthBot by InputObject</span></span>

## <span data-ttu-id="373bb-114">參數</span><span class="sxs-lookup"><span data-stu-id="373bb-114">PARAMETERS</span></span>

### <span data-ttu-id="373bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="373bb-115">-DefaultProfile</span></span>
<span data-ttu-id="373bb-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="373bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="373bb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="373bb-117">-InputObject</span></span>
<span data-ttu-id="373bb-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="373bb-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="373bb-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="373bb-119">-Name</span></span>
<span data-ttu-id="373bb-120">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="373bb-120">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="373bb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="373bb-121">-ResourceGroupName</span></span>
<span data-ttu-id="373bb-122">使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="373bb-122">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="373bb-123">-SKU</span><span class="sxs-lookup"><span data-stu-id="373bb-123">-Sku</span></span>
<span data-ttu-id="373bb-124">HealthBot SKU 的名稱</span><span class="sxs-lookup"><span data-stu-id="373bb-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="373bb-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="373bb-125">-SubscriptionId</span></span>
<span data-ttu-id="373bb-126">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="373bb-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="373bb-127">-標記</span><span class="sxs-lookup"><span data-stu-id="373bb-127">-Tag</span></span>
<span data-ttu-id="373bb-128">HealthBot 的標記。</span><span class="sxs-lookup"><span data-stu-id="373bb-128">Tags for a HealthBot.</span></span>

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

### <span data-ttu-id="373bb-129">-確認</span><span class="sxs-lookup"><span data-stu-id="373bb-129">-Confirm</span></span>
<span data-ttu-id="373bb-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="373bb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="373bb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="373bb-131">-WhatIf</span></span>
<span data-ttu-id="373bb-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="373bb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="373bb-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="373bb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="373bb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="373bb-134">CommonParameters</span></span>
<span data-ttu-id="373bb-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="373bb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="373bb-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="373bb-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="373bb-137">輸入</span><span class="sxs-lookup"><span data-stu-id="373bb-137">INPUTS</span></span>

### <span data-ttu-id="373bb-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="373bb-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="373bb-139">輸出</span><span class="sxs-lookup"><span data-stu-id="373bb-139">OUTPUTS</span></span>

### <span data-ttu-id="373bb-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="373bb-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="373bb-141">筆記</span><span class="sxs-lookup"><span data-stu-id="373bb-141">NOTES</span></span>

<span data-ttu-id="373bb-142">別名</span><span class="sxs-lookup"><span data-stu-id="373bb-142">ALIASES</span></span>

<span data-ttu-id="373bb-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="373bb-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="373bb-144">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="373bb-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="373bb-145">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="373bb-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="373bb-146">INPUTOBJECT： <IHealthBotIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="373bb-146">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="373bb-147">`[BotName <String>]`：Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="373bb-147">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="373bb-148">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="373bb-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="373bb-149">`[ResourceGroupName <String>]`：使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="373bb-149">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="373bb-150">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="373bb-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="373bb-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="373bb-151">RELATED LINKS</span></span>

