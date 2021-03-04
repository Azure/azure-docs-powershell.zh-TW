---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 54678dd00a0edae4af3a90c84e1c930c1c032e84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906954"
---
# <span data-ttu-id="8ae27-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="8ae27-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="8ae27-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8ae27-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae27-103">刪除網路管理成員。</span><span class="sxs-lookup"><span data-stu-id="8ae27-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="8ae27-104">語法</span><span class="sxs-lookup"><span data-stu-id="8ae27-104">SYNTAX</span></span>

### <span data-ttu-id="8ae27-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="8ae27-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8ae27-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8ae27-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8ae27-107">描述</span><span class="sxs-lookup"><span data-stu-id="8ae27-107">DESCRIPTION</span></span>
<span data-ttu-id="8ae27-108">刪除網路管理成員。</span><span class="sxs-lookup"><span data-stu-id="8ae27-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="8ae27-109">例子</span><span class="sxs-lookup"><span data-stu-id="8ae27-109">EXAMPLES</span></span>

### <span data-ttu-id="8ae27-110">範例 1：移除成員</span><span class="sxs-lookup"><span data-stu-id="8ae27-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="8ae27-111">此命令會移除網路管理成員。</span><span class="sxs-lookup"><span data-stu-id="8ae27-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="8ae27-112">範例 2：移除成員</span><span class="sxs-lookup"><span data-stu-id="8ae27-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="8ae27-113">此命令會移除網路管理成員。</span><span class="sxs-lookup"><span data-stu-id="8ae27-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="8ae27-114">參數</span><span class="sxs-lookup"><span data-stu-id="8ae27-114">PARAMETERS</span></span>

### <span data-ttu-id="8ae27-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ae27-115">-AsJob</span></span>
<span data-ttu-id="8ae27-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="8ae27-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8ae27-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ae27-117">-DefaultProfile</span></span>
<span data-ttu-id="8ae27-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ae27-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ae27-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ae27-119">-InputObject</span></span>
<span data-ttu-id="8ae27-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8ae27-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae27-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="8ae27-121">-Name</span></span>
<span data-ttu-id="8ae27-122">進位會員名稱</span><span class="sxs-lookup"><span data-stu-id="8ae27-122">Blockchain member name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae27-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8ae27-123">-NoWait</span></span>
<span data-ttu-id="8ae27-124">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="8ae27-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8ae27-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ae27-125">-PassThru</span></span>
<span data-ttu-id="8ae27-126">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="8ae27-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8ae27-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae27-127">-ResourceGroupName</span></span>
<span data-ttu-id="8ae27-128">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8ae27-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8ae27-129">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="8ae27-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8ae27-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ae27-130">-SubscriptionId</span></span>
<span data-ttu-id="8ae27-131">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ae27-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8ae27-132">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8ae27-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8ae27-133">-確認</span><span class="sxs-lookup"><span data-stu-id="8ae27-133">-Confirm</span></span>
<span data-ttu-id="8ae27-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8ae27-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ae27-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ae27-135">-WhatIf</span></span>
<span data-ttu-id="8ae27-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8ae27-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ae27-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8ae27-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ae27-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae27-138">CommonParameters</span></span>
<span data-ttu-id="8ae27-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8ae27-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae27-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ae27-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae27-141">輸入</span><span class="sxs-lookup"><span data-stu-id="8ae27-141">INPUTS</span></span>

### <span data-ttu-id="8ae27-142">Microsoft.Azure.PowerShell.Cmdlets.Ident.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="8ae27-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="8ae27-143">輸出</span><span class="sxs-lookup"><span data-stu-id="8ae27-143">OUTPUTS</span></span>

### <span data-ttu-id="8ae27-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8ae27-144">System.Boolean</span></span>

## <span data-ttu-id="8ae27-145">筆記</span><span class="sxs-lookup"><span data-stu-id="8ae27-145">NOTES</span></span>

<span data-ttu-id="8ae27-146">別名</span><span class="sxs-lookup"><span data-stu-id="8ae27-146">ALIASES</span></span>

<span data-ttu-id="8ae27-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8ae27-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8ae27-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8ae27-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8ae27-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8ae27-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8ae27-150">INPUTOBJECT： <IBlockchainIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8ae27-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8ae27-151">`[BlockchainMemberName <String>]`：進位會員名稱。</span><span class="sxs-lookup"><span data-stu-id="8ae27-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="8ae27-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="8ae27-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8ae27-153">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="8ae27-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="8ae27-154">`[OperationId <String>]`：操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ae27-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="8ae27-155">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8ae27-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8ae27-156">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="8ae27-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8ae27-157">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8ae27-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="8ae27-158">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8ae27-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="8ae27-159">`[TransactionNodeName <String>]`：交易處理節點名稱。</span><span class="sxs-lookup"><span data-stu-id="8ae27-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="8ae27-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ae27-160">RELATED LINKS</span></span>

