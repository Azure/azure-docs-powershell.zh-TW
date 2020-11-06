---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: b9e1c42ca3a67a80a939a4e79626253b903764f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93446411"
---
# <span data-ttu-id="85c2a-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="85c2a-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="85c2a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85c2a-102">SYNOPSIS</span></span>
<span data-ttu-id="85c2a-103">列出所有計算資源 Sku</span><span class="sxs-lookup"><span data-stu-id="85c2a-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85c2a-104">句法</span><span class="sxs-lookup"><span data-stu-id="85c2a-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [<CommonParameters>]
```

## <span data-ttu-id="85c2a-105">說明</span><span class="sxs-lookup"><span data-stu-id="85c2a-105">DESCRIPTION</span></span>
<span data-ttu-id="85c2a-106">列出所有計算資源 Sku</span><span class="sxs-lookup"><span data-stu-id="85c2a-106">List all compute resource Skus</span></span>

## <span data-ttu-id="85c2a-107">示例</span><span class="sxs-lookup"><span data-stu-id="85c2a-107">EXAMPLES</span></span>

### <span data-ttu-id="85c2a-108">範例1</span><span class="sxs-lookup"><span data-stu-id="85c2a-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="85c2a-109">列出西部美國地區的所有計算資源 sku</span><span class="sxs-lookup"><span data-stu-id="85c2a-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="85c2a-110">參數</span><span class="sxs-lookup"><span data-stu-id="85c2a-110">PARAMETERS</span></span>

### <span data-ttu-id="85c2a-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c2a-111">CommonParameters</span></span>
<span data-ttu-id="85c2a-112">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85c2a-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c2a-113">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85c2a-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c2a-114">輸入</span><span class="sxs-lookup"><span data-stu-id="85c2a-114">INPUTS</span></span>

### <span data-ttu-id="85c2a-115">所有</span><span class="sxs-lookup"><span data-stu-id="85c2a-115">None</span></span>


## <span data-ttu-id="85c2a-116">輸出</span><span class="sxs-lookup"><span data-stu-id="85c2a-116">OUTPUTS</span></span>

### <span data-ttu-id="85c2a-117">System.object</span><span class="sxs-lookup"><span data-stu-id="85c2a-117">System.Object</span></span>

## <span data-ttu-id="85c2a-118">筆記</span><span class="sxs-lookup"><span data-stu-id="85c2a-118">NOTES</span></span>

## <span data-ttu-id="85c2a-119">相關連結</span><span class="sxs-lookup"><span data-stu-id="85c2a-119">RELATED LINKS</span></span>

