---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 6f39e869137996a64c5fc440ee0c2c8bb559542b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139098"
---
# <span data-ttu-id="1634a-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="1634a-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="1634a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1634a-102">SYNOPSIS</span></span>
<span data-ttu-id="1634a-103">針對 blockchain 成員重新產生 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="1634a-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="1634a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1634a-104">SYNTAX</span></span>

### <span data-ttu-id="1634a-105">RegenerateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="1634a-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1634a-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1634a-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1634a-107">說明</span><span class="sxs-lookup"><span data-stu-id="1634a-107">DESCRIPTION</span></span>
<span data-ttu-id="1634a-108">針對 blockchain 成員重新產生 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="1634a-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="1634a-109">示例</span><span class="sxs-lookup"><span data-stu-id="1634a-109">EXAMPLES</span></span>

### <span data-ttu-id="1634a-110">範例1：使用名稱重新產生事務節點的 Api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="1634a-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="1634a-111">這個命令會使用 [名稱]、[資源群組] 來產生交易處理節點的 Api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="1634a-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="1634a-112">範例2：重新產生交易節點的 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="1634a-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="1634a-113">這個命令會使用 idenity 來產生事務節點的 Api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="1634a-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="1634a-114">參數</span><span class="sxs-lookup"><span data-stu-id="1634a-114">PARAMETERS</span></span>

### <span data-ttu-id="1634a-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="1634a-115">-BlockchainMemberName</span></span>
<span data-ttu-id="1634a-116">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="1634a-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1634a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1634a-117">-DefaultProfile</span></span>
<span data-ttu-id="1634a-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1634a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1634a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1634a-119">-InputObject</span></span>
<span data-ttu-id="1634a-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="1634a-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1634a-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="1634a-121">-KeyName</span></span>
<span data-ttu-id="1634a-122">取得或設定 API 金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="1634a-122">Gets or sets the API key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1634a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1634a-123">-ResourceGroupName</span></span>
<span data-ttu-id="1634a-124">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1634a-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1634a-125">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="1634a-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1634a-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1634a-126">-SubscriptionId</span></span>
<span data-ttu-id="1634a-127">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="1634a-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1634a-128">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1634a-128">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1634a-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="1634a-129">-TransactionNodeName</span></span>
<span data-ttu-id="1634a-130">交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="1634a-130">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1634a-131">-值</span><span class="sxs-lookup"><span data-stu-id="1634a-131">-Value</span></span>
<span data-ttu-id="1634a-132">取得或設定 API 金鑰值。</span><span class="sxs-lookup"><span data-stu-id="1634a-132">Gets or sets the API key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1634a-133">-確認</span><span class="sxs-lookup"><span data-stu-id="1634a-133">-Confirm</span></span>
<span data-ttu-id="1634a-134">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1634a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1634a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1634a-135">-WhatIf</span></span>
<span data-ttu-id="1634a-136">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1634a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1634a-137">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1634a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1634a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1634a-138">CommonParameters</span></span>
<span data-ttu-id="1634a-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1634a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1634a-140">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1634a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1634a-141">輸入</span><span class="sxs-lookup"><span data-stu-id="1634a-141">INPUTS</span></span>

### <span data-ttu-id="1634a-142">IBlockchainIdentity （Blockchain）的</span><span class="sxs-lookup"><span data-stu-id="1634a-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="1634a-143">輸出</span><span class="sxs-lookup"><span data-stu-id="1634a-143">OUTPUTS</span></span>

### <span data-ttu-id="1634a-144">IApiKey （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="1634a-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="1634a-145">筆記</span><span class="sxs-lookup"><span data-stu-id="1634a-145">NOTES</span></span>

<span data-ttu-id="1634a-146">別名</span><span class="sxs-lookup"><span data-stu-id="1634a-146">ALIASES</span></span>

<span data-ttu-id="1634a-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="1634a-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1634a-148">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="1634a-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1634a-149">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="1634a-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1634a-150">INPUTOBJECT <IBlockchainIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="1634a-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1634a-151">`[BlockchainMemberName <String>]`： Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="1634a-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="1634a-152">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="1634a-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1634a-153">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="1634a-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="1634a-154">`[OperationId <String>]`：操作 Id。</span><span class="sxs-lookup"><span data-stu-id="1634a-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="1634a-155">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1634a-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="1634a-156">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="1634a-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="1634a-157">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="1634a-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="1634a-158">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1634a-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="1634a-159">`[TransactionNodeName <String>]`：交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="1634a-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="1634a-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="1634a-160">RELATED LINKS</span></span>

