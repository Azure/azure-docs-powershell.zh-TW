---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainSku.md
ms.openlocfilehash: f3da23b4ae30860013dfd31d714177e09a9cbd89
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140997"
---
# <span data-ttu-id="32af9-101">Get-AzBlockchainSku</span><span class="sxs-lookup"><span data-stu-id="32af9-101">Get-AzBlockchainSku</span></span>

## <span data-ttu-id="32af9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="32af9-102">SYNOPSIS</span></span>
<span data-ttu-id="32af9-103">列出資源類型的 Sku。</span><span class="sxs-lookup"><span data-stu-id="32af9-103">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="32af9-104">句法</span><span class="sxs-lookup"><span data-stu-id="32af9-104">SYNTAX</span></span>

```
Get-AzBlockchainSku [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="32af9-105">說明</span><span class="sxs-lookup"><span data-stu-id="32af9-105">DESCRIPTION</span></span>
<span data-ttu-id="32af9-106">列出資源類型的 Sku。</span><span class="sxs-lookup"><span data-stu-id="32af9-106">Lists the Skus of the resource type.</span></span>

## <span data-ttu-id="32af9-107">示例</span><span class="sxs-lookup"><span data-stu-id="32af9-107">EXAMPLES</span></span>

### <span data-ttu-id="32af9-108">範例1：列出訂閱的 SKU</span><span class="sxs-lookup"><span data-stu-id="32af9-108">Example 1: List SKU for a subscription</span></span>
```powershell
PS C:\> Get-AzBlockchainSku -SubscriptionId c9cbd920-c00c-427c-852b-8aaf38badaeb

```

<span data-ttu-id="32af9-109">這個命令會列出訂閱的 SKU。</span><span class="sxs-lookup"><span data-stu-id="32af9-109">This command lists SKU for a subscription.</span></span>

## <span data-ttu-id="32af9-110">參數</span><span class="sxs-lookup"><span data-stu-id="32af9-110">PARAMETERS</span></span>

### <span data-ttu-id="32af9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32af9-111">-DefaultProfile</span></span>
<span data-ttu-id="32af9-112">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="32af9-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32af9-113">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32af9-113">-SubscriptionId</span></span>
<span data-ttu-id="32af9-114">取得唯一識別 Microsoft Azure 訂閱的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="32af9-114">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="32af9-115">訂閱識別碼是每個服務呼叫 URI 的一部分。</span><span class="sxs-lookup"><span data-stu-id="32af9-115">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="32af9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32af9-116">CommonParameters</span></span>
<span data-ttu-id="32af9-117">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="32af9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32af9-118">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="32af9-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32af9-119">輸入</span><span class="sxs-lookup"><span data-stu-id="32af9-119">INPUTS</span></span>

## <span data-ttu-id="32af9-120">輸出</span><span class="sxs-lookup"><span data-stu-id="32af9-120">OUTPUTS</span></span>

### <span data-ttu-id="32af9-121">IResourceTypeSku （Blockchain）。 Api20180601Preview。</span><span class="sxs-lookup"><span data-stu-id="32af9-121">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IResourceTypeSku</span></span>

## <span data-ttu-id="32af9-122">筆記</span><span class="sxs-lookup"><span data-stu-id="32af9-122">NOTES</span></span>

<span data-ttu-id="32af9-123">別名</span><span class="sxs-lookup"><span data-stu-id="32af9-123">ALIASES</span></span>

## <span data-ttu-id="32af9-124">相關連結</span><span class="sxs-lookup"><span data-stu-id="32af9-124">RELATED LINKS</span></span>

