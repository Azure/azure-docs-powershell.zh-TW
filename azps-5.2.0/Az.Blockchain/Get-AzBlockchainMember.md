---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98280558"
---
# <span data-ttu-id="768a4-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="768a4-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="768a4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="768a4-102">SYNOPSIS</span></span>
<span data-ttu-id="768a4-103">取得 blockchain 成員的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="768a4-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="768a4-104">句法</span><span class="sxs-lookup"><span data-stu-id="768a4-104">SYNTAX</span></span>

### <span data-ttu-id="768a4-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="768a4-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="768a4-106">獲取</span><span class="sxs-lookup"><span data-stu-id="768a4-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="768a4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="768a4-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="768a4-108">清單</span><span class="sxs-lookup"><span data-stu-id="768a4-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="768a4-109">說明</span><span class="sxs-lookup"><span data-stu-id="768a4-109">DESCRIPTION</span></span>
<span data-ttu-id="768a4-110">取得 blockchain 成員的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="768a4-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="768a4-111">示例</span><span class="sxs-lookup"><span data-stu-id="768a4-111">EXAMPLES</span></span>

### <span data-ttu-id="768a4-112">範例1：清單 blockchain 成員</span><span class="sxs-lookup"><span data-stu-id="768a4-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="768a4-113">這個命令會列出訂閱下的 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="768a4-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="768a4-114">範例2：清單 blockchain 成員</span><span class="sxs-lookup"><span data-stu-id="768a4-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="768a4-115">這個命令會列出資源群組下的 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="768a4-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="768a4-116">範例3：取得 blockchain 成員</span><span class="sxs-lookup"><span data-stu-id="768a4-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="768a4-117">這個命令會在資源群組下取得 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="768a4-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="768a4-118">範例4：取得 blockchain 成員</span><span class="sxs-lookup"><span data-stu-id="768a4-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="768a4-119">這個命令會在資源群組下取得 blockchain 成員。</span><span class="sxs-lookup"><span data-stu-id="768a4-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="768a4-120">參數</span><span class="sxs-lookup"><span data-stu-id="768a4-120">PARAMETERS</span></span>

### <span data-ttu-id="768a4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="768a4-121">-DefaultProfile</span></span>
<span data-ttu-id="768a4-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="768a4-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="768a4-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="768a4-123">-InputObject</span></span>
<span data-ttu-id="768a4-124">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="768a4-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="768a4-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="768a4-125">-Name</span></span>
<span data-ttu-id="768a4-126">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="768a4-126">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="768a4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="768a4-127">-ResourceGroupName</span></span>
<span data-ttu-id="768a4-128">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="768a4-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="768a4-129">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="768a4-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="768a4-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="768a4-130">-SubscriptionId</span></span>
<span data-ttu-id="768a4-131">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="768a4-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="768a4-132">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="768a4-132">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="768a4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="768a4-133">CommonParameters</span></span>
<span data-ttu-id="768a4-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="768a4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="768a4-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="768a4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="768a4-136">輸入</span><span class="sxs-lookup"><span data-stu-id="768a4-136">INPUTS</span></span>

### <span data-ttu-id="768a4-137">IBlockchainIdentity （Blockchain）的</span><span class="sxs-lookup"><span data-stu-id="768a4-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="768a4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="768a4-138">OUTPUTS</span></span>

### <span data-ttu-id="768a4-139">IBlockchainMember （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="768a4-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="768a4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="768a4-140">NOTES</span></span>

<span data-ttu-id="768a4-141">別名</span><span class="sxs-lookup"><span data-stu-id="768a4-141">ALIASES</span></span>

<span data-ttu-id="768a4-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="768a4-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="768a4-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="768a4-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="768a4-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="768a4-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="768a4-145">INPUTOBJECT <IBlockchainIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="768a4-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="768a4-146">`[BlockchainMemberName <String>]`： Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="768a4-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="768a4-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="768a4-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="768a4-148">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="768a4-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="768a4-149">`[OperationId <String>]`：操作 Id。</span><span class="sxs-lookup"><span data-stu-id="768a4-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="768a4-150">`[ResourceGroupName <String>]`：包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="768a4-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="768a4-151">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="768a4-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="768a4-152">`[SubscriptionId <String>]`：取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="768a4-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="768a4-153">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="768a4-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="768a4-154">`[TransactionNodeName <String>]`：交易節點名稱。</span><span class="sxs-lookup"><span data-stu-id="768a4-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="768a4-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="768a4-155">RELATED LINKS</span></span>

