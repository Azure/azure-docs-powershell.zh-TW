---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: da4cd54b9865cdf30487a7e49e5581474ebb2a35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917054"
---
# <span data-ttu-id="6cefe-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="6cefe-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="6cefe-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6cefe-102">SYNOPSIS</span></span>
<span data-ttu-id="6cefe-103">會返回指定之連接之組群的屬性，包括名稱、身分識別、屬性和其他組群詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6cefe-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="6cefe-104">語法</span><span class="sxs-lookup"><span data-stu-id="6cefe-104">SYNTAX</span></span>

### <span data-ttu-id="6cefe-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="6cefe-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6cefe-106">獲取</span><span class="sxs-lookup"><span data-stu-id="6cefe-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6cefe-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6cefe-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cefe-108">清單</span><span class="sxs-lookup"><span data-stu-id="6cefe-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6cefe-109">描述</span><span class="sxs-lookup"><span data-stu-id="6cefe-109">DESCRIPTION</span></span>
<span data-ttu-id="6cefe-110">會返回指定之連接之組群的屬性，包括名稱、身分識別、屬性和其他組群詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6cefe-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="6cefe-111">例子</span><span class="sxs-lookup"><span data-stu-id="6cefe-111">EXAMPLES</span></span>

### <span data-ttu-id="6cefe-112">範例 1：在訂閱下取得所有已連接的kubernetes</span><span class="sxs-lookup"><span data-stu-id="6cefe-112">Example 1: Get all connected kubernetes under a subscription</span></span>
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

<span data-ttu-id="6cefe-113">此命令會獲得訂閱下所有已連接的庫bernet。</span><span class="sxs-lookup"><span data-stu-id="6cefe-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="6cefe-114">範例 2：在資源群組下取得所有已連接的kubernetes</span><span class="sxs-lookup"><span data-stu-id="6cefe-114">Example 2: Get all connected kubernetes under the resource group</span></span>
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

<span data-ttu-id="6cefe-115">此命令會獲得資源群組下的所有已連接庫。</span><span class="sxs-lookup"><span data-stu-id="6cefe-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="6cefe-116">範例 3：取得連接的kubernetes</span><span class="sxs-lookup"><span data-stu-id="6cefe-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="6cefe-117">此命令會獲得一個連接的庫bernetes。</span><span class="sxs-lookup"><span data-stu-id="6cefe-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="6cefe-118">範例 4：取得由物件連接的kubernetes</span><span class="sxs-lookup"><span data-stu-id="6cefe-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="6cefe-119">此命令會按物件獲得已連接的kubernetes。</span><span class="sxs-lookup"><span data-stu-id="6cefe-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="6cefe-120">參數</span><span class="sxs-lookup"><span data-stu-id="6cefe-120">PARAMETERS</span></span>

### <span data-ttu-id="6cefe-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6cefe-121">-ClusterName</span></span>
<span data-ttu-id="6cefe-122">稱為Kubernetes 組名的組名。</span><span class="sxs-lookup"><span data-stu-id="6cefe-122">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="6cefe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cefe-123">-DefaultProfile</span></span>
<span data-ttu-id="6cefe-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="6cefe-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cefe-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cefe-125">-InputObject</span></span>
<span data-ttu-id="6cefe-126">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6cefe-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6cefe-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cefe-127">-ResourceGroupName</span></span>
<span data-ttu-id="6cefe-128">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cefe-128">The name of the resource group.</span></span>
<span data-ttu-id="6cefe-129">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6cefe-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6cefe-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cefe-130">-SubscriptionId</span></span>
<span data-ttu-id="6cefe-131">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6cefe-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6cefe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cefe-132">CommonParameters</span></span>
<span data-ttu-id="6cefe-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6cefe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cefe-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cefe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cefe-135">輸入</span><span class="sxs-lookup"><span data-stu-id="6cefe-135">INPUTS</span></span>

### <span data-ttu-id="6cefe-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="6cefe-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="6cefe-137">輸出</span><span class="sxs-lookup"><span data-stu-id="6cefe-137">OUTPUTS</span></span>

### <span data-ttu-id="6cefe-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="6cefe-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="6cefe-139">筆記</span><span class="sxs-lookup"><span data-stu-id="6cefe-139">NOTES</span></span>

<span data-ttu-id="6cefe-140">別名</span><span class="sxs-lookup"><span data-stu-id="6cefe-140">ALIASES</span></span>

<span data-ttu-id="6cefe-141">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="6cefe-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6cefe-142">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="6cefe-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6cefe-143">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="6cefe-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6cefe-144">INPUTOBJECT： <IConnectedKubernetesIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="6cefe-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6cefe-145">`[ClusterName <String>]`：稱為Kubernetes 組名。</span><span class="sxs-lookup"><span data-stu-id="6cefe-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="6cefe-146">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="6cefe-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6cefe-147">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6cefe-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6cefe-148">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="6cefe-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="6cefe-149">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="6cefe-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="6cefe-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="6cefe-150">RELATED LINKS</span></span>

