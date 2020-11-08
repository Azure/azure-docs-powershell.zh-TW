---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 704e95cdd01291fb617a6f0c22a051daa69434d4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94129354"
---
# <span data-ttu-id="e041b-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="e041b-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="e041b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e041b-102">SYNOPSIS</span></span>
<span data-ttu-id="e041b-103">清單可用來建立受管理的 Kubernetes 群集的版本。</span><span class="sxs-lookup"><span data-stu-id="e041b-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e041b-104">句法</span><span class="sxs-lookup"><span data-stu-id="e041b-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e041b-105">說明</span><span class="sxs-lookup"><span data-stu-id="e041b-105">DESCRIPTION</span></span>
<span data-ttu-id="e041b-106">清單可用來建立受管理的 Kubernetes 群集的版本。</span><span class="sxs-lookup"><span data-stu-id="e041b-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e041b-107">示例</span><span class="sxs-lookup"><span data-stu-id="e041b-107">EXAMPLES</span></span>

### <span data-ttu-id="e041b-108">範例1</span><span class="sxs-lookup"><span data-stu-id="e041b-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="e041b-109">參數</span><span class="sxs-lookup"><span data-stu-id="e041b-109">PARAMETERS</span></span>

### <span data-ttu-id="e041b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e041b-110">-DefaultProfile</span></span>
<span data-ttu-id="e041b-111">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e041b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e041b-112">-位置</span><span class="sxs-lookup"><span data-stu-id="e041b-112">-Location</span></span>
<span data-ttu-id="e041b-113">群集的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="e041b-113">Azure location for the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e041b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e041b-114">CommonParameters</span></span>
<span data-ttu-id="e041b-115">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e041b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e041b-116">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e041b-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e041b-117">輸入</span><span class="sxs-lookup"><span data-stu-id="e041b-117">INPUTS</span></span>

### <span data-ttu-id="e041b-118">所有</span><span class="sxs-lookup"><span data-stu-id="e041b-118">None</span></span>

## <span data-ttu-id="e041b-119">輸出</span><span class="sxs-lookup"><span data-stu-id="e041b-119">OUTPUTS</span></span>

### <span data-ttu-id="e041b-120">PSOrchestratorVersionProfile 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="e041b-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="e041b-121">筆記</span><span class="sxs-lookup"><span data-stu-id="e041b-121">NOTES</span></span>

## <span data-ttu-id="e041b-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="e041b-122">RELATED LINKS</span></span>