---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: 777c02f6588d7c1fdb1a1d6e9e9c004f51694293
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917014"
---
# <span data-ttu-id="436d2-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="436d2-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="436d2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="436d2-102">SYNOPSIS</span></span>
<span data-ttu-id="436d2-103">刪除延伸模組的作業。</span><span class="sxs-lookup"><span data-stu-id="436d2-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="436d2-104">語法</span><span class="sxs-lookup"><span data-stu-id="436d2-104">SYNTAX</span></span>

### <span data-ttu-id="436d2-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="436d2-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="436d2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="436d2-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="436d2-107">描述</span><span class="sxs-lookup"><span data-stu-id="436d2-107">DESCRIPTION</span></span>
<span data-ttu-id="436d2-108">刪除延伸模組的作業。</span><span class="sxs-lookup"><span data-stu-id="436d2-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="436d2-109">例子</span><span class="sxs-lookup"><span data-stu-id="436d2-109">EXAMPLES</span></span>

### <span data-ttu-id="436d2-110">範例 1：移除電腦副檔名。</span><span class="sxs-lookup"><span data-stu-id="436d2-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="436d2-111">刪除電腦上延伸模組。</span><span class="sxs-lookup"><span data-stu-id="436d2-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="436d2-112">範例 2：透過管線移除延伸模組</span><span class="sxs-lookup"><span data-stu-id="436d2-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="436d2-113">移除指定電腦中所有的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="436d2-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="436d2-114">參數</span><span class="sxs-lookup"><span data-stu-id="436d2-114">PARAMETERS</span></span>

### <span data-ttu-id="436d2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="436d2-115">-AsJob</span></span>
<span data-ttu-id="436d2-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="436d2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="436d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="436d2-117">-DefaultProfile</span></span>
<span data-ttu-id="436d2-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="436d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="436d2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="436d2-119">-InputObject</span></span>
<span data-ttu-id="436d2-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="436d2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="436d2-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="436d2-121">-MachineName</span></span>
<span data-ttu-id="436d2-122">延伸模組應刪除之電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="436d2-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="436d2-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="436d2-123">-Name</span></span>
<span data-ttu-id="436d2-124">電腦副檔名。</span><span class="sxs-lookup"><span data-stu-id="436d2-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="436d2-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="436d2-125">-NoWait</span></span>
<span data-ttu-id="436d2-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="436d2-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="436d2-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="436d2-127">-PassThru</span></span>
<span data-ttu-id="436d2-128">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="436d2-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="436d2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="436d2-129">-ResourceGroupName</span></span>
<span data-ttu-id="436d2-130">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="436d2-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="436d2-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="436d2-131">-SubscriptionId</span></span>
<span data-ttu-id="436d2-132">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="436d2-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="436d2-133">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="436d2-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="436d2-134">-確認</span><span class="sxs-lookup"><span data-stu-id="436d2-134">-Confirm</span></span>
<span data-ttu-id="436d2-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="436d2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="436d2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="436d2-136">-WhatIf</span></span>
<span data-ttu-id="436d2-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="436d2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="436d2-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="436d2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="436d2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="436d2-139">CommonParameters</span></span>
<span data-ttu-id="436d2-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="436d2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="436d2-141">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="436d2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="436d2-142">輸入</span><span class="sxs-lookup"><span data-stu-id="436d2-142">INPUTS</span></span>

### <span data-ttu-id="436d2-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="436d2-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="436d2-144">輸出</span><span class="sxs-lookup"><span data-stu-id="436d2-144">OUTPUTS</span></span>

### <span data-ttu-id="436d2-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="436d2-145">System.Boolean</span></span>

## <span data-ttu-id="436d2-146">筆記</span><span class="sxs-lookup"><span data-stu-id="436d2-146">NOTES</span></span>

<span data-ttu-id="436d2-147">別名</span><span class="sxs-lookup"><span data-stu-id="436d2-147">ALIASES</span></span>

<span data-ttu-id="436d2-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="436d2-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="436d2-149">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="436d2-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="436d2-150">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="436d2-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="436d2-151">INPUTOBJECT： <IConnectedMachineIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="436d2-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="436d2-152">`[ExtensionName <String>]`：電腦副檔名。</span><span class="sxs-lookup"><span data-stu-id="436d2-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="436d2-153">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="436d2-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="436d2-154">`[Name <String>]`：混合式電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="436d2-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="436d2-155">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="436d2-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="436d2-156">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="436d2-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="436d2-157">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="436d2-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="436d2-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="436d2-158">RELATED LINKS</span></span>

