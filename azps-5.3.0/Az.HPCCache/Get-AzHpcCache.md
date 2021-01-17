---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCache.md
ms.openlocfilehash: 82b5bdd7e10b8119a058ab3a30f6836ff9255d01
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435033"
---
# <span data-ttu-id="a1b92-101">Get-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="a1b92-101">Get-AzHpcCache</span></span>

## <span data-ttu-id="a1b92-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a1b92-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b92-103">取得 (s) 的快取。</span><span class="sxs-lookup"><span data-stu-id="a1b92-103">Gets a cache(s).</span></span>

## <span data-ttu-id="a1b92-104">句法</span><span class="sxs-lookup"><span data-stu-id="a1b92-104">SYNTAX</span></span>

```
Get-AzHpcCache [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1b92-105">說明</span><span class="sxs-lookup"><span data-stu-id="a1b92-105">DESCRIPTION</span></span>
<span data-ttu-id="a1b92-106">AzHpcCache Cmdlet 會取得單一緩存、 **快取** (s) 在特定資源群組中，或 [訂閱大量的緩存清單]。</span><span class="sxs-lookup"><span data-stu-id="a1b92-106">The **Get-AzHpcCache** cmdlet gets a single cache, cache(s) in a specific resource group, or subscription wide list of caches.</span></span>

## <span data-ttu-id="a1b92-107">示例</span><span class="sxs-lookup"><span data-stu-id="a1b92-107">EXAMPLES</span></span>

### <span data-ttu-id="a1b92-108">範例1</span><span class="sxs-lookup"><span data-stu-id="a1b92-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest -CacheName cachetest
```

### <span data-ttu-id="a1b92-109">範例2</span><span class="sxs-lookup"><span data-stu-id="a1b92-109">Example 2</span></span>
```powershell
PS C:\> Get-AzHPCCache -ResourceGroupName rgtest
```

### <span data-ttu-id="a1b92-110">範例3</span><span class="sxs-lookup"><span data-stu-id="a1b92-110">Example 3</span></span>
```powershell
PS C:\> Get-AzHPCCache
```

## <span data-ttu-id="a1b92-111">參數</span><span class="sxs-lookup"><span data-stu-id="a1b92-111">PARAMETERS</span></span>

### <span data-ttu-id="a1b92-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b92-112">-DefaultProfile</span></span>
<span data-ttu-id="a1b92-113">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a1b92-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1b92-114">-名稱</span><span class="sxs-lookup"><span data-stu-id="a1b92-114">-Name</span></span>
<span data-ttu-id="a1b92-115">特定快取的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1b92-115">Name of specific cache.</span></span>

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

### <span data-ttu-id="a1b92-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1b92-116">-ResourceGroupName</span></span>
<span data-ttu-id="a1b92-117">您想要在其中列出快取 () s 之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a1b92-117">Name of resource group under which you want to list cache(s).</span></span>

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

### <span data-ttu-id="a1b92-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b92-118">CommonParameters</span></span>
<span data-ttu-id="a1b92-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a1b92-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b92-120">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a1b92-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b92-121">輸入</span><span class="sxs-lookup"><span data-stu-id="a1b92-121">INPUTS</span></span>

### <span data-ttu-id="a1b92-122">System.object</span><span class="sxs-lookup"><span data-stu-id="a1b92-122">System.String</span></span>

## <span data-ttu-id="a1b92-123">輸出</span><span class="sxs-lookup"><span data-stu-id="a1b92-123">OUTPUTS</span></span>

### <span data-ttu-id="a1b92-124">PSHPCCache （HPCCache）的</span><span class="sxs-lookup"><span data-stu-id="a1b92-124">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="a1b92-125">筆記</span><span class="sxs-lookup"><span data-stu-id="a1b92-125">NOTES</span></span>

## <span data-ttu-id="a1b92-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="a1b92-126">RELATED LINKS</span></span>
