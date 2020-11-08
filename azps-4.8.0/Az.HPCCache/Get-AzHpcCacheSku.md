---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
ms.openlocfilehash: b9b9771cb5e06b4560dc436b738425288c0ad202
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971061"
---
# <span data-ttu-id="aadb7-101">Get-AzHpcCacheSku</span><span class="sxs-lookup"><span data-stu-id="aadb7-101">Get-AzHpcCacheSku</span></span>

## <span data-ttu-id="aadb7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aadb7-102">SYNOPSIS</span></span>
<span data-ttu-id="aadb7-103">取得訂閱中所有可用的 Sku。</span><span class="sxs-lookup"><span data-stu-id="aadb7-103">Gets all SKUs available in subscription.</span></span>

## <span data-ttu-id="aadb7-104">句法</span><span class="sxs-lookup"><span data-stu-id="aadb7-104">SYNTAX</span></span>

```
Get-AzHpcCacheSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aadb7-105">說明</span><span class="sxs-lookup"><span data-stu-id="aadb7-105">DESCRIPTION</span></span>
<span data-ttu-id="aadb7-106">**AzHpcCacheSku** Cmdlet 會傳回訂閱中可用的 sku 清單。</span><span class="sxs-lookup"><span data-stu-id="aadb7-106">The **Get-AzHpcCacheSku** cmdlet returns a list of SKUs available in subscription.</span></span>

## <span data-ttu-id="aadb7-107">示例</span><span class="sxs-lookup"><span data-stu-id="aadb7-107">EXAMPLES</span></span>

### <span data-ttu-id="aadb7-108">範例1</span><span class="sxs-lookup"><span data-stu-id="aadb7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheSku
```

## <span data-ttu-id="aadb7-109">參數</span><span class="sxs-lookup"><span data-stu-id="aadb7-109">PARAMETERS</span></span>

### <span data-ttu-id="aadb7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aadb7-110">-DefaultProfile</span></span>
<span data-ttu-id="aadb7-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="aadb7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aadb7-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aadb7-112">CommonParameters</span></span>
<span data-ttu-id="aadb7-113">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aadb7-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aadb7-114">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="aadb7-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aadb7-115">輸入</span><span class="sxs-lookup"><span data-stu-id="aadb7-115">INPUTS</span></span>

### <span data-ttu-id="aadb7-116">所有</span><span class="sxs-lookup"><span data-stu-id="aadb7-116">None</span></span>

## <span data-ttu-id="aadb7-117">輸出</span><span class="sxs-lookup"><span data-stu-id="aadb7-117">OUTPUTS</span></span>

### <span data-ttu-id="aadb7-118">PSSku 中的 HPCCache</span><span class="sxs-lookup"><span data-stu-id="aadb7-118">Microsoft.Azure.Commands.HPCCache.PSSku</span></span>

## <span data-ttu-id="aadb7-119">筆記</span><span class="sxs-lookup"><span data-stu-id="aadb7-119">NOTES</span></span>

## <span data-ttu-id="aadb7-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="aadb7-120">RELATED LINKS</span></span>