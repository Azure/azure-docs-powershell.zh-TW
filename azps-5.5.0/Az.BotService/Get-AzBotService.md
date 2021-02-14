---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/get-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
ms.openlocfilehash: 4324c1e78ce56cc4b56455eaaff266b52c1d87d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100129967"
---
# <span data-ttu-id="57398-101">Get-AzBotService</span><span class="sxs-lookup"><span data-stu-id="57398-101">Get-AzBotService</span></span>

## <span data-ttu-id="57398-102">摘要</span><span class="sxs-lookup"><span data-stu-id="57398-102">SYNOPSIS</span></span>
<span data-ttu-id="57398-103">傳回由參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="57398-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="57398-104">句法</span><span class="sxs-lookup"><span data-stu-id="57398-104">SYNTAX</span></span>

### <span data-ttu-id="57398-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="57398-105">List1 (Default)</span></span>
```
Get-AzBotService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57398-106">獲取</span><span class="sxs-lookup"><span data-stu-id="57398-106">Get</span></span>
```
Get-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57398-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57398-107">GetViaIdentity</span></span>
```
Get-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57398-108">清單</span><span class="sxs-lookup"><span data-stu-id="57398-108">List</span></span>
```
Get-AzBotService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="57398-109">說明</span><span class="sxs-lookup"><span data-stu-id="57398-109">DESCRIPTION</span></span>
<span data-ttu-id="57398-110">傳回由參數指定的 BotService。</span><span class="sxs-lookup"><span data-stu-id="57398-110">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="57398-111">示例</span><span class="sxs-lookup"><span data-stu-id="57398-111">EXAMPLES</span></span>

### <span data-ttu-id="57398-112">範例1：取得所有 BotServices</span><span class="sxs-lookup"><span data-stu-id="57398-112">Example 1: Get all BotServices</span></span>
```powershell
PS C:\> Get-AzBotService

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="57398-113">取得所有 BotServices</span><span class="sxs-lookup"><span data-stu-id="57398-113">Get all BotServices</span></span>

### <span data-ttu-id="57398-114">範例2：透過 ResourceGroupName 和 Name 取得 BotService</span><span class="sxs-lookup"><span data-stu-id="57398-114">Example 2: Get the BotService by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot F0              Microsoft.BotService/botServices
```

<span data-ttu-id="57398-115">透過 ResourceGroupName 和名稱取得 BotService</span><span class="sxs-lookup"><span data-stu-id="57398-115">Get the BotService by ResourceGroupName and Name</span></span>

### <span data-ttu-id="57398-116">範例3：透過 ResourceGroupName 取得所有 BotServices</span><span class="sxs-lookup"><span data-stu-id="57398-116">Example 3: Get all BotServices by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzBotService -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="57398-117">透過 ResourceGroupName 取得所有 BotServices</span><span class="sxs-lookup"><span data-stu-id="57398-117">Get all BotServices by ResourceGroupName</span></span>

### <span data-ttu-id="57398-118">範例4：透過 inputObject 取得 BotService</span><span class="sxs-lookup"><span data-stu-id="57398-118">Example 4: Get the BotService by inputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'
Get-AzBotService -InputObject $getAzbot

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="57398-119">透過 inputObject 取得 BotService</span><span class="sxs-lookup"><span data-stu-id="57398-119">Get the BotService by inputObject</span></span>

## <span data-ttu-id="57398-120">參數</span><span class="sxs-lookup"><span data-stu-id="57398-120">PARAMETERS</span></span>

### <span data-ttu-id="57398-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57398-121">-DefaultProfile</span></span>
<span data-ttu-id="57398-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="57398-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57398-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57398-123">-InputObject</span></span>
<span data-ttu-id="57398-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="57398-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="57398-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="57398-125">-Name</span></span>
<span data-ttu-id="57398-126">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="57398-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="57398-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57398-127">-ResourceGroupName</span></span>
<span data-ttu-id="57398-128">使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="57398-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="57398-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57398-129">-SubscriptionId</span></span>
<span data-ttu-id="57398-130">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="57398-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="57398-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57398-131">CommonParameters</span></span>
<span data-ttu-id="57398-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="57398-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57398-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="57398-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57398-134">輸入</span><span class="sxs-lookup"><span data-stu-id="57398-134">INPUTS</span></span>

### <span data-ttu-id="57398-135">IBotServiceIdentity （BotService）的</span><span class="sxs-lookup"><span data-stu-id="57398-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="57398-136">輸出</span><span class="sxs-lookup"><span data-stu-id="57398-136">OUTPUTS</span></span>

### <span data-ttu-id="57398-137">IBot （BotService）。 Api20180712。</span><span class="sxs-lookup"><span data-stu-id="57398-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="57398-138">筆記</span><span class="sxs-lookup"><span data-stu-id="57398-138">NOTES</span></span>

<span data-ttu-id="57398-139">別名</span><span class="sxs-lookup"><span data-stu-id="57398-139">ALIASES</span></span>

<span data-ttu-id="57398-140">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="57398-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="57398-141">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="57398-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57398-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="57398-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="57398-143">INPUTOBJECT <IBotServiceIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="57398-143">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57398-144">`[ChannelName <ChannelName?>]`：頻道資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="57398-144">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="57398-145">`[ConnectionName <String>]`： Bot 服務連線設定資源的名稱</span><span class="sxs-lookup"><span data-stu-id="57398-145">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="57398-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="57398-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57398-147">`[ResourceGroupName <String>]`：使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="57398-147">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="57398-148">`[ResourceName <String>]`： Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="57398-148">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="57398-149">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="57398-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="57398-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="57398-150">RELATED LINKS</span></span>

