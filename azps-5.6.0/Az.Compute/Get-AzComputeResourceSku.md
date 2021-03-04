---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e2b3dd89152b376ac12826eeb342c80486c2c39a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909861"
---
# <span data-ttu-id="58f05-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="58f05-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="58f05-102">簡介</span><span class="sxs-lookup"><span data-stu-id="58f05-102">SYNOPSIS</span></span>
<span data-ttu-id="58f05-103">列出所有計算資源 SKU</span><span class="sxs-lookup"><span data-stu-id="58f05-103">List all compute resource Skus</span></span>

## <span data-ttu-id="58f05-104">語法</span><span class="sxs-lookup"><span data-stu-id="58f05-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58f05-105">描述</span><span class="sxs-lookup"><span data-stu-id="58f05-105">DESCRIPTION</span></span>
<span data-ttu-id="58f05-106">列出所有計算資源 SKU</span><span class="sxs-lookup"><span data-stu-id="58f05-106">List all compute resource Skus</span></span>

## <span data-ttu-id="58f05-107">例子</span><span class="sxs-lookup"><span data-stu-id="58f05-107">EXAMPLES</span></span>

### <span data-ttu-id="58f05-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="58f05-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="58f05-109">列出美國西部地區的所有計算資源 SKU</span><span class="sxs-lookup"><span data-stu-id="58f05-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="58f05-110">參數</span><span class="sxs-lookup"><span data-stu-id="58f05-110">PARAMETERS</span></span>

### <span data-ttu-id="58f05-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58f05-111">-DefaultProfile</span></span>
<span data-ttu-id="58f05-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="58f05-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58f05-113">-位置</span><span class="sxs-lookup"><span data-stu-id="58f05-113">-Location</span></span>
<span data-ttu-id="58f05-114">指定要列出可用 SKU 的位置。</span><span class="sxs-lookup"><span data-stu-id="58f05-114">Specifies a location of the available skus to list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58f05-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58f05-115">CommonParameters</span></span>
<span data-ttu-id="58f05-116">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="58f05-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58f05-117">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58f05-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58f05-118">輸入</span><span class="sxs-lookup"><span data-stu-id="58f05-118">INPUTS</span></span>

### <span data-ttu-id="58f05-119">System.String</span><span class="sxs-lookup"><span data-stu-id="58f05-119">System.String</span></span>

## <span data-ttu-id="58f05-120">輸出</span><span class="sxs-lookup"><span data-stu-id="58f05-120">OUTPUTS</span></span>

### <span data-ttu-id="58f05-121">Microsoft.Azure.Commands.Compute.Automation.models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="58f05-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="58f05-122">筆記</span><span class="sxs-lookup"><span data-stu-id="58f05-122">NOTES</span></span>

## <span data-ttu-id="58f05-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="58f05-123">RELATED LINKS</span></span>
