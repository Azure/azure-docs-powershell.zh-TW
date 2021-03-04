---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 77b4d7800d556fc43aee4e47ebc243d006a0f484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101902642"
---
# <span data-ttu-id="31387-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="31387-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="31387-102">簡介</span><span class="sxs-lookup"><span data-stu-id="31387-102">SYNOPSIS</span></span>
<span data-ttu-id="31387-103">重新產生網路管理成員 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="31387-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="31387-104">語法</span><span class="sxs-lookup"><span data-stu-id="31387-104">SYNTAX</span></span>

### <span data-ttu-id="31387-105">重新產生Expanded (預設) </span><span class="sxs-lookup"><span data-stu-id="31387-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="31387-106">重新產生ViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="31387-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="31387-107">描述</span><span class="sxs-lookup"><span data-stu-id="31387-107">DESCRIPTION</span></span>
<span data-ttu-id="31387-108">重新產生網路管理成員 API 金鑰。</span><span class="sxs-lookup"><span data-stu-id="31387-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="31387-109">例子</span><span class="sxs-lookup"><span data-stu-id="31387-109">EXAMPLES</span></span>

### <span data-ttu-id="31387-110">範例 1：使用名稱為一位進位成員重新產生 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="31387-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="31387-111">此命令會針對使用名稱、資源群組的介面成員重新產生 Api 鍵。</span><span class="sxs-lookup"><span data-stu-id="31387-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="31387-112">範例 2：使用 idenity 為一個位成員重新產生 Api 金鑰</span><span class="sxs-lookup"><span data-stu-id="31387-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="31387-113">此命令會針對使用身分識別的介面成員重新產生 Api 金鑰。</span><span class="sxs-lookup"><span data-stu-id="31387-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="31387-114">參數</span><span class="sxs-lookup"><span data-stu-id="31387-114">PARAMETERS</span></span>

### <span data-ttu-id="31387-115">-有一個產品名稱</span><span class="sxs-lookup"><span data-stu-id="31387-115">-BlockchainMemberName</span></span>
<span data-ttu-id="31387-116">進位成員名稱。</span><span class="sxs-lookup"><span data-stu-id="31387-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="31387-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31387-117">-DefaultProfile</span></span>
<span data-ttu-id="31387-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="31387-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="31387-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31387-119">-InputObject</span></span>
<span data-ttu-id="31387-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="31387-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="31387-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="31387-121">-KeyName</span></span>
<span data-ttu-id="31387-122">獲取或設定 API 金鑰名稱。</span><span class="sxs-lookup"><span data-stu-id="31387-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="31387-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31387-123">-ResourceGroupName</span></span>
<span data-ttu-id="31387-124">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="31387-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="31387-125">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="31387-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="31387-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="31387-126">-SubscriptionId</span></span>
<span data-ttu-id="31387-127">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="31387-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="31387-128">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="31387-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="31387-129">-值</span><span class="sxs-lookup"><span data-stu-id="31387-129">-Value</span></span>
<span data-ttu-id="31387-130">獲取或設定 API 鍵值。</span><span class="sxs-lookup"><span data-stu-id="31387-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="31387-131">-確認</span><span class="sxs-lookup"><span data-stu-id="31387-131">-Confirm</span></span>
<span data-ttu-id="31387-132">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="31387-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31387-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31387-133">-WhatIf</span></span>
<span data-ttu-id="31387-134">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="31387-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31387-135">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="31387-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31387-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31387-136">CommonParameters</span></span>
<span data-ttu-id="31387-137">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="31387-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31387-138">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="31387-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31387-139">輸入</span><span class="sxs-lookup"><span data-stu-id="31387-139">INPUTS</span></span>

### <span data-ttu-id="31387-140">Microsoft.Azure.PowerShell.Cmdlets.Ident.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="31387-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="31387-141">輸出</span><span class="sxs-lookup"><span data-stu-id="31387-141">OUTPUTS</span></span>

### <span data-ttu-id="31387-142">Microsoft.Azure.PowerShell.Cmdlets.Azure.Models.Api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="31387-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="31387-143">筆記</span><span class="sxs-lookup"><span data-stu-id="31387-143">NOTES</span></span>

<span data-ttu-id="31387-144">別名</span><span class="sxs-lookup"><span data-stu-id="31387-144">ALIASES</span></span>

<span data-ttu-id="31387-145">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="31387-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="31387-146">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="31387-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="31387-147">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="31387-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="31387-148">INPUTOBJECT： <IBlockchainIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="31387-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="31387-149">`[BlockchainMemberName <String>]`：進位會員名稱。</span><span class="sxs-lookup"><span data-stu-id="31387-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="31387-150">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="31387-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="31387-151">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="31387-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="31387-152">`[OperationId <String>]`：操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="31387-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="31387-153">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="31387-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="31387-154">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="31387-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="31387-155">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="31387-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="31387-156">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="31387-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="31387-157">`[TransactionNodeName <String>]`：交易處理節點名稱。</span><span class="sxs-lookup"><span data-stu-id="31387-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="31387-158">相關連結</span><span class="sxs-lookup"><span data-stu-id="31387-158">RELATED LINKS</span></span>

