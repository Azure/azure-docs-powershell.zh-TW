---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970602"
---
# <span data-ttu-id="74519-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="74519-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="74519-102">摘要</span><span class="sxs-lookup"><span data-stu-id="74519-102">SYNOPSIS</span></span>
<span data-ttu-id="74519-103">刪除 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="74519-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="74519-104">句法</span><span class="sxs-lookup"><span data-stu-id="74519-104">SYNTAX</span></span>

### <span data-ttu-id="74519-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="74519-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74519-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="74519-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74519-107">說明</span><span class="sxs-lookup"><span data-stu-id="74519-107">DESCRIPTION</span></span>
<span data-ttu-id="74519-108">刪除 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="74519-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="74519-109">示例</span><span class="sxs-lookup"><span data-stu-id="74519-109">EXAMPLES</span></span>

### <span data-ttu-id="74519-110">範例1：移除 blockchain 成員</span><span class="sxs-lookup"><span data-stu-id="74519-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="74519-111">這個命令會移除 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="74519-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="74519-112">範例2：移除 blockchain 成員</span><span class="sxs-lookup"><span data-stu-id="74519-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="74519-113">這個命令會移除 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="74519-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="74519-114">參數</span><span class="sxs-lookup"><span data-stu-id="74519-114">PARAMETERS</span></span>

### <span data-ttu-id="74519-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="74519-115">-AsJob</span></span>
<span data-ttu-id="74519-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="74519-116">Run the command as a job</span></span>

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

### <span data-ttu-id="74519-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74519-117">-DefaultProfile</span></span>
<span data-ttu-id="74519-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="74519-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74519-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74519-119">-InputObject</span></span>
<span data-ttu-id="74519-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="74519-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="74519-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="74519-121">-Name</span></span>
<span data-ttu-id="74519-122">Blockchain 成員名稱</span><span class="sxs-lookup"><span data-stu-id="74519-122">Blockchain member name</span></span>

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

### <span data-ttu-id="74519-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="74519-123">-NoWait</span></span>
<span data-ttu-id="74519-124">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="74519-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="74519-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74519-125">-PassThru</span></span>
<span data-ttu-id="74519-126">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="74519-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="74519-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74519-127">-ResourceGroupName</span></span>
<span data-ttu-id="74519-128">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="74519-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="74519-129">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="74519-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="74519-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74519-130">-SubscriptionId</span></span>
<span data-ttu-id="74519-131">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="74519-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="74519-132">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="74519-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="74519-133">-確認</span><span class="sxs-lookup"><span data-stu-id="74519-133">-Confirm</span></span>
<span data-ttu-id="74519-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="74519-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74519-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74519-135">-WhatIf</span></span>
<span data-ttu-id="74519-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="74519-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74519-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="74519-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74519-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74519-138">CommonParameters</span></span>
<span data-ttu-id="74519-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="74519-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74519-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="74519-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74519-141">輸入</span><span class="sxs-lookup"><span data-stu-id="74519-141">INPUTS</span></span>

### <span data-ttu-id="74519-142">IBlockchainIdentity （Blockchain）的</span><span class="sxs-lookup"><span data-stu-id="74519-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="74519-143">輸出</span><span class="sxs-lookup"><span data-stu-id="74519-143">OUTPUTS</span></span>

### <span data-ttu-id="74519-144">System.object</span><span class="sxs-lookup"><span data-stu-id="74519-144">System.Boolean</span></span>

## <span data-ttu-id="74519-145">筆記</span><span class="sxs-lookup"><span data-stu-id="74519-145">NOTES</span></span>

<span data-ttu-id="74519-146">別名</span><span class="sxs-lookup"><span data-stu-id="74519-146">ALIASES</span></span>

<span data-ttu-id="74519-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="74519-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="74519-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="74519-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74519-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="74519-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="74519-150">INPUTOBJECT <IBlockchainIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="74519-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="74519-151">`[BlockchainMemberName <String>]`： Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="74519-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="74519-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="74519-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="74519-153">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="74519-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="74519-154">`[OperationId <String>]`：操作 Id。</span><span class="sxs-lookup"><span data-stu-id="74519-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="74519-155">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="74519-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="74519-156">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="74519-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="74519-157">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="74519-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="74519-158">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="74519-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="74519-159">`[TransactionNodeName <String>]`：交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="74519-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="74519-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="74519-160">RELATED LINKS</span></span>
