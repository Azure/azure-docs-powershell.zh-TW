---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/get-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
ms.openlocfilehash: 305e65e95b876e3093f4a14590e8b2e111e44aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916590"
---
# <span data-ttu-id="5cf63-101">Get-AzBotService</span><span class="sxs-lookup"><span data-stu-id="5cf63-101">Get-AzBotService</span></span>

## <span data-ttu-id="5cf63-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5cf63-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf63-103">會返回參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="5cf63-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="5cf63-104">語法</span><span class="sxs-lookup"><span data-stu-id="5cf63-104">SYNTAX</span></span>

### <span data-ttu-id="5cf63-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="5cf63-105">List1 (Default)</span></span>
```
Get-AzBotService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5cf63-106">獲取</span><span class="sxs-lookup"><span data-stu-id="5cf63-106">Get</span></span>
```
Get-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5cf63-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5cf63-107">GetViaIdentity</span></span>
```
Get-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5cf63-108">清單</span><span class="sxs-lookup"><span data-stu-id="5cf63-108">List</span></span>
```
Get-AzBotService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5cf63-109">描述</span><span class="sxs-lookup"><span data-stu-id="5cf63-109">DESCRIPTION</span></span>
<span data-ttu-id="5cf63-110">會返回參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="5cf63-110">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="5cf63-111">例子</span><span class="sxs-lookup"><span data-stu-id="5cf63-111">EXAMPLES</span></span>

### <span data-ttu-id="5cf63-112">範例 1：取得所有 BotServices</span><span class="sxs-lookup"><span data-stu-id="5cf63-112">Example 1: Get all BotServices</span></span>
```powershell
PS C:\> Get-AzBotService

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="5cf63-113">取得所有 BotServices</span><span class="sxs-lookup"><span data-stu-id="5cf63-113">Get all BotServices</span></span>

### <span data-ttu-id="5cf63-114">範例 2：取得 BotService by ResourceGroupName 和 Name</span><span class="sxs-lookup"><span data-stu-id="5cf63-114">Example 2: Get the BotService by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot F0              Microsoft.BotService/botServices
```

<span data-ttu-id="5cf63-115">按 ResourceGroupName 和 Name 取得 BotService</span><span class="sxs-lookup"><span data-stu-id="5cf63-115">Get the BotService by ResourceGroupName and Name</span></span>

### <span data-ttu-id="5cf63-116">範例 3：使用 ResourceGroupName 取得所有 BotServices</span><span class="sxs-lookup"><span data-stu-id="5cf63-116">Example 3: Get all BotServices by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzBotService -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="5cf63-117">根據 ResourceGroupName 取得所有 BotServices</span><span class="sxs-lookup"><span data-stu-id="5cf63-117">Get all BotServices by ResourceGroupName</span></span>

### <span data-ttu-id="5cf63-118">範例 4：取得 BotService by inputObject</span><span class="sxs-lookup"><span data-stu-id="5cf63-118">Example 4: Get the BotService by inputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'
Get-AzBotService -InputObject $getAzbot

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="5cf63-119">根據 inputObject 取得 BotService</span><span class="sxs-lookup"><span data-stu-id="5cf63-119">Get the BotService by inputObject</span></span>

## <span data-ttu-id="5cf63-120">參數</span><span class="sxs-lookup"><span data-stu-id="5cf63-120">PARAMETERS</span></span>

### <span data-ttu-id="5cf63-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf63-121">-DefaultProfile</span></span>
<span data-ttu-id="5cf63-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5cf63-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cf63-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5cf63-123">-InputObject</span></span>
<span data-ttu-id="5cf63-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5cf63-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cf63-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="5cf63-125">-Name</span></span>
<span data-ttu-id="5cf63-126">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="5cf63-126">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf63-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cf63-127">-ResourceGroupName</span></span>
<span data-ttu-id="5cf63-128">使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="5cf63-128">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf63-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cf63-129">-SubscriptionId</span></span>
<span data-ttu-id="5cf63-130">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="5cf63-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cf63-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf63-131">CommonParameters</span></span>
<span data-ttu-id="5cf63-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5cf63-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf63-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cf63-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf63-134">輸入</span><span class="sxs-lookup"><span data-stu-id="5cf63-134">INPUTS</span></span>

### <span data-ttu-id="5cf63-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="5cf63-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="5cf63-136">輸出</span><span class="sxs-lookup"><span data-stu-id="5cf63-136">OUTPUTS</span></span>

### <span data-ttu-id="5cf63-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="5cf63-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="5cf63-138">筆記</span><span class="sxs-lookup"><span data-stu-id="5cf63-138">NOTES</span></span>

<span data-ttu-id="5cf63-139">別名</span><span class="sxs-lookup"><span data-stu-id="5cf63-139">ALIASES</span></span>

<span data-ttu-id="5cf63-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="5cf63-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5cf63-141">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="5cf63-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5cf63-142">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="5cf63-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5cf63-143">INPUTOBJECT： <IBotServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="5cf63-143">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5cf63-144">`[ChannelName <ChannelName?>]`：通道資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="5cf63-144">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="5cf63-145">`[ConnectionName <String>]`：Bot 服務連接設定資源的名稱</span><span class="sxs-lookup"><span data-stu-id="5cf63-145">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="5cf63-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="5cf63-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5cf63-147">`[ResourceGroupName <String>]`：使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="5cf63-147">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="5cf63-148">`[ResourceName <String>]`：Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="5cf63-148">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="5cf63-149">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="5cf63-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="5cf63-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="5cf63-150">RELATED LINKS</span></span>

