---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/get-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Get-AzAksCluster.md
ms.openlocfilehash: d2702c28a4cedc0198f3fb767f0e509912269a63
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139341"
---
# <span data-ttu-id="af216-101">Get-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="af216-101">Get-AzAksCluster</span></span>

## <span data-ttu-id="af216-102">摘要</span><span class="sxs-lookup"><span data-stu-id="af216-102">SYNOPSIS</span></span>
<span data-ttu-id="af216-103">清單 Kubernetes 受管理的群集。</span><span class="sxs-lookup"><span data-stu-id="af216-103">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="af216-104">句法</span><span class="sxs-lookup"><span data-stu-id="af216-104">SYNTAX</span></span>

### <span data-ttu-id="af216-105">ResourceGroupParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="af216-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzAksCluster [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af216-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af216-106">IdParameterSet</span></span>
```
Get-AzAksCluster [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af216-107">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af216-107">NameParameterSet</span></span>
```
Get-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="af216-108">說明</span><span class="sxs-lookup"><span data-stu-id="af216-108">DESCRIPTION</span></span>
<span data-ttu-id="af216-109">清單 Kubernetes 受管理的群集。</span><span class="sxs-lookup"><span data-stu-id="af216-109">List Kubernetes managed clusters.</span></span>

## <span data-ttu-id="af216-110">示例</span><span class="sxs-lookup"><span data-stu-id="af216-110">EXAMPLES</span></span>

### <span data-ttu-id="af216-111">列出所有 Kubernetes 群集</span><span class="sxs-lookup"><span data-stu-id="af216-111">List all Kubernetes clusters</span></span>
```powershell
PS C:\> Get-AzAksCluster
```

## <span data-ttu-id="af216-112">參數</span><span class="sxs-lookup"><span data-stu-id="af216-112">PARAMETERS</span></span>

### <span data-ttu-id="af216-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af216-113">-DefaultProfile</span></span>
<span data-ttu-id="af216-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="af216-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af216-115">-識別碼</span><span class="sxs-lookup"><span data-stu-id="af216-115">-Id</span></span>
<span data-ttu-id="af216-116">受管理的 Kubernetes 群集的 Id</span><span class="sxs-lookup"><span data-stu-id="af216-116">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="af216-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="af216-117">-Name</span></span>
<span data-ttu-id="af216-118">受管理的 Kubernetes 群集的名稱</span><span class="sxs-lookup"><span data-stu-id="af216-118">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="af216-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af216-119">-ResourceGroupName</span></span>
<span data-ttu-id="af216-120">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="af216-120">Resource group name</span></span>

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

### <span data-ttu-id="af216-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af216-121">CommonParameters</span></span>
<span data-ttu-id="af216-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="af216-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af216-123">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="af216-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af216-124">輸入</span><span class="sxs-lookup"><span data-stu-id="af216-124">INPUTS</span></span>

### <span data-ttu-id="af216-125">System.object</span><span class="sxs-lookup"><span data-stu-id="af216-125">System.String</span></span>

## <span data-ttu-id="af216-126">輸出</span><span class="sxs-lookup"><span data-stu-id="af216-126">OUTPUTS</span></span>

### <span data-ttu-id="af216-127">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="af216-127">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="af216-128">筆記</span><span class="sxs-lookup"><span data-stu-id="af216-128">NOTES</span></span>

## <span data-ttu-id="af216-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="af216-129">RELATED LINKS</span></span>
