---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/new-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/New-AzConnectedKubernetes.md
ms.openlocfilehash: 5ee758c305a960f6a06fb72290996bbec8037ed7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971223"
---
# <span data-ttu-id="13308-101">New-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="13308-101">New-AzConnectedKubernetes</span></span>

## <span data-ttu-id="13308-102">摘要</span><span class="sxs-lookup"><span data-stu-id="13308-102">SYNOPSIS</span></span>
<span data-ttu-id="13308-103">使用 API 註冊新的 K8s 群集，進而在 ARM 中建立追蹤的資源</span><span class="sxs-lookup"><span data-stu-id="13308-103">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="13308-104">句法</span><span class="sxs-lookup"><span data-stu-id="13308-104">SYNTAX</span></span>

```
New-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> -Location <String>
 [-SubscriptionId <String>] [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="13308-105">說明</span><span class="sxs-lookup"><span data-stu-id="13308-105">DESCRIPTION</span></span>
<span data-ttu-id="13308-106">使用 API 註冊新的 K8s 群集，進而在 ARM 中建立追蹤的資源</span><span class="sxs-lookup"><span data-stu-id="13308-106">API to register a new K8s cluster and thereby create a tracked resource in ARM</span></span>

## <span data-ttu-id="13308-107">示例</span><span class="sxs-lookup"><span data-stu-id="13308-107">EXAMPLES</span></span>

### <span data-ttu-id="13308-108">範例1：建立已連接的 kubernetes</span><span class="sxs-lookup"><span data-stu-id="13308-108">Example 1: Create a connected kubernetes</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t01 -ResourceGroupName connected-aks -Location 
Location Name         Type
-------- ----         ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="13308-109">這個命令會建立已連接的 kubernetes。</span><span class="sxs-lookup"><span data-stu-id="13308-109">This command creates a connected kubernetes.</span></span>

### <span data-ttu-id="13308-110">範例1：使用參數 kubeConfig 和 kubeCoNtext 建立已連接的 kubernetes</span><span class="sxs-lookup"><span data-stu-id="13308-110">Example 1: Create a connected kubernetes with parameters kubeConfig and kubeContext</span></span>
```powershell
PS C:\> New-AzConnectedKubernetes -ClusterName ps-connaks-t02 -ResourceGroupName connected-aks -Location eastus -KubeConfig $HOME\.kube\config -KubeContext portal-aks-t01

Location Name         Type
-------- ----         ----
eastus   ps-connaks-t02 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="13308-111">這個命令會建立一個連接的 kubernetes，並使用參數 kubeConfig 和 kubeCoNtext。</span><span class="sxs-lookup"><span data-stu-id="13308-111">This command creates a connected kubernetes with parameters kubeConfig and kubeContext.</span></span>

## <span data-ttu-id="13308-112">參數</span><span class="sxs-lookup"><span data-stu-id="13308-112">PARAMETERS</span></span>

### <span data-ttu-id="13308-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="13308-113">-ClusterName</span></span>
<span data-ttu-id="13308-114">呼叫取得之 Kubernetes 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="13308-114">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="13308-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13308-115">-DefaultProfile</span></span>
<span data-ttu-id="13308-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="13308-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="13308-117">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="13308-117">-KubeConfig</span></span>
<span data-ttu-id="13308-118">Kube config 檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="13308-118">Path to the kube config file</span></span>

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

### <span data-ttu-id="13308-119">-KubeCoNtext</span><span class="sxs-lookup"><span data-stu-id="13308-119">-KubeContext</span></span>
<span data-ttu-id="13308-120">從目前電腦 Kubconfig 內容</span><span class="sxs-lookup"><span data-stu-id="13308-120">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="13308-121">-位置</span><span class="sxs-lookup"><span data-stu-id="13308-121">-Location</span></span>
<span data-ttu-id="13308-122">群集的位置</span><span class="sxs-lookup"><span data-stu-id="13308-122">Location of the cluster</span></span>

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

### <span data-ttu-id="13308-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13308-123">-ResourceGroupName</span></span>
<span data-ttu-id="13308-124">Kubernetes 群集已登錄的資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="13308-124">The name of the resource group to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="13308-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="13308-125">-SubscriptionId</span></span>
<span data-ttu-id="13308-126">已登錄 kubernetes 群集的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="13308-126">The ID of the subscription to which the kubernetes cluster is registered.</span></span>

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

### <span data-ttu-id="13308-127">-確認</span><span class="sxs-lookup"><span data-stu-id="13308-127">-Confirm</span></span>
<span data-ttu-id="13308-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="13308-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13308-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13308-129">-WhatIf</span></span>
<span data-ttu-id="13308-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="13308-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13308-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="13308-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13308-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13308-132">CommonParameters</span></span>
<span data-ttu-id="13308-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="13308-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13308-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="13308-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13308-135">輸入</span><span class="sxs-lookup"><span data-stu-id="13308-135">INPUTS</span></span>

## <span data-ttu-id="13308-136">輸出</span><span class="sxs-lookup"><span data-stu-id="13308-136">OUTPUTS</span></span>

### <span data-ttu-id="13308-137">IConnectedCluster （ConnectedKubernetes）。 Api202001Preview。</span><span class="sxs-lookup"><span data-stu-id="13308-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="13308-138">筆記</span><span class="sxs-lookup"><span data-stu-id="13308-138">NOTES</span></span>

<span data-ttu-id="13308-139">別名</span><span class="sxs-lookup"><span data-stu-id="13308-139">ALIASES</span></span>

## <span data-ttu-id="13308-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="13308-140">RELATED LINKS</span></span>

