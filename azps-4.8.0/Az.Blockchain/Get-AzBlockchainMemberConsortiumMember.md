---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmemberconsortiummember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMemberConsortiumMember.md
ms.openlocfilehash: f4dc342d72ce092a1f3cbd1695613fce2220661d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969931"
---
# <span data-ttu-id="1074a-101">Get-AzBlockchainMemberConsortiumMember</span><span class="sxs-lookup"><span data-stu-id="1074a-101">Get-AzBlockchainMemberConsortiumMember</span></span>

## <span data-ttu-id="1074a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1074a-102">SYNOPSIS</span></span>
<span data-ttu-id="1074a-103">列出 blockchain 成員的聯合會成員。</span><span class="sxs-lookup"><span data-stu-id="1074a-103">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="1074a-104">句法</span><span class="sxs-lookup"><span data-stu-id="1074a-104">SYNTAX</span></span>

```
Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="1074a-105">說明</span><span class="sxs-lookup"><span data-stu-id="1074a-105">DESCRIPTION</span></span>
<span data-ttu-id="1074a-106">列出 blockchain 成員的聯合會成員。</span><span class="sxs-lookup"><span data-stu-id="1074a-106">Lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="1074a-107">示例</span><span class="sxs-lookup"><span data-stu-id="1074a-107">EXAMPLES</span></span>

### <span data-ttu-id="1074a-108">範例1：列出 blockchain 成員的聯合會成員。</span><span class="sxs-lookup"><span data-stu-id="1074a-108">Example 1: Lists the consortium members for a blockchain member.</span></span>
```powershell
PS C:\> Get-AzBlockchainMemberConsortiumMember -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

DateModified          DisplayName JoinDate              Name       Role  Status SubscriptionId
------------          ----------- --------              ----       ----  ------ --------------
11/19/2019 5:14:41 AM dolauli001  11/19/2019 5:01:20 AM dolauli001 ADMIN Ready  c9cbd920-c00c-427c-852b-8aaf38badaeb
```

<span data-ttu-id="1074a-109">這個命令會列出 blockchain 成員的聯合會成員。</span><span class="sxs-lookup"><span data-stu-id="1074a-109">This command lists the consortium members for a blockchain member.</span></span>

## <span data-ttu-id="1074a-110">參數</span><span class="sxs-lookup"><span data-stu-id="1074a-110">PARAMETERS</span></span>

### <span data-ttu-id="1074a-111">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="1074a-111">-BlockchainMemberName</span></span>
<span data-ttu-id="1074a-112">Blockchain 成員名稱。</span><span class="sxs-lookup"><span data-stu-id="1074a-112">Blockchain member name.</span></span>

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

### <span data-ttu-id="1074a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1074a-113">-DefaultProfile</span></span>
<span data-ttu-id="1074a-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1074a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1074a-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1074a-115">-ResourceGroupName</span></span>
<span data-ttu-id="1074a-116">包含資源之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1074a-116">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="1074a-117">您可以從 Azure 資源管理器 API 或入口網站取得此值。</span><span class="sxs-lookup"><span data-stu-id="1074a-117">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="1074a-118">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1074a-118">-SubscriptionId</span></span>
<span data-ttu-id="1074a-119">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="1074a-119">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1074a-120">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="1074a-120">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1074a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1074a-121">CommonParameters</span></span>
<span data-ttu-id="1074a-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1074a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1074a-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="1074a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1074a-124">輸入</span><span class="sxs-lookup"><span data-stu-id="1074a-124">INPUTS</span></span>

## <span data-ttu-id="1074a-125">輸出</span><span class="sxs-lookup"><span data-stu-id="1074a-125">OUTPUTS</span></span>

### <span data-ttu-id="1074a-126">IConsortiumMember （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="1074a-126">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IConsortiumMember</span></span>

## <span data-ttu-id="1074a-127">筆記</span><span class="sxs-lookup"><span data-stu-id="1074a-127">NOTES</span></span>

<span data-ttu-id="1074a-128">別名</span><span class="sxs-lookup"><span data-stu-id="1074a-128">ALIASES</span></span>

## <span data-ttu-id="1074a-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="1074a-129">RELATED LINKS</span></span>
