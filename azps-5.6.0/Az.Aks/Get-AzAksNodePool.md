---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 4d6fab247a56054b8c78914f5e47bc5737f8828f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905649"
---
# <span data-ttu-id="79c9b-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="79c9b-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="79c9b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="79c9b-102">SYNOPSIS</span></span>
<span data-ttu-id="79c9b-103">在指定的組集中建立筆記集區。</span><span class="sxs-lookup"><span data-stu-id="79c9b-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="79c9b-104">語法</span><span class="sxs-lookup"><span data-stu-id="79c9b-104">SYNTAX</span></span>

### <span data-ttu-id="79c9b-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="79c9b-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79c9b-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79c9b-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="79c9b-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79c9b-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79c9b-108">描述</span><span class="sxs-lookup"><span data-stu-id="79c9b-108">DESCRIPTION</span></span>
<span data-ttu-id="79c9b-109">在指定的組集中建立筆記集區。</span><span class="sxs-lookup"><span data-stu-id="79c9b-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="79c9b-110">例子</span><span class="sxs-lookup"><span data-stu-id="79c9b-110">EXAMPLES</span></span>

### <span data-ttu-id="79c9b-111">取得指定組內的所有節點集區</span><span class="sxs-lookup"><span data-stu-id="79c9b-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="79c9b-112">參數</span><span class="sxs-lookup"><span data-stu-id="79c9b-112">PARAMETERS</span></span>

### <span data-ttu-id="79c9b-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="79c9b-113">-ClusterName</span></span>
<span data-ttu-id="79c9b-114">受管理的組群資源名稱。</span><span class="sxs-lookup"><span data-stu-id="79c9b-114">The name of the managed cluster resource.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c9b-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="79c9b-115">-ClusterObject</span></span>
<span data-ttu-id="79c9b-116">該組物件。</span><span class="sxs-lookup"><span data-stu-id="79c9b-116">The cluster object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79c9b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c9b-117">-DefaultProfile</span></span>
<span data-ttu-id="79c9b-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="79c9b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79c9b-119">-Id</span><span class="sxs-lookup"><span data-stu-id="79c9b-119">-Id</span></span>
<span data-ttu-id="79c9b-120">受管理的 Kubernetes 集中節點集區識別碼</span><span class="sxs-lookup"><span data-stu-id="79c9b-120">Id of an node pool in managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c9b-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="79c9b-121">-Name</span></span>
<span data-ttu-id="79c9b-122">節點組名。</span><span class="sxs-lookup"><span data-stu-id="79c9b-122">The name of the node pool.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c9b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c9b-123">-ResourceGroupName</span></span>
<span data-ttu-id="79c9b-124">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="79c9b-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c9b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c9b-125">CommonParameters</span></span>
<span data-ttu-id="79c9b-126">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="79c9b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c9b-127">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79c9b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c9b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="79c9b-128">INPUTS</span></span>

### <span data-ttu-id="79c9b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="79c9b-129">System.String</span></span>

## <span data-ttu-id="79c9b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="79c9b-130">OUTPUTS</span></span>

### <span data-ttu-id="79c9b-131">Microsoft.Azure.Commands.Aks.models.PSNodePool</span><span class="sxs-lookup"><span data-stu-id="79c9b-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="79c9b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="79c9b-132">NOTES</span></span>

## <span data-ttu-id="79c9b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="79c9b-133">RELATED LINKS</span></span>
