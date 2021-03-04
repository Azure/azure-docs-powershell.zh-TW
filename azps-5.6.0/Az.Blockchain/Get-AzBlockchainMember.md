---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 6ec33665bfa8a7f369c90c71fe9b8141682641e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904541"
---
# <span data-ttu-id="8af70-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="8af70-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="8af70-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8af70-102">SYNOPSIS</span></span>
<span data-ttu-id="8af70-103">取得有關中央管理成員的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8af70-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="8af70-104">語法</span><span class="sxs-lookup"><span data-stu-id="8af70-104">SYNTAX</span></span>

### <span data-ttu-id="8af70-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="8af70-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8af70-106">獲取</span><span class="sxs-lookup"><span data-stu-id="8af70-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8af70-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8af70-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8af70-108">清單</span><span class="sxs-lookup"><span data-stu-id="8af70-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8af70-109">描述</span><span class="sxs-lookup"><span data-stu-id="8af70-109">DESCRIPTION</span></span>
<span data-ttu-id="8af70-110">取得有關中央管理成員的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="8af70-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="8af70-111">例子</span><span class="sxs-lookup"><span data-stu-id="8af70-111">EXAMPLES</span></span>

### <span data-ttu-id="8af70-112">範例 1：列出成員</span><span class="sxs-lookup"><span data-stu-id="8af70-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="8af70-113">此命令會列出訂閱下的成員。</span><span class="sxs-lookup"><span data-stu-id="8af70-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="8af70-114">範例 2：清單成員</span><span class="sxs-lookup"><span data-stu-id="8af70-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="8af70-115">此命令會列出資源群組下的成員。</span><span class="sxs-lookup"><span data-stu-id="8af70-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="8af70-116">範例 3：取得成員</span><span class="sxs-lookup"><span data-stu-id="8af70-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="8af70-117">此命令會獲得資源群組下的一個中央管理成員。</span><span class="sxs-lookup"><span data-stu-id="8af70-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="8af70-118">範例 4：取得成員</span><span class="sxs-lookup"><span data-stu-id="8af70-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="8af70-119">此命令會獲得資源群組下的一個中央管理成員。</span><span class="sxs-lookup"><span data-stu-id="8af70-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="8af70-120">參數</span><span class="sxs-lookup"><span data-stu-id="8af70-120">PARAMETERS</span></span>

### <span data-ttu-id="8af70-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af70-121">-DefaultProfile</span></span>
<span data-ttu-id="8af70-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8af70-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8af70-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8af70-123">-InputObject</span></span>
<span data-ttu-id="8af70-124">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8af70-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8af70-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="8af70-125">-Name</span></span>
<span data-ttu-id="8af70-126">進位成員名稱。</span><span class="sxs-lookup"><span data-stu-id="8af70-126">Blockchain member name.</span></span>

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

### <span data-ttu-id="8af70-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8af70-127">-ResourceGroupName</span></span>
<span data-ttu-id="8af70-128">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8af70-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8af70-129">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="8af70-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8af70-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8af70-130">-SubscriptionId</span></span>
<span data-ttu-id="8af70-131">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8af70-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8af70-132">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8af70-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8af70-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af70-133">CommonParameters</span></span>
<span data-ttu-id="8af70-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8af70-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af70-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8af70-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af70-136">輸入</span><span class="sxs-lookup"><span data-stu-id="8af70-136">INPUTS</span></span>

### <span data-ttu-id="8af70-137">Microsoft.Azure.PowerShell.Cmdlets.Ident.Models.IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="8af70-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="8af70-138">輸出</span><span class="sxs-lookup"><span data-stu-id="8af70-138">OUTPUTS</span></span>

### <span data-ttu-id="8af70-139">Microsoft.Azure.PowerShell.Cmdlets.Azer.Models.Api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="8af70-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="8af70-140">筆記</span><span class="sxs-lookup"><span data-stu-id="8af70-140">NOTES</span></span>

<span data-ttu-id="8af70-141">別名</span><span class="sxs-lookup"><span data-stu-id="8af70-141">ALIASES</span></span>

<span data-ttu-id="8af70-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="8af70-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8af70-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="8af70-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8af70-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="8af70-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8af70-145">INPUTOBJECT： <IBlockchainIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="8af70-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8af70-146">`[BlockchainMemberName <String>]`：進位會員名稱。</span><span class="sxs-lookup"><span data-stu-id="8af70-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="8af70-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="8af70-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8af70-148">`[Location <String>]`：位置名稱。</span><span class="sxs-lookup"><span data-stu-id="8af70-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="8af70-149">`[OperationId <String>]`：操作識別碼。</span><span class="sxs-lookup"><span data-stu-id="8af70-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="8af70-150">`[ResourceGroupName <String>]`：包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="8af70-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8af70-151">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="8af70-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8af70-152">`[SubscriptionId <String>]`：獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8af70-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="8af70-153">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="8af70-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="8af70-154">`[TransactionNodeName <String>]`：交易處理節點名稱。</span><span class="sxs-lookup"><span data-stu-id="8af70-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="8af70-155">相關連結</span><span class="sxs-lookup"><span data-stu-id="8af70-155">RELATED LINKS</span></span>

