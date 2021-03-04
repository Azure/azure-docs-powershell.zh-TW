---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: 486490a3b88025fb97b8790df202c944c05d888e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905190"
---
# <span data-ttu-id="b48b0-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="b48b0-101">Remove-AzBotService</span></span>

## <span data-ttu-id="b48b0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b48b0-102">SYNOPSIS</span></span>
<span data-ttu-id="b48b0-103">從資源群組刪除 Bot 服務。</span><span class="sxs-lookup"><span data-stu-id="b48b0-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="b48b0-104">語法</span><span class="sxs-lookup"><span data-stu-id="b48b0-104">SYNTAX</span></span>

### <span data-ttu-id="b48b0-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="b48b0-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b48b0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b48b0-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b48b0-107">描述</span><span class="sxs-lookup"><span data-stu-id="b48b0-107">DESCRIPTION</span></span>
<span data-ttu-id="b48b0-108">從資源群組刪除 Bot 服務。</span><span class="sxs-lookup"><span data-stu-id="b48b0-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="b48b0-109">例子</span><span class="sxs-lookup"><span data-stu-id="b48b0-109">EXAMPLES</span></span>

### <span data-ttu-id="b48b0-110">範例 1：刪除 BotService By Name and ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b48b0-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="b48b0-111">刪除 BotService By Name 與 ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b48b0-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="b48b0-112">範例 2：刪除 BotService By InputObject</span><span class="sxs-lookup"><span data-stu-id="b48b0-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="b48b0-113">刪除 BotService By InputObject</span><span class="sxs-lookup"><span data-stu-id="b48b0-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="b48b0-114">參數</span><span class="sxs-lookup"><span data-stu-id="b48b0-114">PARAMETERS</span></span>

### <span data-ttu-id="b48b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b48b0-115">-DefaultProfile</span></span>
<span data-ttu-id="b48b0-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b48b0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b48b0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b48b0-117">-InputObject</span></span>
<span data-ttu-id="b48b0-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b48b0-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b48b0-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="b48b0-119">-Name</span></span>
<span data-ttu-id="b48b0-120">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b48b0-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="b48b0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b48b0-121">-PassThru</span></span>
<span data-ttu-id="b48b0-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="b48b0-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b48b0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b48b0-123">-ResourceGroupName</span></span>
<span data-ttu-id="b48b0-124">使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="b48b0-124">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="b48b0-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b48b0-125">-SubscriptionId</span></span>
<span data-ttu-id="b48b0-126">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b48b0-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b48b0-127">-確認</span><span class="sxs-lookup"><span data-stu-id="b48b0-127">-Confirm</span></span>
<span data-ttu-id="b48b0-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b48b0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b48b0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b48b0-129">-WhatIf</span></span>
<span data-ttu-id="b48b0-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b48b0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b48b0-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b48b0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b48b0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b48b0-132">CommonParameters</span></span>
<span data-ttu-id="b48b0-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b48b0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b48b0-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b48b0-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b48b0-135">輸入</span><span class="sxs-lookup"><span data-stu-id="b48b0-135">INPUTS</span></span>

### <span data-ttu-id="b48b0-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="b48b0-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="b48b0-137">輸出</span><span class="sxs-lookup"><span data-stu-id="b48b0-137">OUTPUTS</span></span>

### <span data-ttu-id="b48b0-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b48b0-138">System.Boolean</span></span>

## <span data-ttu-id="b48b0-139">筆記</span><span class="sxs-lookup"><span data-stu-id="b48b0-139">NOTES</span></span>

<span data-ttu-id="b48b0-140">別名</span><span class="sxs-lookup"><span data-stu-id="b48b0-140">ALIASES</span></span>

<span data-ttu-id="b48b0-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b48b0-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b48b0-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b48b0-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b48b0-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b48b0-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b48b0-144">INPUTOBJECT： <IBotServiceIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b48b0-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b48b0-145">`[ChannelName <ChannelName?>]`：通道資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b48b0-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="b48b0-146">`[ConnectionName <String>]`：Bot 服務連接設定資源的名稱</span><span class="sxs-lookup"><span data-stu-id="b48b0-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="b48b0-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b48b0-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b48b0-148">`[ResourceGroupName <String>]`：使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="b48b0-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="b48b0-149">`[ResourceName <String>]`：Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b48b0-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="b48b0-150">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b48b0-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="b48b0-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="b48b0-151">RELATED LINKS</span></span>

