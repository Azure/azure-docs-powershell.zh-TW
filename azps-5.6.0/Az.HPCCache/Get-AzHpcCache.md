---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: c88e7d2b930eb7d04760f963a5ab8ea60ab8d455
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916946"
---
# <span data-ttu-id="bcb2d-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="bcb2d-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="bcb2d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bcb2d-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb2d-103">在 (中) 。</span><span class="sxs-lookup"><span data-stu-id="bcb2d-103">Gets a cache(s).</span></span>

## <span data-ttu-id="bcb2d-104">語法</span><span class="sxs-lookup"><span data-stu-id="bcb2d-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bcb2d-105">描述</span><span class="sxs-lookup"><span data-stu-id="bcb2d-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb2d-106">**Get-AzHpcCache** Cmdlet 會取得單一快 (、) 特定資源群組中的快件快) 或訂閱範圍的快件清單。</span><span class="sxs-lookup"><span data-stu-id="bcb2d-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="bcb2d-107">例子</span><span class="sxs-lookup"><span data-stu-id="bcb2d-107">EXAMPLES</span></span>

### <span data-ttu-id="bcb2d-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="bcb2d-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="bcb2d-109">範例 2</span><span class="sxs-lookup"><span data-stu-id="bcb2d-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="bcb2d-110">範例 3</span><span class="sxs-lookup"><span data-stu-id="bcb2d-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="bcb2d-111">參數</span><span class="sxs-lookup"><span data-stu-id="bcb2d-111">PARAMETERS</span></span>

### <span data-ttu-id="bcb2d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb2d-112">-DefaultProfile</span></span>
<span data-ttu-id="bcb2d-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bcb2d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcb2d-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="bcb2d-114">-Name</span></span>
<span data-ttu-id="bcb2d-115">特定緩存的名稱。</span><span class="sxs-lookup"><span data-stu-id="bcb2d-115">Name of specific cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb2d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb2d-116">-ResourceGroupName</span></span>
<span data-ttu-id="bcb2d-117">您想要在資源群組中列出要 () 。</span><span class="sxs-lookup"><span data-stu-id="bcb2d-117">Name of resource group under which you want to list cache(s).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb2d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb2d-118">CommonParameters</span></span>
<span data-ttu-id="bcb2d-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bcb2d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb2d-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bcb2d-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb2d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="bcb2d-121">INPUTS</span></span>

### <span data-ttu-id="bcb2d-122">System.String</span><span class="sxs-lookup"><span data-stu-id="bcb2d-122">System.String</span></span>

## <span data-ttu-id="bcb2d-123">輸出</span><span class="sxs-lookup"><span data-stu-id="bcb2d-123">OUTPUTS</span></span>

### <span data-ttu-id="bcb2d-124">Microsoft.Azure.PowerShell.Cmdlets.HPCache.models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="bcb2d-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="bcb2d-125">筆記</span><span class="sxs-lookup"><span data-stu-id="bcb2d-125">NOTES</span></span>

## <span data-ttu-id="bcb2d-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="bcb2d-126">RELATED LINKS</span></span>
