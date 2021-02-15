---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/remove-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
ms.openlocfilehash: 1a3125939e1640a6bd734ee8f75f36a4c34196ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142304"
---
# <span data-ttu-id="d4c45-101">Remove-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="d4c45-101">Remove-AzHealthBot</span></span>

## <span data-ttu-id="d4c45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d4c45-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c45-103">刪除 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="d4c45-103">Delete a HealthBot.</span></span>

## <span data-ttu-id="d4c45-104">句法</span><span class="sxs-lookup"><span data-stu-id="d4c45-104">SYNTAX</span></span>

### <span data-ttu-id="d4c45-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="d4c45-105">Delete (Default)</span></span>
```
Remove-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d4c45-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d4c45-106">DeleteViaIdentity</span></span>
```
Remove-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d4c45-107">說明</span><span class="sxs-lookup"><span data-stu-id="d4c45-107">DESCRIPTION</span></span>
<span data-ttu-id="d4c45-108">刪除 HealthBot。</span><span class="sxs-lookup"><span data-stu-id="d4c45-108">Delete a HealthBot.</span></span>

## <span data-ttu-id="d4c45-109">示例</span><span class="sxs-lookup"><span data-stu-id="d4c45-109">EXAMPLES</span></span>

### <span data-ttu-id="d4c45-110">範例1：依 ResourceGroupName 和 Name 刪除 HealthBot</span><span class="sxs-lookup"><span data-stu-id="d4c45-110">Example 1: Delete HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzHealthBot -Name yourihealthbot -ResourceGroupName youriTest

```

<span data-ttu-id="d4c45-111">依 ResourceGroupName 和 Name 刪除 HealthBot</span><span class="sxs-lookup"><span data-stu-id="d4c45-111">Delete HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="d4c45-112">範例2：刪除 HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="d4c45-112">Example 2: Delete HealthBot by InputObject</span></span>
```powershell
PS C:\> $gethealthbot = Get-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest
Remove-AzHealthBot -InputObject $gethealthbot

```

<span data-ttu-id="d4c45-113">刪除 HealthBot by InputObject</span><span class="sxs-lookup"><span data-stu-id="d4c45-113">Delete HealthBot by InputObject</span></span>

## <span data-ttu-id="d4c45-114">參數</span><span class="sxs-lookup"><span data-stu-id="d4c45-114">PARAMETERS</span></span>

### <span data-ttu-id="d4c45-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d4c45-115">-AsJob</span></span>
<span data-ttu-id="d4c45-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="d4c45-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d4c45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c45-117">-DefaultProfile</span></span>
<span data-ttu-id="d4c45-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d4c45-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4c45-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4c45-119">-InputObject</span></span>
<span data-ttu-id="d4c45-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="d4c45-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d4c45-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d4c45-121">-Name</span></span>
<span data-ttu-id="d4c45-122">Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4c45-122">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="d4c45-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d4c45-123">-NoWait</span></span>
<span data-ttu-id="d4c45-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="d4c45-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d4c45-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d4c45-125">-PassThru</span></span>
<span data-ttu-id="d4c45-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="d4c45-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d4c45-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c45-127">-ResourceGroupName</span></span>
<span data-ttu-id="d4c45-128">使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4c45-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="d4c45-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d4c45-129">-SubscriptionId</span></span>
<span data-ttu-id="d4c45-130">Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="d4c45-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d4c45-131">-確認</span><span class="sxs-lookup"><span data-stu-id="d4c45-131">-Confirm</span></span>
<span data-ttu-id="d4c45-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d4c45-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4c45-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4c45-133">-WhatIf</span></span>
<span data-ttu-id="d4c45-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d4c45-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4c45-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d4c45-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4c45-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c45-136">CommonParameters</span></span>
<span data-ttu-id="d4c45-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d4c45-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c45-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d4c45-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c45-139">輸入</span><span class="sxs-lookup"><span data-stu-id="d4c45-139">INPUTS</span></span>

### <span data-ttu-id="d4c45-140">IHealthBotIdentity （HealthBot）的</span><span class="sxs-lookup"><span data-stu-id="d4c45-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="d4c45-141">輸出</span><span class="sxs-lookup"><span data-stu-id="d4c45-141">OUTPUTS</span></span>

### <span data-ttu-id="d4c45-142">System.object</span><span class="sxs-lookup"><span data-stu-id="d4c45-142">System.Boolean</span></span>

## <span data-ttu-id="d4c45-143">筆記</span><span class="sxs-lookup"><span data-stu-id="d4c45-143">NOTES</span></span>

<span data-ttu-id="d4c45-144">別名</span><span class="sxs-lookup"><span data-stu-id="d4c45-144">ALIASES</span></span>

<span data-ttu-id="d4c45-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="d4c45-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d4c45-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d4c45-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d4c45-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="d4c45-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d4c45-148">INPUTOBJECT <IHealthBotIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="d4c45-148">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d4c45-149">`[BotName <String>]`： Bot 資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4c45-149">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="d4c45-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="d4c45-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d4c45-151">`[ResourceGroupName <String>]`：使用者訂閱中 Bot 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d4c45-151">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="d4c45-152">`[SubscriptionId <String>]`： Azure 訂閱 ID。</span><span class="sxs-lookup"><span data-stu-id="d4c45-152">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="d4c45-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="d4c45-153">RELATED LINKS</span></span>

