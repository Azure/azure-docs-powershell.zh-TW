---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: 9f33eef5b9f0bd0b245c444cf869fa0ff7a0a064
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906793"
---
# <span data-ttu-id="f7bd1-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="f7bd1-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="f7bd1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f7bd1-102">SYNOPSIS</span></span>
<span data-ttu-id="f7bd1-103">列出資源類型的 SKU。</span><span class="sxs-lookup"><span data-stu-id="f7bd1-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="f7bd1-104">語法</span><span class="sxs-lookup"><span data-stu-id="f7bd1-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="f7bd1-105">描述</span><span class="sxs-lookup"><span data-stu-id="f7bd1-105">DESCRIPTION</span></span>
<span data-ttu-id="f7bd1-106">列出資源類型的 SKU。</span><span class="sxs-lookup"><span data-stu-id="f7bd1-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="f7bd1-107">例子</span><span class="sxs-lookup"><span data-stu-id="f7bd1-107">EXAMPLES</span></span>

### <span data-ttu-id="f7bd1-108">範例 1：訂閱的清單 SKU</span><span class="sxs-lookup"><span data-stu-id="f7bd1-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="f7bd1-109">此命令會列出訂閱的 SKU。</span><span class="sxs-lookup"><span data-stu-id="f7bd1-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="f7bd1-110">參數</span><span class="sxs-lookup"><span data-stu-id="f7bd1-110">PARAMETERS</span></span>

### <span data-ttu-id="f7bd1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7bd1-111">-DefaultProfile</span></span>
<span data-ttu-id="f7bd1-112">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f7bd1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7bd1-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7bd1-113">-SubscriptionId</span></span>
<span data-ttu-id="f7bd1-114">獲得可唯一識別 Microsoft Azure 訂閱的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="f7bd1-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="f7bd1-115">訂閱識別碼是每個服務通話 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="f7bd1-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f7bd1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7bd1-116">CommonParameters</span></span>
<span data-ttu-id="f7bd1-117">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f7bd1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7bd1-118">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7bd1-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7bd1-119">輸入</span><span class="sxs-lookup"><span data-stu-id="f7bd1-119">INPUTS</span></span>

## <span data-ttu-id="f7bd1-120">輸出</span><span class="sxs-lookup"><span data-stu-id="f7bd1-120">OUTPUTS</span></span>

### <span data-ttu-id="f7bd1-121">Microsoft.Azure.PowerShell.Cmdlets.Azure.Models.Api20180601Preview.IResourceTypeSku</span><span class="sxs-lookup"><span data-stu-id="f7bd1-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="f7bd1-122">筆記</span><span class="sxs-lookup"><span data-stu-id="f7bd1-122">NOTES</span></span>

<span data-ttu-id="f7bd1-123">別名</span><span class="sxs-lookup"><span data-stu-id="f7bd1-123">ALIASES</span></span>

## <span data-ttu-id="f7bd1-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7bd1-124">RELATED LINKS</span></span>

