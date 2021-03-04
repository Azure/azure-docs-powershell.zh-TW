---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: 19901a3834716e1f2b04102c4904c059fab29397
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906798"
---
# <span data-ttu-id="0f743-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="0f743-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="0f743-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0f743-102">SYNOPSIS</span></span>
<span data-ttu-id="0f743-103">列出會員會員的聯合會成員。</span><span class="sxs-lookup"><span data-stu-id="0f743-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="0f743-104">語法</span><span class="sxs-lookup"><span data-stu-id="0f743-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0f743-105">描述</span><span class="sxs-lookup"><span data-stu-id="0f743-105">DESCRIPTION</span></span>
<span data-ttu-id="0f743-106">列出會員會員的聯合會成員。</span><span class="sxs-lookup"><span data-stu-id="0f743-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="0f743-107">例子</span><span class="sxs-lookup"><span data-stu-id="0f743-107">EXAMPLES</span></span>

### <span data-ttu-id="0f743-108">範例 1：列出一個進位會員的聯會成員。</span><span class="sxs-lookup"><span data-stu-id="0f743-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="0f743-109">此命令會列出一個中間體成員的聯合企業成員。</span><span class="sxs-lookup"><span data-stu-id="0f743-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="0f743-110">參數</span><span class="sxs-lookup"><span data-stu-id="0f743-110">PARAMETERS</span></span>

### <span data-ttu-id="0f743-111">-有一個產品名稱</span><span class="sxs-lookup"><span data-stu-id="0f743-111">-BlockchainMemberName</span></span>
<span data-ttu-id="0f743-112">進位成員名稱。</span><span class="sxs-lookup"><span data-stu-id="0f743-112">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f743-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f743-113">-DefaultProfile</span></span>
<span data-ttu-id="0f743-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0f743-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f743-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f743-115">-ResourceGroupName</span></span>
<span data-ttu-id="0f743-116">包含資源的資源組名。</span><span class="sxs-lookup"><span data-stu-id="0f743-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0f743-117">您可以從 Azure Resource Manager API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="0f743-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f743-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f743-118">-SubscriptionId</span></span>
<span data-ttu-id="0f743-119">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="0f743-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="0f743-120">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="0f743-120">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f743-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f743-121">CommonParameters</span></span>
<span data-ttu-id="0f743-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0f743-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f743-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0f743-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f743-124">輸入</span><span class="sxs-lookup"><span data-stu-id="0f743-124">INPUTS</span></span>

## <span data-ttu-id="0f743-125">輸出</span><span class="sxs-lookup"><span data-stu-id="0f743-125">OUTPUTS</span></span>

### <span data-ttu-id="0f743-126">Microsoft.Azure.PowerShell.Cmdlets.Azer.Models.Api20180601Preview.IConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="0f743-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="0f743-127">筆記</span><span class="sxs-lookup"><span data-stu-id="0f743-127">NOTES</span></span>

<span data-ttu-id="0f743-128">別名</span><span class="sxs-lookup"><span data-stu-id="0f743-128">ALIASES</span></span>

## <span data-ttu-id="0f743-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="0f743-129">RELATED LINKS</span></span>

