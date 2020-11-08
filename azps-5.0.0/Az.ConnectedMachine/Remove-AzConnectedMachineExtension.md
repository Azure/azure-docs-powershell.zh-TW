---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140181"
---
# <span data-ttu-id="bef1c-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="bef1c-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="bef1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bef1c-102">SYNOPSIS</span></span>
<span data-ttu-id="bef1c-103">刪除延伸的操作。</span><span class="sxs-lookup"><span data-stu-id="bef1c-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="bef1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="bef1c-104">SYNTAX</span></span>

### <span data-ttu-id="bef1c-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="bef1c-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bef1c-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bef1c-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bef1c-107">說明</span><span class="sxs-lookup"><span data-stu-id="bef1c-107">DESCRIPTION</span></span>
<span data-ttu-id="bef1c-108">刪除延伸的操作。</span><span class="sxs-lookup"><span data-stu-id="bef1c-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="bef1c-109">示例</span><span class="sxs-lookup"><span data-stu-id="bef1c-109">EXAMPLES</span></span>

### <span data-ttu-id="bef1c-110">範例1：移除電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="bef1c-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="bef1c-111">刪除電腦上的副檔名。</span><span class="sxs-lookup"><span data-stu-id="bef1c-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="bef1c-112">範例2：透過管線移除延伸</span><span class="sxs-lookup"><span data-stu-id="bef1c-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="bef1c-113">移除指定電腦中的所有延伸。</span><span class="sxs-lookup"><span data-stu-id="bef1c-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="bef1c-114">參數</span><span class="sxs-lookup"><span data-stu-id="bef1c-114">PARAMETERS</span></span>

### <span data-ttu-id="bef1c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bef1c-115">-AsJob</span></span>
<span data-ttu-id="bef1c-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="bef1c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bef1c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bef1c-117">-DefaultProfile</span></span>
<span data-ttu-id="bef1c-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bef1c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bef1c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bef1c-119">-InputObject</span></span>
<span data-ttu-id="bef1c-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="bef1c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bef1c-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="bef1c-121">-MachineName</span></span>
<span data-ttu-id="bef1c-122">應刪除延伸的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="bef1c-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="bef1c-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="bef1c-123">-Name</span></span>
<span data-ttu-id="bef1c-124">電腦副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="bef1c-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="bef1c-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bef1c-125">-NoWait</span></span>
<span data-ttu-id="bef1c-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="bef1c-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bef1c-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bef1c-127">-PassThru</span></span>
<span data-ttu-id="bef1c-128">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="bef1c-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bef1c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bef1c-129">-ResourceGroupName</span></span>
<span data-ttu-id="bef1c-130">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bef1c-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="bef1c-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bef1c-131">-SubscriptionId</span></span>
<span data-ttu-id="bef1c-132">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="bef1c-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bef1c-133">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="bef1c-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bef1c-134">-確認</span><span class="sxs-lookup"><span data-stu-id="bef1c-134">-Confirm</span></span>
<span data-ttu-id="bef1c-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bef1c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bef1c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bef1c-136">-WhatIf</span></span>
<span data-ttu-id="bef1c-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bef1c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bef1c-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bef1c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bef1c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bef1c-139">CommonParameters</span></span>
<span data-ttu-id="bef1c-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bef1c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bef1c-141">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bef1c-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bef1c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="bef1c-142">INPUTS</span></span>

### <span data-ttu-id="bef1c-143">IConnectedMachineIdentity （ConnectedMachine）的</span><span class="sxs-lookup"><span data-stu-id="bef1c-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="bef1c-144">輸出</span><span class="sxs-lookup"><span data-stu-id="bef1c-144">OUTPUTS</span></span>

### <span data-ttu-id="bef1c-145">System.object</span><span class="sxs-lookup"><span data-stu-id="bef1c-145">System.Boolean</span></span>

## <span data-ttu-id="bef1c-146">筆記</span><span class="sxs-lookup"><span data-stu-id="bef1c-146">NOTES</span></span>

<span data-ttu-id="bef1c-147">別名</span><span class="sxs-lookup"><span data-stu-id="bef1c-147">ALIASES</span></span>

<span data-ttu-id="bef1c-148">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="bef1c-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bef1c-149">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="bef1c-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bef1c-150">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="bef1c-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bef1c-151">INPUTOBJECT <IConnectedMachineIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="bef1c-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bef1c-152">`[ExtensionName <String>]`：電腦副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="bef1c-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="bef1c-153">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="bef1c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bef1c-154">`[Name <String>]`：混合式電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="bef1c-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="bef1c-155">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="bef1c-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="bef1c-156">`[SubscriptionId <String>]`：可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="bef1c-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bef1c-157">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="bef1c-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bef1c-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="bef1c-158">RELATED LINKS</span></span>

