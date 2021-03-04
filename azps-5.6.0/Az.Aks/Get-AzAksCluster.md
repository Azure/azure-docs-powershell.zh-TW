---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: 50d4dc8531f28ebb50ef562321b3974c7b50a102
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905657"
---
# <span data-ttu-id="bafa3-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="bafa3-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="bafa3-102">簡介</span><span class="sxs-lookup"><span data-stu-id="bafa3-102">SYNOPSIS</span></span>
<span data-ttu-id="bafa3-103">列出Kubernetes 受管理的集區。</span><span class="sxs-lookup"><span data-stu-id="bafa3-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="bafa3-104">語法</span><span class="sxs-lookup"><span data-stu-id="bafa3-104">SYNTAX</span></span>

### <span data-ttu-id="bafa3-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="bafa3-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bafa3-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bafa3-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bafa3-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bafa3-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bafa3-108">描述</span><span class="sxs-lookup"><span data-stu-id="bafa3-108">DESCRIPTION</span></span>
<span data-ttu-id="bafa3-109">列出Kubernetes 受管理的集區。</span><span class="sxs-lookup"><span data-stu-id="bafa3-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="bafa3-110">例子</span><span class="sxs-lookup"><span data-stu-id="bafa3-110">EXAMPLES</span></span>

### <span data-ttu-id="bafa3-111">列出所有 Kubernetes 群</span><span class="sxs-lookup"><span data-stu-id="bafa3-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="bafa3-112">參數</span><span class="sxs-lookup"><span data-stu-id="bafa3-112">PARAMETERS</span></span>

### <span data-ttu-id="bafa3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bafa3-113">-DefaultProfile</span></span>
<span data-ttu-id="bafa3-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="bafa3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bafa3-115">-Id</span><span class="sxs-lookup"><span data-stu-id="bafa3-115">-Id</span></span>
<span data-ttu-id="bafa3-116">受管理的Kubernetes 集的識別碼</span><span class="sxs-lookup"><span data-stu-id="bafa3-116">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bafa3-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="bafa3-117">-Name</span></span>
<span data-ttu-id="bafa3-118">受管理的Kubernetes 組名</span><span class="sxs-lookup"><span data-stu-id="bafa3-118">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafa3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bafa3-119">-ResourceGroupName</span></span>
<span data-ttu-id="bafa3-120">資源組名</span><span class="sxs-lookup"><span data-stu-id="bafa3-120">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bafa3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bafa3-121">CommonParameters</span></span>
<span data-ttu-id="bafa3-122">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="bafa3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bafa3-123">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bafa3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bafa3-124">輸入</span><span class="sxs-lookup"><span data-stu-id="bafa3-124">INPUTS</span></span>

### <span data-ttu-id="bafa3-125">System.String</span><span class="sxs-lookup"><span data-stu-id="bafa3-125">System.String</span></span>

## <span data-ttu-id="bafa3-126">輸出</span><span class="sxs-lookup"><span data-stu-id="bafa3-126">OUTPUTS</span></span>

### <span data-ttu-id="bafa3-127">Microsoft.Azure.Commands.Aks.models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="bafa3-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="bafa3-128">筆記</span><span class="sxs-lookup"><span data-stu-id="bafa3-128">NOTES</span></span>

## <span data-ttu-id="bafa3-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="bafa3-129">RELATED LINKS</span></span>
