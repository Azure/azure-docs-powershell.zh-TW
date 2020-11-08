---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azaksnodepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksNodePool.md
ms.openlocfilehash: 5c690b377d658e3ebc4eddaf49d546efd503a01c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138563"
---
# <span data-ttu-id="b9a5f-101">Get-AzAksNodePool</span><span class="sxs-lookup"><span data-stu-id="b9a5f-101">Get-AzAksNodePool</span></span>

## <span data-ttu-id="b9a5f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b9a5f-102">SYNOPSIS</span></span>
<span data-ttu-id="b9a5f-103">在指定的群集中建立記事池。</span><span class="sxs-lookup"><span data-stu-id="b9a5f-103">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="b9a5f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b9a5f-104">SYNTAX</span></span>

### <span data-ttu-id="b9a5f-105">NameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="b9a5f-105">NameParameterSet (Default)</span></span>
```
Get-AzAksNodePool -ResourceGroupName <String> -ClusterName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9a5f-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9a5f-106">IdParameterSet</span></span>
```
Get-AzAksNodePool -Id <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9a5f-107">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9a5f-107">ParentObjectParameterSet</span></span>
```
Get-AzAksNodePool -ClusterObject <PSKubernetesCluster> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9a5f-108">說明</span><span class="sxs-lookup"><span data-stu-id="b9a5f-108">DESCRIPTION</span></span>
<span data-ttu-id="b9a5f-109">在指定的群集中建立記事池。</span><span class="sxs-lookup"><span data-stu-id="b9a5f-109">Create note pool in specified cluster.</span></span>

## <span data-ttu-id="b9a5f-110">示例</span><span class="sxs-lookup"><span data-stu-id="b9a5f-110">EXAMPLES</span></span>

### <span data-ttu-id="b9a5f-111">取得指定群集中的所有節點池</span><span class="sxs-lookup"><span data-stu-id="b9a5f-111">Get all node pools within specified cluster</span></span>
```powershell
PS C:\> Get-AzAksNodePool -ResourceGroupName myResourceGroup -ClusterName myCluster
```

## <span data-ttu-id="b9a5f-112">參數</span><span class="sxs-lookup"><span data-stu-id="b9a5f-112">PARAMETERS</span></span>

### <span data-ttu-id="b9a5f-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b9a5f-113">-ClusterName</span></span>
<span data-ttu-id="b9a5f-114">受管理的群集資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9a5f-114">The name of the managed cluster resource.</span></span>

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

### <span data-ttu-id="b9a5f-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="b9a5f-115">-ClusterObject</span></span>
<span data-ttu-id="b9a5f-116">群集物件。</span><span class="sxs-lookup"><span data-stu-id="b9a5f-116">The cluster object.</span></span>

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

### <span data-ttu-id="b9a5f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9a5f-117">-DefaultProfile</span></span>
<span data-ttu-id="b9a5f-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b9a5f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9a5f-119">-識別碼</span><span class="sxs-lookup"><span data-stu-id="b9a5f-119">-Id</span></span>
<span data-ttu-id="b9a5f-120">受管理的 Kubernetes 群集中的節點池 Id</span><span class="sxs-lookup"><span data-stu-id="b9a5f-120">Id of an node pool in managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="b9a5f-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="b9a5f-121">-Name</span></span>
<span data-ttu-id="b9a5f-122">節點池的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9a5f-122">The name of the node pool.</span></span>

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

### <span data-ttu-id="b9a5f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9a5f-123">-ResourceGroupName</span></span>
<span data-ttu-id="b9a5f-124">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b9a5f-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="b9a5f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9a5f-125">CommonParameters</span></span>
<span data-ttu-id="b9a5f-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b9a5f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9a5f-127">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b9a5f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9a5f-128">輸入</span><span class="sxs-lookup"><span data-stu-id="b9a5f-128">INPUTS</span></span>

### <span data-ttu-id="b9a5f-129">System.object</span><span class="sxs-lookup"><span data-stu-id="b9a5f-129">System.String</span></span>

## <span data-ttu-id="b9a5f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b9a5f-130">OUTPUTS</span></span>

### <span data-ttu-id="b9a5f-131">PSNodePool 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="b9a5f-131">Microsoft.Azure.Commands.Aks.Models.PSNodePool</span></span>

## <span data-ttu-id="b9a5f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b9a5f-132">NOTES</span></span>

## <span data-ttu-id="b9a5f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b9a5f-133">RELATED LINKS</span></span>
