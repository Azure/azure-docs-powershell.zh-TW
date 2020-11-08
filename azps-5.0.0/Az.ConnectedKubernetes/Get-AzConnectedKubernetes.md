---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138199"
---
# <span data-ttu-id="038f4-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="038f4-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="038f4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="038f4-102">SYNOPSIS</span></span>
<span data-ttu-id="038f4-103">傳回指定的連線群集的屬性，包括名稱、身分識別、屬性及其他群集詳細資料。</span><span class="sxs-lookup"><span data-stu-id="038f4-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="038f4-104">句法</span><span class="sxs-lookup"><span data-stu-id="038f4-104">SYNTAX</span></span>

### <span data-ttu-id="038f4-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="038f4-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="038f4-106">獲取</span><span class="sxs-lookup"><span data-stu-id="038f4-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="038f4-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="038f4-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="038f4-108">清單</span><span class="sxs-lookup"><span data-stu-id="038f4-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="038f4-109">說明</span><span class="sxs-lookup"><span data-stu-id="038f4-109">DESCRIPTION</span></span>
<span data-ttu-id="038f4-110">傳回指定的連線群集的屬性，包括名稱、身分識別、屬性及其他群集詳細資料。</span><span class="sxs-lookup"><span data-stu-id="038f4-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="038f4-111">示例</span><span class="sxs-lookup"><span data-stu-id="038f4-111">EXAMPLES</span></span>

### <span data-ttu-id="038f4-112">範例1：取得訂閱下的所有連線 kubernetes</span><span class="sxs-lookup"><span data-stu-id="038f4-112">Example 1: Get all connected kubernetes under a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="038f4-113">這個命令會在訂閱下取得所有已連接的 kubernetes。</span><span class="sxs-lookup"><span data-stu-id="038f4-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="038f4-114">範例2：在 [資源] 群組下取得所有已連接的 kubernetes</span><span class="sxs-lookup"><span data-stu-id="038f4-114">Example 2: Get all connected kubernetes under the resource group</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="038f4-115">這個命令會取得 [資源] 群組底下所有已連接的 kubernetes。</span><span class="sxs-lookup"><span data-stu-id="038f4-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="038f4-116">範例3：取得已連接的 kubernetes</span><span class="sxs-lookup"><span data-stu-id="038f4-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="038f4-117">這個命令會取得已連接的 kubernetes。</span><span class="sxs-lookup"><span data-stu-id="038f4-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="038f4-118">範例4：透過物件取得連接的 kubernetes</span><span class="sxs-lookup"><span data-stu-id="038f4-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="038f4-119">這個命令會透過物件取得連接的 kubernetes。</span><span class="sxs-lookup"><span data-stu-id="038f4-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="038f4-120">參數</span><span class="sxs-lookup"><span data-stu-id="038f4-120">PARAMETERS</span></span>

### <span data-ttu-id="038f4-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="038f4-121">-ClusterName</span></span>
<span data-ttu-id="038f4-122">呼叫取得之 Kubernetes 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="038f4-122">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="038f4-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="038f4-123">-DefaultProfile</span></span>
<span data-ttu-id="038f4-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="038f4-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="038f4-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="038f4-125">-InputObject</span></span>
<span data-ttu-id="038f4-126">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="038f4-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="038f4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="038f4-127">-ResourceGroupName</span></span>
<span data-ttu-id="038f4-128">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="038f4-128">The name of the resource group.</span></span>
<span data-ttu-id="038f4-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="038f4-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="038f4-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="038f4-130">-SubscriptionId</span></span>
<span data-ttu-id="038f4-131">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="038f4-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="038f4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="038f4-132">CommonParameters</span></span>
<span data-ttu-id="038f4-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="038f4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="038f4-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="038f4-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="038f4-135">輸入</span><span class="sxs-lookup"><span data-stu-id="038f4-135">INPUTS</span></span>

### <span data-ttu-id="038f4-136">IConnectedKubernetesIdentity （ConnectedKubernetes）的</span><span class="sxs-lookup"><span data-stu-id="038f4-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="038f4-137">輸出</span><span class="sxs-lookup"><span data-stu-id="038f4-137">OUTPUTS</span></span>

### <span data-ttu-id="038f4-138">IConnectedCluster （ConnectedKubernetes）。 Api202001Preview。</span><span class="sxs-lookup"><span data-stu-id="038f4-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="038f4-139">筆記</span><span class="sxs-lookup"><span data-stu-id="038f4-139">NOTES</span></span>

<span data-ttu-id="038f4-140">別名</span><span class="sxs-lookup"><span data-stu-id="038f4-140">ALIASES</span></span>

<span data-ttu-id="038f4-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="038f4-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="038f4-142">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="038f4-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="038f4-143">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="038f4-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="038f4-144">INPUTOBJECT <IConnectedKubernetesIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="038f4-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="038f4-145">`[ClusterName <String>]`：呼叫取得之 Kubernetes 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="038f4-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="038f4-146">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="038f4-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="038f4-147">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="038f4-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="038f4-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="038f4-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="038f4-149">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="038f4-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="038f4-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="038f4-150">RELATED LINKS</span></span>
