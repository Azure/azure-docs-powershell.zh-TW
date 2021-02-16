---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127986"
---
# <span data-ttu-id="c6801-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="c6801-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="c6801-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c6801-102">SYNOPSIS</span></span>
<span data-ttu-id="c6801-103">刪除交易節點。</span><span class="sxs-lookup"><span data-stu-id="c6801-103">Delete the transaction node.</span></span>

## <span data-ttu-id="c6801-104">句法</span><span class="sxs-lookup"><span data-stu-id="c6801-104">SYNTAX</span></span>

### <span data-ttu-id="c6801-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="c6801-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c6801-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c6801-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c6801-107">說明</span><span class="sxs-lookup"><span data-stu-id="c6801-107">DESCRIPTION</span></span>
<span data-ttu-id="c6801-108">刪除交易節點。</span><span class="sxs-lookup"><span data-stu-id="c6801-108">Delete the transaction node.</span></span>

## <span data-ttu-id="c6801-109">示例</span><span class="sxs-lookup"><span data-stu-id="c6801-109">EXAMPLES</span></span>

### <span data-ttu-id="c6801-110">範例1：移除交易節點</span><span class="sxs-lookup"><span data-stu-id="c6801-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="c6801-111">這個命令會移除交易節點。</span><span class="sxs-lookup"><span data-stu-id="c6801-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="c6801-112">範例2：移除交易節點</span><span class="sxs-lookup"><span data-stu-id="c6801-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="c6801-113">這個命令會移除交易節點。</span><span class="sxs-lookup"><span data-stu-id="c6801-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="c6801-114">參數</span><span class="sxs-lookup"><span data-stu-id="c6801-114">PARAMETERS</span></span>

### <span data-ttu-id="c6801-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6801-115">-AsJob</span></span>
<span data-ttu-id="c6801-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="c6801-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c6801-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="c6801-117">-BlockchainMemberName</span></span>
<span data-ttu-id="c6801-118">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="c6801-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="c6801-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6801-119">-DefaultProfile</span></span>
<span data-ttu-id="c6801-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c6801-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6801-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6801-121">-InputObject</span></span>
<span data-ttu-id="c6801-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c6801-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c6801-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c6801-123">-Name</span></span>
<span data-ttu-id="c6801-124">交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="c6801-124">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6801-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c6801-125">-NoWait</span></span>
<span data-ttu-id="c6801-126">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="c6801-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c6801-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6801-127">-PassThru</span></span>
<span data-ttu-id="c6801-128">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="c6801-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c6801-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6801-129">-ResourceGroupName</span></span>
<span data-ttu-id="c6801-130">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6801-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c6801-131">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="c6801-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c6801-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6801-132">-SubscriptionId</span></span>
<span data-ttu-id="c6801-133">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="c6801-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c6801-134">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c6801-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c6801-135">-確認</span><span class="sxs-lookup"><span data-stu-id="c6801-135">-Confirm</span></span>
<span data-ttu-id="c6801-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c6801-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6801-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6801-137">-WhatIf</span></span>
<span data-ttu-id="c6801-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c6801-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6801-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c6801-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6801-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6801-140">CommonParameters</span></span>
<span data-ttu-id="c6801-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c6801-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6801-142">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c6801-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6801-143">輸入</span><span class="sxs-lookup"><span data-stu-id="c6801-143">INPUTS</span></span>

### <span data-ttu-id="c6801-144">IBlockchainIdentity （Blockchain）的</span><span class="sxs-lookup"><span data-stu-id="c6801-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="c6801-145">輸出</span><span class="sxs-lookup"><span data-stu-id="c6801-145">OUTPUTS</span></span>

### <span data-ttu-id="c6801-146">System.object</span><span class="sxs-lookup"><span data-stu-id="c6801-146">System.Boolean</span></span>

## <span data-ttu-id="c6801-147">筆記</span><span class="sxs-lookup"><span data-stu-id="c6801-147">NOTES</span></span>

<span data-ttu-id="c6801-148">別名</span><span class="sxs-lookup"><span data-stu-id="c6801-148">ALIASES</span></span>

<span data-ttu-id="c6801-149">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c6801-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c6801-150">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c6801-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c6801-151">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c6801-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c6801-152">INPUTOBJECT <IBlockchainIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c6801-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c6801-153">`[BlockchainMemberName <String>]`： Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="c6801-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="c6801-154">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="c6801-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c6801-155">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="c6801-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="c6801-156">`[OperationId <String>]`：操作 Id。</span><span class="sxs-lookup"><span data-stu-id="c6801-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="c6801-157">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c6801-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c6801-158">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="c6801-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c6801-159">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="c6801-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="c6801-160">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="c6801-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="c6801-161">`[TransactionNodeName <String>]`：交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="c6801-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="c6801-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="c6801-162">RELATED LINKS</span></span>

