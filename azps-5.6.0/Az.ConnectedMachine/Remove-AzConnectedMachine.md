---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: 72e7df2a9f543af6b3247e400d55ac0f9c14ce0d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917017"
---
# <span data-ttu-id="099c4-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="099c4-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="099c4-102">簡介</span><span class="sxs-lookup"><span data-stu-id="099c4-102">SYNOPSIS</span></span>
<span data-ttu-id="099c4-103">在 Azure 中移除混合式電腦身分識別的作業。</span><span class="sxs-lookup"><span data-stu-id="099c4-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="099c4-104">語法</span><span class="sxs-lookup"><span data-stu-id="099c4-104">SYNTAX</span></span>

### <span data-ttu-id="099c4-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="099c4-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="099c4-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="099c4-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="099c4-107">描述</span><span class="sxs-lookup"><span data-stu-id="099c4-107">DESCRIPTION</span></span>
<span data-ttu-id="099c4-108">在 Azure 中移除混合式電腦身分識別的作業。</span><span class="sxs-lookup"><span data-stu-id="099c4-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="099c4-109">例子</span><span class="sxs-lookup"><span data-stu-id="099c4-109">EXAMPLES</span></span>

### <span data-ttu-id="099c4-110">範例 1：移除已連接的機器</span><span class="sxs-lookup"><span data-stu-id="099c4-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="099c4-111">刪除已連接的機器。</span><span class="sxs-lookup"><span data-stu-id="099c4-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="099c4-112">範例 2：透過管線移除連接的機器</span><span class="sxs-lookup"><span data-stu-id="099c4-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="099c4-113">移除資源群組中 `contoso-connected-machines` 所有的電腦。</span><span class="sxs-lookup"><span data-stu-id="099c4-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="099c4-114">參數</span><span class="sxs-lookup"><span data-stu-id="099c4-114">PARAMETERS</span></span>

### <span data-ttu-id="099c4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="099c4-115">-DefaultProfile</span></span>
<span data-ttu-id="099c4-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="099c4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="099c4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="099c4-117">-InputObject</span></span>
<span data-ttu-id="099c4-118">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="099c4-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="099c4-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="099c4-119">-Name</span></span>
<span data-ttu-id="099c4-120">混合式電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="099c4-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="099c4-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="099c4-121">-PassThru</span></span>
<span data-ttu-id="099c4-122">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="099c4-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="099c4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="099c4-123">-ResourceGroupName</span></span>
<span data-ttu-id="099c4-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="099c4-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="099c4-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="099c4-125">-SubscriptionId</span></span>
<span data-ttu-id="099c4-126">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="099c4-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="099c4-127">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="099c4-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="099c4-128">-確認</span><span class="sxs-lookup"><span data-stu-id="099c4-128">-Confirm</span></span>
<span data-ttu-id="099c4-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="099c4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="099c4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="099c4-130">-WhatIf</span></span>
<span data-ttu-id="099c4-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="099c4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="099c4-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="099c4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="099c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="099c4-133">CommonParameters</span></span>
<span data-ttu-id="099c4-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="099c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="099c4-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="099c4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="099c4-136">輸入</span><span class="sxs-lookup"><span data-stu-id="099c4-136">INPUTS</span></span>

### <span data-ttu-id="099c4-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="099c4-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="099c4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="099c4-138">OUTPUTS</span></span>

### <span data-ttu-id="099c4-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="099c4-139">System.Boolean</span></span>

## <span data-ttu-id="099c4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="099c4-140">NOTES</span></span>

<span data-ttu-id="099c4-141">別名</span><span class="sxs-lookup"><span data-stu-id="099c4-141">ALIASES</span></span>

<span data-ttu-id="099c4-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="099c4-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="099c4-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="099c4-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="099c4-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="099c4-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="099c4-145">INPUTOBJECT： <IConnectedMachineIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="099c4-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="099c4-146">`[ExtensionName <String>]`：電腦副檔名。</span><span class="sxs-lookup"><span data-stu-id="099c4-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="099c4-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="099c4-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="099c4-148">`[Name <String>]`：混合式電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="099c4-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="099c4-149">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="099c4-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="099c4-150">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="099c4-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="099c4-151">訂閱識別碼會構成每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="099c4-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="099c4-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="099c4-152">RELATED LINKS</span></span>

