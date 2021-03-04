---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: 330aca1a9d4cc9438bdf360d5aee4af914df6c7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916277"
---
# <span data-ttu-id="b6658-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="b6658-101">Update-AzBotService</span></span>

## <span data-ttu-id="b6658-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b6658-102">SYNOPSIS</span></span>
<span data-ttu-id="b6658-103">更新 Bot 服務</span><span class="sxs-lookup"><span data-stu-id="b6658-103">Updates a Bot Service</span></span>

## <span data-ttu-id="b6658-104">語法</span><span class="sxs-lookup"><span data-stu-id="b6658-104">SYNTAX</span></span>

### <span data-ttu-id="b6658-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="b6658-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b6658-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b6658-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b6658-107">描述</span><span class="sxs-lookup"><span data-stu-id="b6658-107">DESCRIPTION</span></span>
<span data-ttu-id="b6658-108">更新 Bot 服務</span><span class="sxs-lookup"><span data-stu-id="b6658-108">Updates a Bot Service</span></span>

## <span data-ttu-id="b6658-109">例子</span><span class="sxs-lookup"><span data-stu-id="b6658-109">EXAMPLES</span></span>

### <span data-ttu-id="b6658-110">範例 1：更新 Bot By Name and ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6658-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="b6658-111">按名稱和資源組名更新 Bot</span><span class="sxs-lookup"><span data-stu-id="b6658-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="b6658-112">範例 2：使用 InputObject 更新 Bot</span><span class="sxs-lookup"><span data-stu-id="b6658-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="b6658-113">使用 InputObject 更新 Bot</span><span class="sxs-lookup"><span data-stu-id="b6658-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="b6658-114">參數</span><span class="sxs-lookup"><span data-stu-id="b6658-114">PARAMETERS</span></span>

### <span data-ttu-id="b6658-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6658-115">-DefaultProfile</span></span>
<span data-ttu-id="b6658-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6658-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6658-117">-描述</span><span class="sxs-lookup"><span data-stu-id="b6658-117">-Description</span></span>
<span data-ttu-id="b6658-118">Bot 的描述</span><span class="sxs-lookup"><span data-stu-id="b6658-118">The description of the bot</span></span>

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

### <span data-ttu-id="b6658-119">-DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="b6658-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="b6658-120">應用程式深入資訊金鑰</span><span class="sxs-lookup"><span data-stu-id="b6658-120">The Application Insights key</span></span>

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

### <span data-ttu-id="b6658-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="b6658-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="b6658-122">應用程式深入資訊 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="b6658-122">The Application Insights Api Key</span></span>

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

### <span data-ttu-id="b6658-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="b6658-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="b6658-124">應用程式深入資訊應用程式識別碼</span><span class="sxs-lookup"><span data-stu-id="b6658-124">The Application Insights App Id</span></span>

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

### <span data-ttu-id="b6658-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b6658-125">-DisplayName</span></span>
<span data-ttu-id="b6658-126">Bot 的名稱</span><span class="sxs-lookup"><span data-stu-id="b6658-126">The Name of the bot</span></span>

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

### <span data-ttu-id="b6658-127">-端點</span><span class="sxs-lookup"><span data-stu-id="b6658-127">-Endpoint</span></span>
<span data-ttu-id="b6658-128">Bot 的端點</span><span class="sxs-lookup"><span data-stu-id="b6658-128">The bot's endpoint</span></span>

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

### <span data-ttu-id="b6658-129">-Etag</span><span class="sxs-lookup"><span data-stu-id="b6658-129">-Etag</span></span>
<span data-ttu-id="b6658-130">實體標記</span><span class="sxs-lookup"><span data-stu-id="b6658-130">Entity Tag</span></span>

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

### <span data-ttu-id="b6658-131">-IconUrl</span><span class="sxs-lookup"><span data-stu-id="b6658-131">-IconUrl</span></span>
<span data-ttu-id="b6658-132">Bot 的圖示 URL</span><span class="sxs-lookup"><span data-stu-id="b6658-132">The Icon Url of the bot</span></span>

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

