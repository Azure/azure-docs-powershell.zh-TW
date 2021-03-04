---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccachesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheSku.md
ms.openlocfilehash: 65030abcc218e501a54de4ec27a3f557e32470de
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916945"
---
# <span data-ttu-id="8ace7-101">Get-AzHpcCacheSku</span><span class="sxs-lookup"><span data-stu-id="8ace7-101">Get-AzHpcCacheSku</span></span>

## <span data-ttu-id="8ace7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8ace7-102">SYNOPSIS</span></span>
<span data-ttu-id="8ace7-103">在訂閱中獲得所有可用的 SK。</span><span class="sxs-lookup"><span data-stu-id="8ace7-103">Gets all SKUs available in subscription.</span></span>

## <span data-ttu-id="8ace7-104">語法</span><span class="sxs-lookup"><span data-stu-id="8ace7-104">SYNTAX</span></span>

```
Get-AzHpcCacheSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ace7-105">描述</span><span class="sxs-lookup"><span data-stu-id="8ace7-105">DESCRIPTION</span></span>
<span data-ttu-id="8ace7-106">**Get-AzHpcCacheSku** Cmdlet 會返回訂閱中可用的 SKU 清單。</span><span class="sxs-lookup"><span data-stu-id="8ace7-106">The **Get-AzHpcCacheSku** cmdlet returns a list of SKUs available in subscription.</span></span>

## <span data-ttu-id="8ace7-107">例子</span><span class="sxs-lookup"><span data-stu-id="8ace7-107">EXAMPLES</span></span>

### <span data-ttu-id="8ace7-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="8ace7-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheSku
```

## <span data-ttu-id="8ace7-109">參數</span><span class="sxs-lookup"><span data-stu-id="8ace7-109">PARAMETERS</span></span>

### <span data-ttu-id="8ace7-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ace7-110">-DefaultProfile</span></span>
<span data-ttu-id="8ace7-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8ace7-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ace7-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ace7-112">CommonParameters</span></span>
<span data-ttu-id="8ace7-113">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8ace7-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ace7-114">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8ace7-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ace7-115">輸入</span><span class="sxs-lookup"><span data-stu-id="8ace7-115">INPUTS</span></span>

### <span data-ttu-id="8ace7-116">沒有</span><span class="sxs-lookup"><span data-stu-id="8ace7-116">None</span></span>

## <span data-ttu-id="8ace7-117">輸出</span><span class="sxs-lookup"><span data-stu-id="8ace7-117">OUTPUTS</span></span>

### <span data-ttu-id="8ace7-118">Microsoft.Azure.Commands.HPCache.PSSku</span><span class="sxs-lookup"><span data-stu-id="8ace7-118">Microsoft.Azure.Commands.HPCCache.PSSku</span></span>

## <span data-ttu-id="8ace7-119">筆記</span><span class="sxs-lookup"><span data-stu-id="8ace7-119">NOTES</span></span>

## <span data-ttu-id="8ace7-120">相關連結</span><span class="sxs-lookup"><span data-stu-id="8ace7-120">RELATED LINKS</span></span>
