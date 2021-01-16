---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278841"
---
# <span data-ttu-id="910b7-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="910b7-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="910b7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="910b7-102">SYNOPSIS</span></span>
<span data-ttu-id="910b7-103">取得交易節點的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="910b7-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="910b7-104">句法</span><span class="sxs-lookup"><span data-stu-id="910b7-104">SYNTAX</span></span>

### <span data-ttu-id="910b7-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="910b7-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="910b7-106">獲取</span><span class="sxs-lookup"><span data-stu-id="910b7-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="910b7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="910b7-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="910b7-108">說明</span><span class="sxs-lookup"><span data-stu-id="910b7-108">DESCRIPTION</span></span>
<span data-ttu-id="910b7-109">取得交易節點的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="910b7-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="910b7-110">示例</span><span class="sxs-lookup"><span data-stu-id="910b7-110">EXAMPLES</span></span>

### <span data-ttu-id="910b7-111">範例1：列出 blockchain 成員的交易節點</span><span class="sxs-lookup"><span data-stu-id="910b7-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="910b7-112">這個命令會列出 blockchain 成員的交易節點。</span><span class="sxs-lookup"><span data-stu-id="910b7-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="910b7-113">範例2：取得交易節點</span><span class="sxs-lookup"><span data-stu-id="910b7-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="910b7-114">這個命令會取得交易節點。</span><span class="sxs-lookup"><span data-stu-id="910b7-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="910b7-115">範例3：取得交易節點</span><span class="sxs-lookup"><span data-stu-id="910b7-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="910b7-116">這個命令會取得交易節點。</span><span class="sxs-lookup"><span data-stu-id="910b7-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="910b7-117">參數</span><span class="sxs-lookup"><span data-stu-id="910b7-117">PARAMETERS</span></span>

### <span data-ttu-id="910b7-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="910b7-118">-BlockchainMemberName</span></span>
<span data-ttu-id="910b7-119">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="910b7-119">Blockchain member name.</span></span>

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

### <span data-ttu-id="910b7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="910b7-120">-DefaultProfile</span></span>
<span data-ttu-id="910b7-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="910b7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="910b7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="910b7-122">-InputObject</span></span>
<span data-ttu-id="910b7-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="910b7-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="910b7-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="910b7-124">-Name</span></span>
<span data-ttu-id="910b7-125">交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="910b7-125">Transaction node name.</span></span>

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

### <span data-ttu-id="910b7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="910b7-126">-ResourceGroupName</span></span>
<span data-ttu-id="910b7-127">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="910b7-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="910b7-128">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="910b7-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="910b7-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="910b7-129">-SubscriptionId</span></span>
<span data-ttu-id="910b7-130">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="910b7-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="910b7-131">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="910b7-131">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="910b7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="910b7-132">CommonParameters</span></span>
<span data-ttu-id="910b7-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="910b7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="910b7-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="910b7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="910b7-135">輸入</span><span class="sxs-lookup"><span data-stu-id="910b7-135">INPUTS</span></span>

### <span data-ttu-id="910b7-136">IBlockchainIdentity （Blockchain）的</span><span class="sxs-lookup"><span data-stu-id="910b7-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="910b7-137">輸出</span><span class="sxs-lookup"><span data-stu-id="910b7-137">OUTPUTS</span></span>

### <span data-ttu-id="910b7-138">ITransactionNode （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="910b7-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="910b7-139">筆記</span><span class="sxs-lookup"><span data-stu-id="910b7-139">NOTES</span></span>

<span data-ttu-id="910b7-140">別名</span><span class="sxs-lookup"><span data-stu-id="910b7-140">ALIASES</span></span>

<span data-ttu-id="910b7-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="910b7-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="910b7-142">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="910b7-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="910b7-143">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="910b7-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="910b7-144">INPUTOBJECT <IBlockchainIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="910b7-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="910b7-145">`[BlockchainMemberName <String>]`： Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="910b7-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="910b7-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="910b7-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="910b7-147">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="910b7-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="910b7-148">`[OperationId <String>]`：操作 Id。</span><span class="sxs-lookup"><span data-stu-id="910b7-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="910b7-149">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="910b7-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="910b7-150">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="910b7-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="910b7-151">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="910b7-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="910b7-152">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="910b7-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="910b7-153">`[TransactionNodeName <String>]`：交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="910b7-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="910b7-154">相關連結</span><span class="sxs-lookup"><span data-stu-id="910b7-154">RELATED LINKS</span></span>

