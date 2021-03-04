---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/remove-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
ms.openlocfilehash: 2b2a4eba0a062b90866479409e80bbe7e55c1984
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917226"
---
# <span data-ttu-id="b3610-101">Remove-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="b3610-101">Remove-AzHealthBot</span></span>

## <span data-ttu-id="b3610-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3610-102">SYNOPSIS</span></span>
<span data-ttu-id="b3610-103">刪除 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="b3610-103">Delete a HealthBot.</span></span>

## <span data-ttu-id="b3610-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3610-104">SYNTAX</span></span>

### <span data-ttu-id="b3610-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="b3610-105">Delete (Default)</span></span>
```
Remove-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3610-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b3610-106">DeleteViaIdentity</span></span>
```
Remove-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b3610-107">描述</span><span class="sxs-lookup"><span data-stu-id="b3610-107">DESCRIPTION</span></span>
<span data-ttu-id="b3610-108">刪除 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="b3610-108">Delete a HealthBot.</span></span>

## <span data-ttu-id="b3610-109">例子</span><span class="sxs-lookup"><span data-stu-id="b3610-109">EXAMPLES</span></span>

### <span data-ttu-id="b3610-110">範例 1：按 ResourceGroupName 和 Name 刪除 HealthBot</span><span class="sxs-lookup"><span data-stu-id="b3610-110">Example 1: Delete HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzHealthBot -Name yourihealthbot -ResourceGroupName youriTest

```

<span data-ttu-id="b3610-111">按 ResourceGroupName 和 Name 刪除 HealthBot</span><span class="sxs-lookup"><span data-stu-id="b3610-111">Delete HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="b3610-112">範例 2：刪除 HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="b3610-112">Example 2: Delete HealthBot by InputObject</span></span>
```powershell
PS C:\> $gethealthbot = Get-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest
Remove-AzHealthBot -InputObject $gethealthbot

```

<span data-ttu-id="b3610-113">按 InputObject 刪除 HealthBot</span><span class="sxs-lookup"><span data-stu-id="b3610-113">Delete HealthBot by InputObject</span></span>

## <span data-ttu-id="b3610-114">參數</span><span class="sxs-lookup"><span data-stu-id="b3610-114">PARAMETERS</span></span>

### <span data-ttu-id="b3610-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3610-115">-AsJob</span></span>
<span data-ttu-id="b3610-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="b3610-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b3610-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3610-117">-DefaultProfile</span></span>
<span data-ttu-id="b3610-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3610-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3610-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3610-119">-InputObject</span></span>
<span data-ttu-id="b3610-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b3610-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3610-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b3610-121">-Name</span></span>
<span data-ttu-id="b3610-122">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3610-122">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="b3610-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b3610-123">-NoWait</span></span>
<span data-ttu-id="b3610-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="b3610-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b3610-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3610-125">-PassThru</span></span>
<span data-ttu-id="b3610-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="b3610-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b3610-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3610-127">-ResourceGroupName</span></span>
<span data-ttu-id="b3610-128">使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="b3610-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="b3610-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3610-129">-SubscriptionId</span></span>
<span data-ttu-id="b3610-130">Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3610-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="b3610-131">-確認</span><span class="sxs-lookup"><span data-stu-id="b3610-131">-Confirm</span></span>
<span data-ttu-id="b3610-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b3610-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3610-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3610-133">-WhatIf</span></span>
<span data-ttu-id="b3610-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b3610-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3610-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b3610-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3610-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3610-136">CommonParameters</span></span>
<span data-ttu-id="b3610-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3610-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3610-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3610-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3610-139">輸入</span><span class="sxs-lookup"><span data-stu-id="b3610-139">INPUTS</span></span>

### <span data-ttu-id="b3610-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="b3610-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="b3610-141">輸出</span><span class="sxs-lookup"><span data-stu-id="b3610-141">OUTPUTS</span></span>

### <span data-ttu-id="b3610-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b3610-142">System.Boolean</span></span>

## <span data-ttu-id="b3610-143">筆記</span><span class="sxs-lookup"><span data-stu-id="b3610-143">NOTES</span></span>

<span data-ttu-id="b3610-144">別名</span><span class="sxs-lookup"><span data-stu-id="b3610-144">ALIASES</span></span>

<span data-ttu-id="b3610-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b3610-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3610-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b3610-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3610-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b3610-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3610-148">INPUTOBJECT： <IHealthBotIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b3610-148">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3610-149">`[BotName <String>]`：Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b3610-149">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="b3610-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b3610-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3610-151">`[ResourceGroupName <String>]`：使用者訂閱中的 Bot 資源組名。</span><span class="sxs-lookup"><span data-stu-id="b3610-151">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="b3610-152">`[SubscriptionId <String>]`：Azure 訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b3610-152">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="b3610-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3610-153">RELATED LINKS</span></span>

