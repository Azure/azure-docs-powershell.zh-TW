---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccacheusagemodels
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
ms.openlocfilehash: 51b7297aea0378b910d647f892a252a9b2ce494b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917309"
---
# <span data-ttu-id="b6d21-101">Get-AzHpcCacheUsageModel</span><span class="sxs-lookup"><span data-stu-id="b6d21-101">Get-AzHpcCacheUsageModel</span></span>

## <span data-ttu-id="b6d21-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b6d21-102">SYNOPSIS</span></span>
<span data-ttu-id="b6d21-103">獲得所有用於 NFS 儲存目標的使用模型。</span><span class="sxs-lookup"><span data-stu-id="b6d21-103">Gets all usageModels for NFS Storage Target.</span></span>

## <span data-ttu-id="b6d21-104">語法</span><span class="sxs-lookup"><span data-stu-id="b6d21-104">SYNTAX</span></span>

```
Get-AzHpcCacheUsageModel [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6d21-105">描述</span><span class="sxs-lookup"><span data-stu-id="b6d21-105">DESCRIPTION</span></span>
<span data-ttu-id="b6d21-106">**Get-AzHpcCacheUsageModel** Cmdlet 會針對 NFS 儲存目標，會返回使用量模型清單。</span><span class="sxs-lookup"><span data-stu-id="b6d21-106">The **Get-AzHpcCacheUsageModel** cmdlet returns a list of usage models for NFS Storage Target.</span></span>

## <span data-ttu-id="b6d21-107">例子</span><span class="sxs-lookup"><span data-stu-id="b6d21-107">EXAMPLES</span></span>

### <span data-ttu-id="b6d21-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="b6d21-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheUsageModel
```

## <span data-ttu-id="b6d21-109">參數</span><span class="sxs-lookup"><span data-stu-id="b6d21-109">PARAMETERS</span></span>

### <span data-ttu-id="b6d21-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6d21-110">-DefaultProfile</span></span>
<span data-ttu-id="b6d21-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b6d21-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6d21-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6d21-112">CommonParameters</span></span>
<span data-ttu-id="b6d21-113">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b6d21-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6d21-114">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6d21-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6d21-115">輸入</span><span class="sxs-lookup"><span data-stu-id="b6d21-115">INPUTS</span></span>

### <span data-ttu-id="b6d21-116">沒有</span><span class="sxs-lookup"><span data-stu-id="b6d21-116">None</span></span>

## <span data-ttu-id="b6d21-117">輸出</span><span class="sxs-lookup"><span data-stu-id="b6d21-117">OUTPUTS</span></span>

### <span data-ttu-id="b6d21-118">Microsoft.Azure.PowerShell.Cmdlets.HPCache.models.PSHpcUsageModels</span><span class="sxs-lookup"><span data-stu-id="b6d21-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span></span>

### <span data-ttu-id="b6d21-119">System.Object</span><span class="sxs-lookup"><span data-stu-id="b6d21-119">System.Object</span></span>
## <span data-ttu-id="b6d21-120">筆記</span><span class="sxs-lookup"><span data-stu-id="b6d21-120">NOTES</span></span>

## <span data-ttu-id="b6d21-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="b6d21-121">RELATED LINKS</span></span>
