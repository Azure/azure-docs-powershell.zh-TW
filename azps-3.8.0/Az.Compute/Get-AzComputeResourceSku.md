---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: ab57e922a7ef63d14a36bbd91ed268822e2c61e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959633"
---
# <span data-ttu-id="39805-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="39805-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="39805-102">摘要</span><span class="sxs-lookup"><span data-stu-id="39805-102">SYNOPSIS</span></span>
<span data-ttu-id="39805-103">列出所有計算資源 Sku</span><span class="sxs-lookup"><span data-stu-id="39805-103">List all compute resource Skus</span></span>

## <span data-ttu-id="39805-104">句法</span><span class="sxs-lookup"><span data-stu-id="39805-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39805-105">說明</span><span class="sxs-lookup"><span data-stu-id="39805-105">DESCRIPTION</span></span>
<span data-ttu-id="39805-106">列出所有計算資源 Sku</span><span class="sxs-lookup"><span data-stu-id="39805-106">List all compute resource Skus</span></span>

## <span data-ttu-id="39805-107">示例</span><span class="sxs-lookup"><span data-stu-id="39805-107">EXAMPLES</span></span>

### <span data-ttu-id="39805-108">範例1</span><span class="sxs-lookup"><span data-stu-id="39805-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="39805-109">列出西部美國地區的所有計算資源 sku</span><span class="sxs-lookup"><span data-stu-id="39805-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="39805-110">參數</span><span class="sxs-lookup"><span data-stu-id="39805-110">PARAMETERS</span></span>

### <span data-ttu-id="39805-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39805-111">-DefaultProfile</span></span>
<span data-ttu-id="39805-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="39805-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39805-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39805-113">CommonParameters</span></span>
<span data-ttu-id="39805-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="39805-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39805-115">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="39805-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39805-116">輸入</span><span class="sxs-lookup"><span data-stu-id="39805-116">INPUTS</span></span>

### <span data-ttu-id="39805-117">所有</span><span class="sxs-lookup"><span data-stu-id="39805-117">None</span></span>

## <span data-ttu-id="39805-118">輸出</span><span class="sxs-lookup"><span data-stu-id="39805-118">OUTPUTS</span></span>

### <span data-ttu-id="39805-119">PSResourceSku 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="39805-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="39805-120">筆記</span><span class="sxs-lookup"><span data-stu-id="39805-120">NOTES</span></span>

## <span data-ttu-id="39805-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="39805-121">RELATED LINKS</span></span>
