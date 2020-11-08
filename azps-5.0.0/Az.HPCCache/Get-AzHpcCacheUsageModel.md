---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccacheusagemodels
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheUsageModel.md
ms.openlocfilehash: 4552de7be0f2a489aa152a922e39df623736f842
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139259"
---
# <span data-ttu-id="c9e62-101">Get-AzHpcCacheUsageModel</span><span class="sxs-lookup"><span data-stu-id="c9e62-101">Get-AzHpcCacheUsageModel</span></span>

## <span data-ttu-id="c9e62-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c9e62-102">SYNOPSIS</span></span>
<span data-ttu-id="c9e62-103">取得 NFS 儲存目標的所有 usageModels。</span><span class="sxs-lookup"><span data-stu-id="c9e62-103">Gets all usageModels for NFS Storage Target.</span></span>

## <span data-ttu-id="c9e62-104">句法</span><span class="sxs-lookup"><span data-stu-id="c9e62-104">SYNTAX</span></span>

```
Get-AzHpcCacheUsageModel [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9e62-105">說明</span><span class="sxs-lookup"><span data-stu-id="c9e62-105">DESCRIPTION</span></span>
<span data-ttu-id="c9e62-106">**AzHpcCacheUsageModel** Cmdlet 會傳回 NFS 儲存目標的使用模式清單。</span><span class="sxs-lookup"><span data-stu-id="c9e62-106">The **Get-AzHpcCacheUsageModel** cmdlet returns a list of usage models for NFS Storage Target.</span></span>

## <span data-ttu-id="c9e62-107">示例</span><span class="sxs-lookup"><span data-stu-id="c9e62-107">EXAMPLES</span></span>

### <span data-ttu-id="c9e62-108">範例1</span><span class="sxs-lookup"><span data-stu-id="c9e62-108">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheUsageModel
```

## <span data-ttu-id="c9e62-109">參數</span><span class="sxs-lookup"><span data-stu-id="c9e62-109">PARAMETERS</span></span>

### <span data-ttu-id="c9e62-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9e62-110">-DefaultProfile</span></span>
<span data-ttu-id="c9e62-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c9e62-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9e62-112">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9e62-112">CommonParameters</span></span>
<span data-ttu-id="c9e62-113">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c9e62-113">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9e62-114">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c9e62-114">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9e62-115">輸入</span><span class="sxs-lookup"><span data-stu-id="c9e62-115">INPUTS</span></span>

### <span data-ttu-id="c9e62-116">所有</span><span class="sxs-lookup"><span data-stu-id="c9e62-116">None</span></span>

## <span data-ttu-id="c9e62-117">輸出</span><span class="sxs-lookup"><span data-stu-id="c9e62-117">OUTPUTS</span></span>

### <span data-ttu-id="c9e62-118">PSHpcUsageModels （HPCCache）的</span><span class="sxs-lookup"><span data-stu-id="c9e62-118">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcUsageModels</span></span>

### <span data-ttu-id="c9e62-119">System.object</span><span class="sxs-lookup"><span data-stu-id="c9e62-119">System.Object</span></span>
## <span data-ttu-id="c9e62-120">筆記</span><span class="sxs-lookup"><span data-stu-id="c9e62-120">NOTES</span></span>

## <span data-ttu-id="c9e62-121">相關連結</span><span class="sxs-lookup"><span data-stu-id="c9e62-121">RELATED LINKS</span></span>
