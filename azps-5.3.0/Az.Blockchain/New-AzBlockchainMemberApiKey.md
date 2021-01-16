---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98446739"
---
# <span data-ttu-id="3ac87-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="3ac87-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="3ac87-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3ac87-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac87-103">針對 blockchain 成員重新產生 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="3ac87-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="3ac87-104">句法</span><span class="sxs-lookup"><span data-stu-id="3ac87-104">SYNTAX</span></span>

### <span data-ttu-id="3ac87-105">RegenerateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="3ac87-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3ac87-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="3ac87-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3ac87-107">說明</span><span class="sxs-lookup"><span data-stu-id="3ac87-107">DESCRIPTION</span></span>
<span data-ttu-id="3ac87-108">針對 blockchain 成員重新產生 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="3ac87-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="3ac87-109">示例</span><span class="sxs-lookup"><span data-stu-id="3ac87-109">EXAMPLES</span></span>

### <span data-ttu-id="3ac87-110">範例1：使用名稱重新產生 blockchain 成員的 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="3ac87-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="3ac87-111">這個命令會使用名稱、資源群組，為 blockchain 成員重新產生 Api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="3ac87-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="3ac87-112">範例2：使用 idenity 重新產生 blockchain 成員的 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="3ac87-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="3ac87-113">這個命令會使用身分識別為 blockchain 成員重新產生 Api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="3ac87-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="3ac87-114">參數</span><span class="sxs-lookup"><span data-stu-id="3ac87-114">PARAMETERS</span></span>

### <span data-ttu-id="3ac87-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="3ac87-115">-BlockchainMemberName</span></span>
<span data-ttu-id="3ac87-116">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac87-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="3ac87-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ac87-117">-DefaultProfile</span></span>
<span data-ttu-id="3ac87-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3ac87-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3ac87-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ac87-119">-InputObject</span></span>
<span data-ttu-id="3ac87-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="3ac87-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3ac87-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3ac87-121">-KeyName</span></span>
<span data-ttu-id="3ac87-122">取得或設定 API 金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac87-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="3ac87-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ac87-123">-ResourceGroupName</span></span>
<span data-ttu-id="3ac87-124">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac87-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3ac87-125">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="3ac87-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3ac87-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3ac87-126">-SubscriptionId</span></span>
<span data-ttu-id="3ac87-127">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="3ac87-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3ac87-128">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3ac87-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3ac87-129">-值</span><span class="sxs-lookup"><span data-stu-id="3ac87-129">-Value</span></span>
<span data-ttu-id="3ac87-130">取得或設定 API 金鑰值。</span><span class="sxs-lookup"><span data-stu-id="3ac87-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="3ac87-131">-確認</span><span class="sxs-lookup"><span data-stu-id="3ac87-131">-Confirm</span></span>
<span data-ttu-id="3ac87-132">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3ac87-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ac87-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ac87-133">-WhatIf</span></span>
<span data-ttu-id="3ac87-134">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3ac87-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ac87-135">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3ac87-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ac87-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac87-136">CommonParameters</span></span>
<span data-ttu-id="3ac87-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3ac87-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac87-138">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3ac87-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac87-139">輸入</span><span class="sxs-lookup"><span data-stu-id="3ac87-139">INPUTS</span></span>

### <span data-ttu-id="3ac87-140">IBlockchainIdentity （Blockchain）的</span><span class="sxs-lookup"><span data-stu-id="3ac87-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="3ac87-141">輸出</span><span class="sxs-lookup"><span data-stu-id="3ac87-141">OUTPUTS</span></span>

### <span data-ttu-id="3ac87-142">IApiKey （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="3ac87-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="3ac87-143">筆記</span><span class="sxs-lookup"><span data-stu-id="3ac87-143">NOTES</span></span>

<span data-ttu-id="3ac87-144">別名</span><span class="sxs-lookup"><span data-stu-id="3ac87-144">ALIASES</span></span>

<span data-ttu-id="3ac87-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="3ac87-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3ac87-146">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="3ac87-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3ac87-147">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="3ac87-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3ac87-148">INPUTOBJECT <IBlockchainIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="3ac87-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3ac87-149">`[BlockchainMemberName <String>]`： Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac87-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="3ac87-150">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="3ac87-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3ac87-151">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac87-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="3ac87-152">`[OperationId <String>]`：操作 Id。</span><span class="sxs-lookup"><span data-stu-id="3ac87-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="3ac87-153">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac87-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3ac87-154">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="3ac87-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3ac87-155">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="3ac87-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="3ac87-156">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="3ac87-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="3ac87-157">`[TransactionNodeName <String>]`：交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="3ac87-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="3ac87-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="3ac87-158">RELATED LINKS</span></span>

