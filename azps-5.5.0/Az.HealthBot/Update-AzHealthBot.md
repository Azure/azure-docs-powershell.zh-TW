---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/update-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
ms.openlocfilehash: b14ed0d682a6ba74eb557aae79a4fe151e952a73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139107"
---
# <span data-ttu-id="f9e6f-101">Update-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="f9e6f-101">Update-AzHealthBot</span></span>

## <span data-ttu-id="f9e6f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f9e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="f9e6f-103">修補 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-103">Patch a HealthBot.</span></span>

## <span data-ttu-id="f9e6f-104">句法</span><span class="sxs-lookup"><span data-stu-id="f9e6f-104">SYNTAX</span></span>

### <span data-ttu-id="f9e6f-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="f9e6f-105">UpdateExpanded (Default)</span></span>
```
Update-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f9e6f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="f9e6f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzHealthBot -InputObject <IHealthBotIdentity> [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f9e6f-107">說明</span><span class="sxs-lookup"><span data-stu-id="f9e6f-107">DESCRIPTION</span></span>
<span data-ttu-id="f9e6f-108">修補 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-108">Patch a HealthBot.</span></span>

## <span data-ttu-id="f9e6f-109">示例</span><span class="sxs-lookup"><span data-stu-id="f9e6f-109">EXAMPLES</span></span>

### <span data-ttu-id="f9e6f-110">範例1：依 Resourcegroupname 和 Name 更新 HealthBot</span><span class="sxs-lookup"><span data-stu-id="f9e6f-110">Example 1: update HealthBot by Resourcegroupname and Name</span></span>
```powershell
PS C:\> update-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot -Sku S1

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="f9e6f-111">依 Resourcegroupname 和 Name 更新 HealthBot</span><span class="sxs-lookup"><span data-stu-id="f9e6f-111">update HealthBot by Resourcegroupname and Name</span></span>

### <span data-ttu-id="f9e6f-112">範例2：由 InputObject 更新 HealthBot</span><span class="sxs-lookup"><span data-stu-id="f9e6f-112">Example 2: update HealthBot by InputObject</span></span>
```powershell
PS C:\> $getHealth = Get-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot
Update-AzHealthBot -InputObject $getHealth -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="f9e6f-113">以 InputObject 更新 HealthBot</span><span class="sxs-lookup"><span data-stu-id="f9e6f-113">update HealthBot by InputObject</span></span>

## <span data-ttu-id="f9e6f-114">參數</span><span class="sxs-lookup"><span data-stu-id="f9e6f-114">PARAMETERS</span></span>

### <span data-ttu-id="f9e6f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9e6f-115">-DefaultProfile</span></span>
<span data-ttu-id="f9e6f-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9e6f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9e6f-117">-InputObject</span></span>
<span data-ttu-id="f9e6f-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f9e6f-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f9e6f-119">-Name</span></span>
<span data-ttu-id="f9e6f-120">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="f9e6f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9e6f-121">-ResourceGroupName</span></span>
<span data-ttu-id="f9e6f-122">使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="f9e6f-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="f9e6f-123">-Sku</span></span>
<span data-ttu-id="f9e6f-124">HealthBot SKU 的名稱</span><span class="sxs-lookup"><span data-stu-id="f9e6f-124">The name of the HealthBot SKU</span></span>

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

### <span data-ttu-id="f9e6f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f9e6f-125">-SubscriptionId</span></span>
<span data-ttu-id="f9e6f-126">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f9e6f-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="f9e6f-127">-Tag</span></span>
<span data-ttu-id="f9e6f-128">HealthBot 的標記。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-128">Tags for a HealthBot.</span></span>

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

### <span data-ttu-id="f9e6f-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f9e6f-129">-Confirm</span></span>
<span data-ttu-id="f9e6f-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9e6f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9e6f-131">-WhatIf</span></span>
<span data-ttu-id="f9e6f-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9e6f-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9e6f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9e6f-134">CommonParameters</span></span>
<span data-ttu-id="f9e6f-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9e6f-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9e6f-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f9e6f-137">INPUTS</span></span>

### <span data-ttu-id="f9e6f-138">IHealthBotIdentity （HealthBot）的</span><span class="sxs-lookup"><span data-stu-id="f9e6f-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="f9e6f-139">輸出</span><span class="sxs-lookup"><span data-stu-id="f9e6f-139">OUTPUTS</span></span>

### <span data-ttu-id="f9e6f-140">IHealthBot （HealthBot）。 Api20201208。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="f9e6f-141">筆記</span><span class="sxs-lookup"><span data-stu-id="f9e6f-141">NOTES</span></span>

<span data-ttu-id="f9e6f-142">別名</span><span class="sxs-lookup"><span data-stu-id="f9e6f-142">ALIASES</span></span>

<span data-ttu-id="f9e6f-143">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="f9e6f-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f9e6f-144">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f9e6f-145">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f9e6f-146">INPUTOBJECT <IHealthBotIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="f9e6f-146">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f9e6f-147">`[BotName <String>]`： Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-147">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="f9e6f-148">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="f9e6f-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f9e6f-149">`[ResourceGroupName <String>]`：使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-149">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="f9e6f-150">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="f9e6f-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f9e6f-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="f9e6f-151">RELATED LINKS</span></span>

