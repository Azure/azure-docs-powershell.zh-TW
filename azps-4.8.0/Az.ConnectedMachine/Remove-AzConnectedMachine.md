---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94136543"
---
# <span data-ttu-id="bd98b-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="bd98b-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="bd98b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bd98b-102">SYNOPSIS</span></span>
<span data-ttu-id="bd98b-103">在 Azure 中移除混合式電腦身分識別的操作。</span><span class="sxs-lookup"><span data-stu-id="bd98b-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="bd98b-104">句法</span><span class="sxs-lookup"><span data-stu-id="bd98b-104">SYNTAX</span></span>

### <span data-ttu-id="bd98b-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="bd98b-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bd98b-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bd98b-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bd98b-107">說明</span><span class="sxs-lookup"><span data-stu-id="bd98b-107">DESCRIPTION</span></span>
<span data-ttu-id="bd98b-108">在 Azure 中移除混合式電腦身分識別的操作。</span><span class="sxs-lookup"><span data-stu-id="bd98b-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="bd98b-109">示例</span><span class="sxs-lookup"><span data-stu-id="bd98b-109">EXAMPLES</span></span>

### <span data-ttu-id="bd98b-110">範例1：移除已連接的電腦</span><span class="sxs-lookup"><span data-stu-id="bd98b-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="bd98b-111">刪除已連接的電腦。</span><span class="sxs-lookup"><span data-stu-id="bd98b-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="bd98b-112">範例2：透過管線移除已連接的電腦</span><span class="sxs-lookup"><span data-stu-id="bd98b-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="bd98b-113">移除 [資源] 群組中的所有電腦 `contoso-connected-machines` 。</span><span class="sxs-lookup"><span data-stu-id="bd98b-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="bd98b-114">參數</span><span class="sxs-lookup"><span data-stu-id="bd98b-114">PARAMETERS</span></span>

### <span data-ttu-id="bd98b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd98b-115">-DefaultProfile</span></span>
<span data-ttu-id="bd98b-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bd98b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd98b-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd98b-117">-InputObject</span></span>
<span data-ttu-id="bd98b-118">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="bd98b-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bd98b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="bd98b-119">-Name</span></span>
<span data-ttu-id="bd98b-120">混合式電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd98b-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="bd98b-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd98b-121">-PassThru</span></span>
<span data-ttu-id="bd98b-122">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="bd98b-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bd98b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd98b-123">-ResourceGroupName</span></span>
<span data-ttu-id="bd98b-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd98b-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="bd98b-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bd98b-125">-SubscriptionId</span></span>
<span data-ttu-id="bd98b-126">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="bd98b-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bd98b-127">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="bd98b-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bd98b-128">-確認</span><span class="sxs-lookup"><span data-stu-id="bd98b-128">-Confirm</span></span>
<span data-ttu-id="bd98b-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bd98b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd98b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd98b-130">-WhatIf</span></span>
<span data-ttu-id="bd98b-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bd98b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd98b-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bd98b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd98b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd98b-133">CommonParameters</span></span>
<span data-ttu-id="bd98b-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bd98b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd98b-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bd98b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd98b-136">輸入</span><span class="sxs-lookup"><span data-stu-id="bd98b-136">INPUTS</span></span>

### <span data-ttu-id="bd98b-137">IConnectedMachineIdentity （ConnectedMachine）的</span><span class="sxs-lookup"><span data-stu-id="bd98b-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="bd98b-138">輸出</span><span class="sxs-lookup"><span data-stu-id="bd98b-138">OUTPUTS</span></span>

### <span data-ttu-id="bd98b-139">System.object</span><span class="sxs-lookup"><span data-stu-id="bd98b-139">System.Boolean</span></span>

## <span data-ttu-id="bd98b-140">筆記</span><span class="sxs-lookup"><span data-stu-id="bd98b-140">NOTES</span></span>

<span data-ttu-id="bd98b-141">別名</span><span class="sxs-lookup"><span data-stu-id="bd98b-141">ALIASES</span></span>

<span data-ttu-id="bd98b-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="bd98b-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bd98b-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="bd98b-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bd98b-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="bd98b-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bd98b-145">INPUTOBJECT <IConnectedMachineIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="bd98b-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bd98b-146">`[ExtensionName <String>]`：電腦副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd98b-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="bd98b-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="bd98b-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bd98b-148">`[Name <String>]`：混合式電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd98b-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="bd98b-149">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bd98b-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="bd98b-150">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="bd98b-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bd98b-151">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="bd98b-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bd98b-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="bd98b-152">RELATED LINKS</span></span>

