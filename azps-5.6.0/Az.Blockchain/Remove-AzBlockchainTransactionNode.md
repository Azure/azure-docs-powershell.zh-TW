---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: 3de49353a19afbce6ed8996fc5dd7cdeccca1627
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912457"
---
# <span data-ttu-id="297de-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="297de-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="297de-102">簡介</span><span class="sxs-lookup"><span data-stu-id="297de-102">SYNOPSIS</span></span>
<span data-ttu-id="297de-103">刪除交易節點。</span><span class="sxs-lookup"><span data-stu-id="297de-103">Delete the transaction node.</span></span>

## <span data-ttu-id="297de-104">語法</span><span class="sxs-lookup"><span data-stu-id="297de-104">SYNTAX</span></span>

### <span data-ttu-id="297de-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="297de-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="297de-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="297de-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="297de-107">描述</span><span class="sxs-lookup"><span data-stu-id="297de-107">DESCRIPTION</span></span>
<span data-ttu-id="297de-108">刪除交易節點。</span><span class="sxs-lookup"><span data-stu-id="297de-108">Delete the transaction node.</span></span>

## <span data-ttu-id="297de-109">例子</span><span class="sxs-lookup"><span data-stu-id="297de-109">EXAMPLES</span></span>

### <span data-ttu-id="297de-110">範例 1：移除交易節點</span><span class="sxs-lookup"><span data-stu-id="297de-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="297de-111">此命令會移除交易節點。</span><span class="sxs-lookup"><span data-stu-id="297de-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="297de-112">範例 2：移除交易節點</span><span class="sxs-lookup"><span data-stu-id="297de-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="297de-113">此命令會移除交易節點。</span><span class="sxs-lookup"><span data-stu-id="297de-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="297de-114">參數</span><span class="sxs-lookup"><span data-stu-id="297de-114">PARAMETERS</span></span>

### <span data-ttu-id="297de-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="297de-115">-AsJob</span></span>
<span data-ttu-id="297de-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="297de-116">Run the command as a job</span></span>

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

### <span data-ttu-id="297de-117">-有一個產品名稱</span><span class="sxs-lookup"><span data-stu-id="297de-117">-BlockchainMemberName</span></span>
<span data-ttu-id="297de-118">進位成員名稱。</span><span class="sxs-lookup"><span data-stu-id="297de-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="297de-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="297de-119">-DefaultProfile</span></span>
<span data-ttu-id="297de-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="297de-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="297de-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="297de-121">-InputObject</span></span>
<span data-ttu-id="297de-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="297de-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="297de-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="297de-123">-Name</span></span>
<span data-ttu-id="297de-124">交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="297de-124">Transaction node name.</span></span>

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

### <span data-ttu-id="297de-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="297de-125">-NoWait</span></span>
<span data-ttu-id="297de-126">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="297de-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="297de-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="297de-127">-PassThru</span></span>
<span data-ttu-id="297de-128">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="297de-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="297de-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="297de-129">-ResourceGroupName</span></span>
<span data-ttu-id="297de-130">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="297de-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="297de-131">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="297de-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="297de-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="297de-132">-SubscriptionId</span></span>
<span data-ttu-id="297de-133">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="297de-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="297de-134">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="297de-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="297de-135">-確認</span><span class="sxs-lookup"><span data-stu-id="297de-135">-Confirm</span></span>
<span data-ttu-id="297de-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="297de-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="297de-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="297de-137">-WhatIf</span></span>
<span data-ttu-id="297de-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="297de-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="297de-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="297de-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="297de-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="297de-140">CommonParameters</span></span>
<span data-ttu-id="297de-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="297de-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="297de-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="297de-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="297de-143">輸入</span><span class="sxs-lookup"><span data-stu-id="297de-143">INPUTS</span></span>

### <span data-ttu-id="297de-144">Microsoft.Azure.PowerShell.Cmdlets.Ident.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="297de-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="297de-145">輸出</span><span class="sxs-lookup"><span data-stu-id="297de-145">OUTPUTS</span></span>

### <span data-ttu-id="297de-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="297de-146">System.Boolean</span></span>

## <span data-ttu-id="297de-147">筆記</span><span class="sxs-lookup"><span data-stu-id="297de-147">NOTES</span></span>

<span data-ttu-id="297de-148">別名</span><span class="sxs-lookup"><span data-stu-id="297de-148">ALIASES</span></span>

<span data-ttu-id="297de-149">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="297de-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="297de-150">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="297de-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="297de-151">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="297de-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="297de-152">INPUTOBJECT： <IBlockchainIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="297de-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="297de-153">`[BlockchainMemberName <String>]`：進位會員名稱。</span><span class="sxs-lookup"><span data-stu-id="297de-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="297de-154">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="297de-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="297de-155">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="297de-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="297de-156">`[OperationId <String>]`：操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="297de-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="297de-157">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="297de-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="297de-158">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="297de-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="297de-159">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="297de-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="297de-160">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="297de-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="297de-161">`[TransactionNodeName <String>]`：交易處理節點名稱。</span><span class="sxs-lookup"><span data-stu-id="297de-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="297de-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="297de-162">RELATED LINKS</span></span>