### <span data-ttu-id="b6658-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6658-133">-InputObject</span></span>
<span data-ttu-id="b6658-134">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b6658-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b6658-135">-Kind</span><span class="sxs-lookup"><span data-stu-id="b6658-135">-Kind</span></span>
<span data-ttu-id="b6658-136">必填。</span><span class="sxs-lookup"><span data-stu-id="b6658-136">Required.</span></span>
<span data-ttu-id="b6658-137">獲取或設定資源的類型。</span><span class="sxs-lookup"><span data-stu-id="b6658-137">Gets or sets the Kind of the resource.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.Kind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6658-138">-位置</span><span class="sxs-lookup"><span data-stu-id="b6658-138">-Location</span></span>
<span data-ttu-id="b6658-139">指定資源的位置。</span><span class="sxs-lookup"><span data-stu-id="b6658-139">Specifies the location of the resource.</span></span>

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

### <span data-ttu-id="b6658-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="b6658-140">-LuisAppId</span></span>
<span data-ttu-id="b6658-141">LUIS 應用程式識別碼集合</span><span class="sxs-lookup"><span data-stu-id="b6658-141">Collection of LUIS App Ids</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6658-142">-LuisKey</span><span class="sxs-lookup"><span data-stu-id="b6658-142">-LuisKey</span></span>
<span data-ttu-id="b6658-143">LUIS 鍵</span><span class="sxs-lookup"><span data-stu-id="b6658-143">The LUIS Key</span></span>

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

### <span data-ttu-id="b6658-144">-MsaAppId</span><span class="sxs-lookup"><span data-stu-id="b6658-144">-MsaAppId</span></span>
<span data-ttu-id="b6658-145">Bot 的 Microsoft App Id</span><span class="sxs-lookup"><span data-stu-id="b6658-145">Microsoft App Id for the bot</span></span>

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

### <span data-ttu-id="b6658-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="b6658-146">-Name</span></span>
<span data-ttu-id="b6658-147">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6658-147">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="b6658-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6658-148">-ResourceGroupName</span></span>
<span data-ttu-id="b6658-149">使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="b6658-149">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="b6658-150">-SKUName</span><span class="sxs-lookup"><span data-stu-id="b6658-150">-SkuName</span></span>
<span data-ttu-id="b6658-151">SKU 名稱</span><span class="sxs-lookup"><span data-stu-id="b6658-151">The sku name</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6658-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b6658-152">-SubscriptionId</span></span>
<span data-ttu-id="b6658-153">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b6658-153">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b6658-154">-標記</span><span class="sxs-lookup"><span data-stu-id="b6658-154">-Tag</span></span>
<span data-ttu-id="b6658-155">包含定義為金鑰/值組的資源標記。</span><span class="sxs-lookup"><span data-stu-id="b6658-155">Contains resource tags defined as key/value pairs.</span></span>

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

### <span data-ttu-id="b6658-156">-確認</span><span class="sxs-lookup"><span data-stu-id="b6658-156">-Confirm</span></span>
<span data-ttu-id="b6658-157">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b6658-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6658-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6658-158">-WhatIf</span></span>
<span data-ttu-id="b6658-159">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b6658-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6658-160">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b6658-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6658-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6658-161">CommonParameters</span></span>
<span data-ttu-id="b6658-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b6658-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6658-163">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6658-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6658-164">輸入</span><span class="sxs-lookup"><span data-stu-id="b6658-164">INPUTS</span></span>

### <span data-ttu-id="b6658-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b6658-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="b6658-166">輸出</span><span class="sxs-lookup"><span data-stu-id="b6658-166">OUTPUTS</span></span>

### <span data-ttu-id="b6658-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="b6658-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="b6658-168">筆記</span><span class="sxs-lookup"><span data-stu-id="b6658-168">NOTES</span></span>

<span data-ttu-id="b6658-169">別名</span><span class="sxs-lookup"><span data-stu-id="b6658-169">ALIASES</span></span>

<span data-ttu-id="b6658-170">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b6658-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b6658-171">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b6658-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b6658-172">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b6658-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b6658-173">INPUTOBJECT： <IBotServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b6658-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b6658-174">`[ChannelName <ChannelName?>]`：通道資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6658-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="b6658-175">`[ConnectionName <String>]`：Bot 服務連接設定資源的名稱</span><span class="sxs-lookup"><span data-stu-id="b6658-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="b6658-176">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b6658-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b6658-177">`[ResourceGroupName <String>]`：使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="b6658-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="b6658-178">`[ResourceName <String>]`：Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b6658-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="b6658-179">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b6658-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="b6658-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6658-180">RELATED LINKS</span></span>

