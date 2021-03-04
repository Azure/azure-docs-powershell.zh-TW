---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 418786855833164c3f9c15dcd2716ad00c8c6d8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902641"
---
# <span data-ttu-id="b1125-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="b1125-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="b1125-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b1125-102">SYNOPSIS</span></span>
<span data-ttu-id="b1125-103">重新產生主圖形成員 API 鍵。</span><span class="sxs-lookup"><span data-stu-id="b1125-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="b1125-104">語法</span><span class="sxs-lookup"><span data-stu-id="b1125-104">SYNTAX</span></span>

### <span data-ttu-id="b1125-105">重新產生Expanded (預設) </span><span class="sxs-lookup"><span data-stu-id="b1125-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b1125-106">重新產生ViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b1125-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b1125-107">描述</span><span class="sxs-lookup"><span data-stu-id="b1125-107">DESCRIPTION</span></span>
<span data-ttu-id="b1125-108">重新產生主圖形成員 API 鍵。</span><span class="sxs-lookup"><span data-stu-id="b1125-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="b1125-109">例子</span><span class="sxs-lookup"><span data-stu-id="b1125-109">EXAMPLES</span></span>

### <span data-ttu-id="b1125-110">範例 1：使用名稱重新產生交易節點的 Api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="b1125-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="b1125-111">此命令會使用名稱、資源群組為交易節點產生 Api 鍵。</span><span class="sxs-lookup"><span data-stu-id="b1125-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="b1125-112">範例 2：重新產生事務節點的 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="b1125-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="b1125-113">此命令會針對使用 Idenity 的事務節點產生 Api 鍵。</span><span class="sxs-lookup"><span data-stu-id="b1125-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="b1125-114">參數</span><span class="sxs-lookup"><span data-stu-id="b1125-114">PARAMETERS</span></span>

### <span data-ttu-id="b1125-115">-有一個產品名稱</span><span class="sxs-lookup"><span data-stu-id="b1125-115">-BlockchainMemberName</span></span>
<span data-ttu-id="b1125-116">進位成員名稱。</span><span class="sxs-lookup"><span data-stu-id="b1125-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="b1125-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1125-117">-DefaultProfile</span></span>
<span data-ttu-id="b1125-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b1125-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1125-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b1125-119">-InputObject</span></span>
<span data-ttu-id="b1125-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b1125-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b1125-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="b1125-121">-KeyName</span></span>
<span data-ttu-id="b1125-122">獲取或設定 API 金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="b1125-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="b1125-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1125-123">-ResourceGroupName</span></span>
<span data-ttu-id="b1125-124">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b1125-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b1125-125">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="b1125-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b1125-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b1125-126">-SubscriptionId</span></span>
<span data-ttu-id="b1125-127">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1125-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b1125-128">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b1125-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b1125-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="b1125-129">-TransactionNodeName</span></span>
<span data-ttu-id="b1125-130">交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="b1125-130">Transaction node name.</span></span>

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

### <span data-ttu-id="b1125-131">-值</span><span class="sxs-lookup"><span data-stu-id="b1125-131">-Value</span></span>
<span data-ttu-id="b1125-132">獲取或設定 API 鍵值。</span><span class="sxs-lookup"><span data-stu-id="b1125-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="b1125-133">-確認</span><span class="sxs-lookup"><span data-stu-id="b1125-133">-Confirm</span></span>
<span data-ttu-id="b1125-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b1125-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1125-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1125-135">-WhatIf</span></span>
<span data-ttu-id="b1125-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b1125-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1125-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b1125-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1125-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1125-138">CommonParameters</span></span>
<span data-ttu-id="b1125-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b1125-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1125-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b1125-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1125-141">輸入</span><span class="sxs-lookup"><span data-stu-id="b1125-141">INPUTS</span></span>

### <span data-ttu-id="b1125-142">Microsoft.Azure.PowerShell.Cmdlets.Ident.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="b1125-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="b1125-143">輸出</span><span class="sxs-lookup"><span data-stu-id="b1125-143">OUTPUTS</span></span>

### <span data-ttu-id="b1125-144">Microsoft.Azure.PowerShell.Cmdlets.Azure.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="b1125-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="b1125-145">筆記</span><span class="sxs-lookup"><span data-stu-id="b1125-145">NOTES</span></span>

<span data-ttu-id="b1125-146">別名</span><span class="sxs-lookup"><span data-stu-id="b1125-146">ALIASES</span></span>

<span data-ttu-id="b1125-147">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="b1125-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1125-148">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="b1125-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1125-149">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="b1125-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1125-150">INPUTOBJECT： <IBlockchainIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="b1125-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b1125-151">`[BlockchainMemberName <String>]`：進位會員名稱。</span><span class="sxs-lookup"><span data-stu-id="b1125-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="b1125-152">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="b1125-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b1125-153">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="b1125-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="b1125-154">`[OperationId <String>]`：操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1125-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="b1125-155">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b1125-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b1125-156">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="b1125-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b1125-157">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="b1125-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="b1125-158">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="b1125-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="b1125-159">`[TransactionNodeName <String>]`：交易處理節點名稱。</span><span class="sxs-lookup"><span data-stu-id="b1125-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="b1125-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="b1125-160">RELATED LINKS</span></span>

