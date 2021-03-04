---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azaksversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksVersion.md
ms.openlocfilehash: 3a46f28ad0f169f4f4f280922dff675b5e749fed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905646"
---
# <span data-ttu-id="55b93-101">Get-AzAksVersion</span><span class="sxs-lookup"><span data-stu-id="55b93-101">Get-AzAksVersion</span></span>

## <span data-ttu-id="55b93-102">簡介</span><span class="sxs-lookup"><span data-stu-id="55b93-102">SYNOPSIS</span></span>
<span data-ttu-id="55b93-103">用於建立受管理的Kubernetes 集的可用版本清單。</span><span class="sxs-lookup"><span data-stu-id="55b93-103">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="55b93-104">語法</span><span class="sxs-lookup"><span data-stu-id="55b93-104">SYNTAX</span></span>

```
Get-AzAksVersion -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55b93-105">描述</span><span class="sxs-lookup"><span data-stu-id="55b93-105">DESCRIPTION</span></span>
<span data-ttu-id="55b93-106">用於建立受管理的Kubernetes 集的可用版本清單。</span><span class="sxs-lookup"><span data-stu-id="55b93-106">List available version for creating managed Kubernetes cluster.</span></span>

## <span data-ttu-id="55b93-107">例子</span><span class="sxs-lookup"><span data-stu-id="55b93-107">EXAMPLES</span></span>

### <span data-ttu-id="55b93-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="55b93-108">Example 1</span></span>
```powershell
PS C:\> Get-AzAksVersion -Location westus
```

## <span data-ttu-id="55b93-109">參數</span><span class="sxs-lookup"><span data-stu-id="55b93-109">PARAMETERS</span></span>

### <span data-ttu-id="55b93-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55b93-110">-DefaultProfile</span></span>
<span data-ttu-id="55b93-111">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="55b93-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="55b93-112">-位置</span><span class="sxs-lookup"><span data-stu-id="55b93-112">-Location</span></span>
<span data-ttu-id="55b93-113">該組群的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="55b93-113">Azure location for the cluster.</span></span>

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

### <span data-ttu-id="55b93-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55b93-114">CommonParameters</span></span>
<span data-ttu-id="55b93-115">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="55b93-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55b93-116">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55b93-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55b93-117">輸入</span><span class="sxs-lookup"><span data-stu-id="55b93-117">INPUTS</span></span>

### <span data-ttu-id="55b93-118">沒有</span><span class="sxs-lookup"><span data-stu-id="55b93-118">None</span></span>

## <span data-ttu-id="55b93-119">輸出</span><span class="sxs-lookup"><span data-stu-id="55b93-119">OUTPUTS</span></span>

### <span data-ttu-id="55b93-120">Microsoft.Azure.Commands.Aks.models.PSOrchestratorVersionProfile</span><span class="sxs-lookup"><span data-stu-id="55b93-120">Microsoft.Azure.Commands.Aks.Models.PSOrchestratorVersionProfile</span></span>

## <span data-ttu-id="55b93-121">筆記</span><span class="sxs-lookup"><span data-stu-id="55b93-121">NOTES</span></span>

## <span data-ttu-id="55b93-122">相關連結</span><span class="sxs-lookup"><span data-stu-id="55b93-122">RELATED LINKS</span></span>
