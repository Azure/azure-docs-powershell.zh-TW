---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970542"
---
# <span data-ttu-id="3a356-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="3a356-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="3a356-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3a356-102">SYNOPSIS</span></span>
<span data-ttu-id="3a356-103">刪除延伸的操作。</span><span class="sxs-lookup"><span data-stu-id="3a356-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="3a356-104">句法</span><span class="sxs-lookup"><span data-stu-id="3a356-104">SYNTAX</span></span>

### <span data-ttu-id="3a356-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="3a356-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3a356-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3a356-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3a356-107">說明</span><span class="sxs-lookup"><span data-stu-id="3a356-107">DESCRIPTION</span></span>
<span data-ttu-id="3a356-108">刪除延伸的操作。</span><span class="sxs-lookup"><span data-stu-id="3a356-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="3a356-109">示例</span><span class="sxs-lookup"><span data-stu-id="3a356-109">EXAMPLES</span></span>

### <span data-ttu-id="3a356-110">範例1：移除電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="3a356-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="3a356-111">刪除電腦上的副檔名。</span><span class="sxs-lookup"><span data-stu-id="3a356-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="3a356-112">範例2：透過管線移除延伸</span><span class="sxs-lookup"><span data-stu-id="3a356-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="3a356-113">移除指定電腦中的所有延伸。</span><span class="sxs-lookup"><span data-stu-id="3a356-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="3a356-114">參數</span><span class="sxs-lookup"><span data-stu-id="3a356-114">PARAMETERS</span></span>

### <span data-ttu-id="3a356-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a356-115">-AsJob</span></span>
<span data-ttu-id="3a356-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="3a356-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3a356-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a356-117">-DefaultProfile</span></span>
<span data-ttu-id="3a356-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3a356-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a356-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a356-119">-InputObject</span></span>
<span data-ttu-id="3a356-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3a356-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3a356-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="3a356-121">-MachineName</span></span>
<span data-ttu-id="3a356-122">應刪除延伸的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="3a356-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="3a356-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="3a356-123">-Name</span></span>
<span data-ttu-id="3a356-124">電腦副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a356-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="3a356-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3a356-125">-NoWait</span></span>
<span data-ttu-id="3a356-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="3a356-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3a356-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a356-127">-PassThru</span></span>
<span data-ttu-id="3a356-128">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="3a356-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3a356-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a356-129">-ResourceGroupName</span></span>
<span data-ttu-id="3a356-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a356-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="3a356-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a356-131">-SubscriptionId</span></span>
<span data-ttu-id="3a356-132">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="3a356-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3a356-133">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="3a356-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3a356-134">-確認</span><span class="sxs-lookup"><span data-stu-id="3a356-134">-Confirm</span></span>
<span data-ttu-id="3a356-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3a356-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a356-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a356-136">-WhatIf</span></span>
<span data-ttu-id="3a356-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3a356-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a356-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3a356-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a356-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a356-139">CommonParameters</span></span>
<span data-ttu-id="3a356-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3a356-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a356-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3a356-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a356-142">輸入</span><span class="sxs-lookup"><span data-stu-id="3a356-142">INPUTS</span></span>

### <span data-ttu-id="3a356-143">IConnectedMachineIdentity （ConnectedMachine）的</span><span class="sxs-lookup"><span data-stu-id="3a356-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="3a356-144">輸出</span><span class="sxs-lookup"><span data-stu-id="3a356-144">OUTPUTS</span></span>

### <span data-ttu-id="3a356-145">System.object</span><span class="sxs-lookup"><span data-stu-id="3a356-145">System.Boolean</span></span>

## <span data-ttu-id="3a356-146">筆記</span><span class="sxs-lookup"><span data-stu-id="3a356-146">NOTES</span></span>

<span data-ttu-id="3a356-147">別名</span><span class="sxs-lookup"><span data-stu-id="3a356-147">ALIASES</span></span>

<span data-ttu-id="3a356-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3a356-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3a356-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3a356-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3a356-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3a356-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3a356-151">INPUTOBJECT <IConnectedMachineIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3a356-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3a356-152">`[ExtensionName <String>]`：電腦副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a356-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="3a356-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="3a356-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3a356-154">`[Name <String>]`：混合式電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a356-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="3a356-155">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3a356-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="3a356-156">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="3a356-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="3a356-157">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="3a356-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="3a356-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="3a356-158">RELATED LINKS</span></span>

