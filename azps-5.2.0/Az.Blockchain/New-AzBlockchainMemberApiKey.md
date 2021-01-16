---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98278832"
---
# <span data-ttu-id="44dc9-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="44dc9-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="44dc9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="44dc9-102">SYNOPSIS</span></span>
<span data-ttu-id="44dc9-103">針對 blockchain 成員重新產生 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="44dc9-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="44dc9-104">句法</span><span class="sxs-lookup"><span data-stu-id="44dc9-104">SYNTAX</span></span>

### <span data-ttu-id="44dc9-105">RegenerateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="44dc9-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="44dc9-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="44dc9-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44dc9-107">說明</span><span class="sxs-lookup"><span data-stu-id="44dc9-107">DESCRIPTION</span></span>
<span data-ttu-id="44dc9-108">針對 blockchain 成員重新產生 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="44dc9-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="44dc9-109">示例</span><span class="sxs-lookup"><span data-stu-id="44dc9-109">EXAMPLES</span></span>

### <span data-ttu-id="44dc9-110">範例1：使用名稱重新產生 blockchain 成員的 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="44dc9-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="44dc9-111">這個命令會使用名稱、資源群組，為 blockchain 成員重新產生 Api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="44dc9-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="44dc9-112">範例2：使用 idenity 重新產生 blockchain 成員的 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="44dc9-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="44dc9-113">這個命令會使用身分識別為 blockchain 成員重新產生 Api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="44dc9-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="44dc9-114">參數</span><span class="sxs-lookup"><span data-stu-id="44dc9-114">PARAMETERS</span></span>

### <span data-ttu-id="44dc9-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="44dc9-115">-BlockchainMemberName</span></span>
<span data-ttu-id="44dc9-116">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="44dc9-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="44dc9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44dc9-117">-DefaultProfile</span></span>
<span data-ttu-id="44dc9-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="44dc9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44dc9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44dc9-119">-InputObject</span></span>
<span data-ttu-id="44dc9-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="44dc9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="44dc9-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="44dc9-121">-KeyName</span></span>
<span data-ttu-id="44dc9-122">取得或設定 API 金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="44dc9-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="44dc9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44dc9-123">-ResourceGroupName</span></span>
<span data-ttu-id="44dc9-124">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="44dc9-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="44dc9-125">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="44dc9-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="44dc9-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44dc9-126">-SubscriptionId</span></span>
<span data-ttu-id="44dc9-127">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="44dc9-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="44dc9-128">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="44dc9-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="44dc9-129">-值</span><span class="sxs-lookup"><span data-stu-id="44dc9-129">-Value</span></span>
<span data-ttu-id="44dc9-130">取得或設定 API 金鑰值。</span><span class="sxs-lookup"><span data-stu-id="44dc9-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="44dc9-131">-確認</span><span class="sxs-lookup"><span data-stu-id="44dc9-131">-Confirm</span></span>
<span data-ttu-id="44dc9-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="44dc9-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44dc9-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44dc9-133">-WhatIf</span></span>
<span data-ttu-id="44dc9-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="44dc9-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44dc9-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="44dc9-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44dc9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44dc9-136">CommonParameters</span></span>
<span data-ttu-id="44dc9-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="44dc9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44dc9-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="44dc9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44dc9-139">輸入</span><span class="sxs-lookup"><span data-stu-id="44dc9-139">INPUTS</span></span>

### <span data-ttu-id="44dc9-140">IBlockchainIdentity （Blockchain）的</span><span class="sxs-lookup"><span data-stu-id="44dc9-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="44dc9-141">輸出</span><span class="sxs-lookup"><span data-stu-id="44dc9-141">OUTPUTS</span></span>

### <span data-ttu-id="44dc9-142">IApiKey （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="44dc9-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="44dc9-143">筆記</span><span class="sxs-lookup"><span data-stu-id="44dc9-143">NOTES</span></span>

<span data-ttu-id="44dc9-144">別名</span><span class="sxs-lookup"><span data-stu-id="44dc9-144">ALIASES</span></span>

<span data-ttu-id="44dc9-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="44dc9-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="44dc9-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="44dc9-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44dc9-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="44dc9-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="44dc9-148">INPUTOBJECT <IBlockchainIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="44dc9-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="44dc9-149">`[BlockchainMemberName <String>]`： Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="44dc9-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="44dc9-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="44dc9-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="44dc9-151">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="44dc9-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="44dc9-152">`[OperationId <String>]`：操作 Id。</span><span class="sxs-lookup"><span data-stu-id="44dc9-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="44dc9-153">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="44dc9-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="44dc9-154">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="44dc9-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="44dc9-155">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="44dc9-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="44dc9-156">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="44dc9-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="44dc9-157">`[TransactionNodeName <String>]`：交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="44dc9-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="44dc9-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="44dc9-158">RELATED LINKS</span></span>

