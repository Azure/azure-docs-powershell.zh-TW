---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: f6610b86f96602619f12323e7300c66ed39a9f60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917049"
---
# <span data-ttu-id="55853-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="55853-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="55853-102">簡介</span><span class="sxs-lookup"><span data-stu-id="55853-102">SYNOPSIS</span></span>
<span data-ttu-id="55853-103">API 以註冊新的 K8S 集區，進而在 ARM 中建立追蹤資源</span><span class="sxs-lookup"><span data-stu-id="55853-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="55853-104">語法</span><span class="sxs-lookup"><span data-stu-id="55853-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="55853-105">描述</span><span class="sxs-lookup"><span data-stu-id="55853-105">DESCRIPTION</span></span>
<span data-ttu-id="55853-106">API 以註冊新的 K8S 集區，進而在 ARM 中建立追蹤資源</span><span class="sxs-lookup"><span data-stu-id="55853-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="55853-107">例子</span><span class="sxs-lookup"><span data-stu-id="55853-107">EXAMPLES</span></span>

### <span data-ttu-id="55853-108">範例 1：建立連接的 kubernetes</span><span class="sxs-lookup"><span data-stu-id="55853-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="55853-109">此命令會建立一個連接的庫bernetes。</span><span class="sxs-lookup"><span data-stu-id="55853-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="55853-110">範例 1：使用 parameters kubeConfig 和 kubeCoNtext 建立連結的 kubernetes</span><span class="sxs-lookup"><span data-stu-id="55853-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="55853-111">此命令會建立具有參數 kubeConfig 和 kubeCoNtext 的已連結的kubernetes。</span><span class="sxs-lookup"><span data-stu-id="55853-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="55853-112">參數</span><span class="sxs-lookup"><span data-stu-id="55853-112">PARAMETERS</span></span>

### <span data-ttu-id="55853-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="55853-113">-ClusterName</span></span>
<span data-ttu-id="55853-114">稱為Kubernetes 組名的組名。</span><span class="sxs-lookup"><span data-stu-id="55853-114">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55853-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55853-115">-DefaultProfile</span></span>
<span data-ttu-id="55853-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="55853-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55853-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="55853-117">-KubeConfig</span></span>
<span data-ttu-id="55853-118">kube 設定檔的路徑</span><span class="sxs-lookup"><span data-stu-id="55853-118">Path to the kube config file</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55853-119">-KubeCoNtext</span><span class="sxs-lookup"><span data-stu-id="55853-119">-KubeContext</span></span>
<span data-ttu-id="55853-120">目前電腦中的 Kubconfig 內容</span><span class="sxs-lookup"><span data-stu-id="55853-120">Kubconfig context from current machine</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55853-121">-位置</span><span class="sxs-lookup"><span data-stu-id="55853-121">-Location</span></span>
<span data-ttu-id="55853-122">組的位置</span><span class="sxs-lookup"><span data-stu-id="55853-122">Location of the cluster</span></span>

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

### <span data-ttu-id="55853-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55853-123">-ResourceGroupName</span></span>
<span data-ttu-id="55853-124">已登錄 kubernetes 群組的資源組名。</span><span class="sxs-lookup"><span data-stu-id="55853-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="55853-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="55853-125">-SubscriptionId</span></span>
<span data-ttu-id="55853-126">已登錄 kubernetes cluster 的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="55853-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55853-127">-確認</span><span class="sxs-lookup"><span data-stu-id="55853-127">-Confirm</span></span>
<span data-ttu-id="55853-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="55853-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55853-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55853-129">-WhatIf</span></span>
<span data-ttu-id="55853-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="55853-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="55853-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="55853-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55853-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55853-132">CommonParameters</span></span>
<span data-ttu-id="55853-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="55853-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55853-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="55853-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55853-135">輸入</span><span class="sxs-lookup"><span data-stu-id="55853-135">INPUTS</span></span>

## <span data-ttu-id="55853-136">輸出</span><span class="sxs-lookup"><span data-stu-id="55853-136">OUTPUTS</span></span>

### <span data-ttu-id="55853-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="55853-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="55853-138">筆記</span><span class="sxs-lookup"><span data-stu-id="55853-138">NOTES</span></span>

<span data-ttu-id="55853-139">別名</span><span class="sxs-lookup"><span data-stu-id="55853-139">ALIASES</span></span>

## <span data-ttu-id="55853-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="55853-140">RELATED LINKS</span></span>

