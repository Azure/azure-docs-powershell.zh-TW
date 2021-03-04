---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 53178cf8e9eb38024e264aaeb2378349ba3dfa03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906789"
---
# <span data-ttu-id="3e1b3-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="3e1b3-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="3e1b3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3e1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="3e1b3-103">取得交易節點的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="3e1b3-104">語法</span><span class="sxs-lookup"><span data-stu-id="3e1b3-104">SYNTAX</span></span>

### <span data-ttu-id="3e1b3-105">清單 (預設) </span><span class="sxs-lookup"><span data-stu-id="3e1b3-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e1b3-106">獲取</span><span class="sxs-lookup"><span data-stu-id="3e1b3-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3e1b3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3e1b3-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e1b3-108">描述</span><span class="sxs-lookup"><span data-stu-id="3e1b3-108">DESCRIPTION</span></span>
<span data-ttu-id="3e1b3-109">取得交易節點的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="3e1b3-110">例子</span><span class="sxs-lookup"><span data-stu-id="3e1b3-110">EXAMPLES</span></span>

### <span data-ttu-id="3e1b3-111">範例 1：列出一個中介層成員的交易節點</span><span class="sxs-lookup"><span data-stu-id="3e1b3-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="3e1b3-112">此命令會列出位點成員的交易節點。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="3e1b3-113">範例 2：取得交易節點</span><span class="sxs-lookup"><span data-stu-id="3e1b3-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="3e1b3-114">此命令會獲得交易節點。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="3e1b3-115">範例 3：取得交易節點</span><span class="sxs-lookup"><span data-stu-id="3e1b3-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="3e1b3-116">此命令會獲得交易節點。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="3e1b3-117">參數</span><span class="sxs-lookup"><span data-stu-id="3e1b3-117">PARAMETERS</span></span>

### <span data-ttu-id="3e1b3-118">-有一個產品名稱</span><span class="sxs-lookup"><span data-stu-id="3e1b3-118">-BlockchainMemberName</span></span>
<span data-ttu-id="3e1b3-119">進位成員名稱。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-119">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e1b3-120">-DefaultProfile</span></span>
<span data-ttu-id="3e1b3-121">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e1b3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3e1b3-122">-InputObject</span></span>
<span data-ttu-id="3e1b3-123">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b3-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e1b3-124">-Name</span></span>
<span data-ttu-id="3e1b3-125">交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e1b3-126">-ResourceGroupName</span></span>
<span data-ttu-id="3e1b3-127">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3e1b3-128">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b3-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e1b3-129">-SubscriptionId</span></span>
<span data-ttu-id="3e1b3-130">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3e1b3-131">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-131">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e1b3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e1b3-132">CommonParameters</span></span>
<span data-ttu-id="3e1b3-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e1b3-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e1b3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e1b3-135">輸入</span><span class="sxs-lookup"><span data-stu-id="3e1b3-135">INPUTS</span></span>

### <span data-ttu-id="3e1b3-136">Microsoft.Azure.PowerShell.Cmdlets.Ident.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="3e1b3-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="3e1b3-137">輸出</span><span class="sxs-lookup"><span data-stu-id="3e1b3-137">OUTPUTS</span></span>

### <span data-ttu-id="3e1b3-138">Microsoft.Azure.PowerShell.Cmdlets.Azure.Models.Api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="3e1b3-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="3e1b3-139">筆記</span><span class="sxs-lookup"><span data-stu-id="3e1b3-139">NOTES</span></span>

<span data-ttu-id="3e1b3-140">別名</span><span class="sxs-lookup"><span data-stu-id="3e1b3-140">ALIASES</span></span>

<span data-ttu-id="3e1b3-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3e1b3-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3e1b3-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3e1b3-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3e1b3-144">INPUTOBJECT： <IBlockchainIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3e1b3-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3e1b3-145">`[BlockchainMemberName <String>]`：進位會員名稱。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="3e1b3-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="3e1b3-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3e1b3-147">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="3e1b3-148">`[OperationId <String>]`：操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="3e1b3-149">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3e1b3-150">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3e1b3-151">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="3e1b3-152">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="3e1b3-153">`[TransactionNodeName <String>]`：交易處理節點名稱。</span><span class="sxs-lookup"><span data-stu-id="3e1b3-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="3e1b3-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e1b3-154">RELATED LINKS</span></span>

