---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969600"
---
# <span data-ttu-id="a697d-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="a697d-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="a697d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a697d-102">SYNOPSIS</span></span>
<span data-ttu-id="a697d-103">列出所有計算資源 Sku</span><span class="sxs-lookup"><span data-stu-id="a697d-103">List all compute resource Skus</span></span>

## <span data-ttu-id="a697d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a697d-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a697d-105">說明</span><span class="sxs-lookup"><span data-stu-id="a697d-105">DESCRIPTION</span></span>
<span data-ttu-id="a697d-106">列出所有計算資源 Sku</span><span class="sxs-lookup"><span data-stu-id="a697d-106">List all compute resource Skus</span></span>

## <span data-ttu-id="a697d-107">示例</span><span class="sxs-lookup"><span data-stu-id="a697d-107">EXAMPLES</span></span>

### <span data-ttu-id="a697d-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a697d-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="a697d-109">列出西部美國地區的所有計算資源 sku</span><span class="sxs-lookup"><span data-stu-id="a697d-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="a697d-110">參數</span><span class="sxs-lookup"><span data-stu-id="a697d-110">PARAMETERS</span></span>

### <span data-ttu-id="a697d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a697d-111">-DefaultProfile</span></span>
<span data-ttu-id="a697d-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a697d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a697d-113">-位置</span><span class="sxs-lookup"><span data-stu-id="a697d-113">-Location</span></span>
<span data-ttu-id="a697d-114">指定 [可用的 sku] 清單的位置。</span><span class="sxs-lookup"><span data-stu-id="a697d-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="a697d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a697d-115">CommonParameters</span></span>
<span data-ttu-id="a697d-116">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a697d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a697d-117">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a697d-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a697d-118">輸入</span><span class="sxs-lookup"><span data-stu-id="a697d-118">INPUTS</span></span>

### <span data-ttu-id="a697d-119">System.object</span><span class="sxs-lookup"><span data-stu-id="a697d-119">System.String</span></span>

## <span data-ttu-id="a697d-120">輸出</span><span class="sxs-lookup"><span data-stu-id="a697d-120">OUTPUTS</span></span>

### <span data-ttu-id="a697d-121">PSResourceSku 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="a697d-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="a697d-122">筆記</span><span class="sxs-lookup"><span data-stu-id="a697d-122">NOTES</span></span>

## <span data-ttu-id="a697d-123">相關連結</span><span class="sxs-lookup"><span data-stu-id="a697d-123">RELATED LINKS</span></span>
