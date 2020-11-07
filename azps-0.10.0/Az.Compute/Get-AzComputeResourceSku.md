---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 751a551f5ed0a0a1968c74e5f94bcabad3b5ff32
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796321"
---
# <span data-ttu-id="4956c-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="4956c-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="4956c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4956c-102">SYNOPSIS</span></span>
<span data-ttu-id="4956c-103">列出所有計算資源 Sku</span><span class="sxs-lookup"><span data-stu-id="4956c-103">List all compute resource Skus</span></span>

## <span data-ttu-id="4956c-104">句法</span><span class="sxs-lookup"><span data-stu-id="4956c-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4956c-105">說明</span><span class="sxs-lookup"><span data-stu-id="4956c-105">DESCRIPTION</span></span>
<span data-ttu-id="4956c-106">列出所有計算資源 Sku</span><span class="sxs-lookup"><span data-stu-id="4956c-106">List all compute resource Skus</span></span>

## <span data-ttu-id="4956c-107">示例</span><span class="sxs-lookup"><span data-stu-id="4956c-107">EXAMPLES</span></span>

### <span data-ttu-id="4956c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="4956c-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="4956c-109">列出西部美國地區的所有計算資源 sku</span><span class="sxs-lookup"><span data-stu-id="4956c-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="4956c-110">參數</span><span class="sxs-lookup"><span data-stu-id="4956c-110">PARAMETERS</span></span>

### <span data-ttu-id="4956c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4956c-111">-DefaultProfile</span></span>
<span data-ttu-id="4956c-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4956c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4956c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4956c-113">CommonParameters</span></span>
<span data-ttu-id="4956c-114">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4956c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4956c-115">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4956c-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4956c-116">輸入</span><span class="sxs-lookup"><span data-stu-id="4956c-116">INPUTS</span></span>

### <span data-ttu-id="4956c-117">所有</span><span class="sxs-lookup"><span data-stu-id="4956c-117">None</span></span>

## <span data-ttu-id="4956c-118">輸出</span><span class="sxs-lookup"><span data-stu-id="4956c-118">OUTPUTS</span></span>

### <span data-ttu-id="4956c-119">System.object</span><span class="sxs-lookup"><span data-stu-id="4956c-119">System.Object</span></span>

## <span data-ttu-id="4956c-120">筆記</span><span class="sxs-lookup"><span data-stu-id="4956c-120">NOTES</span></span>

## <span data-ttu-id="4956c-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="4956c-121">RELATED LINKS</span></span>

