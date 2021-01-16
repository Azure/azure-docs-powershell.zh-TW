---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: ef75ec3e48a68bffce7c5b281f542bd2e3dba9d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446675"
---
# <span data-ttu-id="0d895-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="0d895-101">Remove-AzBotService</span></span>

## <span data-ttu-id="0d895-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d895-102">SYNOPSIS</span></span>
<span data-ttu-id="0d895-103">從 [資源] 群組刪除 Bot 服務。</span><span class="sxs-lookup"><span data-stu-id="0d895-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="0d895-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d895-104">SYNTAX</span></span>

### <span data-ttu-id="0d895-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="0d895-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0d895-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0d895-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0d895-107">說明</span><span class="sxs-lookup"><span data-stu-id="0d895-107">DESCRIPTION</span></span>
<span data-ttu-id="0d895-108">從 [資源] 群組刪除 Bot 服務。</span><span class="sxs-lookup"><span data-stu-id="0d895-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="0d895-109">示例</span><span class="sxs-lookup"><span data-stu-id="0d895-109">EXAMPLES</span></span>

### <span data-ttu-id="0d895-110">範例1：依名稱和 ResourceGroupName 刪除 BotService</span><span class="sxs-lookup"><span data-stu-id="0d895-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="0d895-111">依名稱和 ResourceGroupName 刪除 BotService</span><span class="sxs-lookup"><span data-stu-id="0d895-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="0d895-112">範例2：刪除 BotService By InputObject</span><span class="sxs-lookup"><span data-stu-id="0d895-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="0d895-113">刪除 BotService By InputObject</span><span class="sxs-lookup"><span data-stu-id="0d895-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="0d895-114">參數</span><span class="sxs-lookup"><span data-stu-id="0d895-114">PARAMETERS</span></span>

### <span data-ttu-id="0d895-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d895-115">-DefaultProfile</span></span>
<span data-ttu-id="0d895-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="0d895-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d895-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d895-117">-InputObject</span></span>
<span data-ttu-id="0d895-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="0d895-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d895-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d895-119">-Name</span></span>
<span data-ttu-id="0d895-120">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d895-120">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d895-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d895-121">-PassThru</span></span>
<span data-ttu-id="0d895-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="0d895-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0d895-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d895-123">-ResourceGroupName</span></span>
<span data-ttu-id="0d895-124">使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d895-124">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d895-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0d895-125">-SubscriptionId</span></span>
<span data-ttu-id="0d895-126">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="0d895-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d895-127">-確認</span><span class="sxs-lookup"><span data-stu-id="0d895-127">-Confirm</span></span>
<span data-ttu-id="0d895-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d895-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d895-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d895-129">-WhatIf</span></span>
<span data-ttu-id="0d895-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d895-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d895-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d895-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d895-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d895-132">CommonParameters</span></span>
<span data-ttu-id="0d895-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d895-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d895-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="0d895-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d895-135">輸入</span><span class="sxs-lookup"><span data-stu-id="0d895-135">INPUTS</span></span>

### <span data-ttu-id="0d895-136">IBotServiceIdentity （BotService）的</span><span class="sxs-lookup"><span data-stu-id="0d895-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="0d895-137">輸出</span><span class="sxs-lookup"><span data-stu-id="0d895-137">OUTPUTS</span></span>

### <span data-ttu-id="0d895-138">System.object</span><span class="sxs-lookup"><span data-stu-id="0d895-138">System.Boolean</span></span>

## <span data-ttu-id="0d895-139">筆記</span><span class="sxs-lookup"><span data-stu-id="0d895-139">NOTES</span></span>

<span data-ttu-id="0d895-140">別名</span><span class="sxs-lookup"><span data-stu-id="0d895-140">ALIASES</span></span>

<span data-ttu-id="0d895-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="0d895-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0d895-142">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="0d895-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0d895-143">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="0d895-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0d895-144">INPUTOBJECT <IBotServiceIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="0d895-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0d895-145">`[ChannelName <ChannelName?>]`：頻道資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d895-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="0d895-146">`[ConnectionName <String>]`： Bot 服務連線設定資源的名稱</span><span class="sxs-lookup"><span data-stu-id="0d895-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="0d895-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="0d895-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0d895-148">`[ResourceGroupName <String>]`：使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d895-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="0d895-149">`[ResourceName <String>]`： Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d895-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="0d895-150">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="0d895-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="0d895-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d895-151">RELATED LINKS</span></span>

