---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127101"
---
# <span data-ttu-id="c3b77-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="c3b77-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="c3b77-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c3b77-102">SYNOPSIS</span></span>
<span data-ttu-id="c3b77-103">用來更新已連接之群集資源之特定屬性的 API</span><span class="sxs-lookup"><span data-stu-id="c3b77-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="c3b77-104">句法</span><span class="sxs-lookup"><span data-stu-id="c3b77-104">SYNTAX</span></span>

### <span data-ttu-id="c3b77-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="c3b77-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c3b77-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c3b77-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c3b77-107">說明</span><span class="sxs-lookup"><span data-stu-id="c3b77-107">DESCRIPTION</span></span>
<span data-ttu-id="c3b77-108">用來更新已連接之群集資源之特定屬性的 API</span><span class="sxs-lookup"><span data-stu-id="c3b77-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="c3b77-109">示例</span><span class="sxs-lookup"><span data-stu-id="c3b77-109">EXAMPLES</span></span>

### <span data-ttu-id="c3b77-110">範例1：更新已連接的 kubernetes</span><span class="sxs-lookup"><span data-stu-id="c3b77-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="c3b77-111">這個命令會更新連線的 kubernetes。</span><span class="sxs-lookup"><span data-stu-id="c3b77-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="c3b77-112">範例2：依物件更新連線的 kubernetes</span><span class="sxs-lookup"><span data-stu-id="c3b77-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="c3b77-113">這個命令會依物件更新連線的 kubernetes。</span><span class="sxs-lookup"><span data-stu-id="c3b77-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="c3b77-114">參數</span><span class="sxs-lookup"><span data-stu-id="c3b77-114">PARAMETERS</span></span>

### <span data-ttu-id="c3b77-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c3b77-115">-ClusterName</span></span>
<span data-ttu-id="c3b77-116">呼叫取得之 Kubernetes 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3b77-116">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b77-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3b77-117">-DefaultProfile</span></span>
<span data-ttu-id="c3b77-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c3b77-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3b77-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3b77-119">-InputObject</span></span>
<span data-ttu-id="c3b77-120">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="c3b77-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3b77-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3b77-121">-ResourceGroupName</span></span>
<span data-ttu-id="c3b77-122">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3b77-122">The name of the resource group.</span></span>
<span data-ttu-id="c3b77-123">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c3b77-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b77-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c3b77-124">-SubscriptionId</span></span>
<span data-ttu-id="c3b77-125">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="c3b77-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b77-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="c3b77-126">-Tag</span></span>
<span data-ttu-id="c3b77-127">資源標記。</span><span class="sxs-lookup"><span data-stu-id="c3b77-127">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3b77-128">-確認</span><span class="sxs-lookup"><span data-stu-id="c3b77-128">-Confirm</span></span>
<span data-ttu-id="c3b77-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c3b77-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3b77-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3b77-130">-WhatIf</span></span>
<span data-ttu-id="c3b77-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c3b77-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3b77-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c3b77-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3b77-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3b77-133">CommonParameters</span></span>
<span data-ttu-id="c3b77-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c3b77-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3b77-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="c3b77-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3b77-136">輸入</span><span class="sxs-lookup"><span data-stu-id="c3b77-136">INPUTS</span></span>

### <span data-ttu-id="c3b77-137">IConnectedKubernetesIdentity （ConnectedKubernetes）的</span><span class="sxs-lookup"><span data-stu-id="c3b77-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="c3b77-138">輸出</span><span class="sxs-lookup"><span data-stu-id="c3b77-138">OUTPUTS</span></span>

### <span data-ttu-id="c3b77-139">IConnectedCluster （ConnectedKubernetes）。 Api202001Preview。</span><span class="sxs-lookup"><span data-stu-id="c3b77-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="c3b77-140">筆記</span><span class="sxs-lookup"><span data-stu-id="c3b77-140">NOTES</span></span>

<span data-ttu-id="c3b77-141">別名</span><span class="sxs-lookup"><span data-stu-id="c3b77-141">ALIASES</span></span>

<span data-ttu-id="c3b77-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="c3b77-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c3b77-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="c3b77-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c3b77-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="c3b77-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c3b77-145">INPUTOBJECT <IConnectedKubernetesIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="c3b77-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c3b77-146">`[ClusterName <String>]`：呼叫取得之 Kubernetes 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3b77-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="c3b77-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="c3b77-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c3b77-148">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c3b77-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c3b77-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="c3b77-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="c3b77-150">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c3b77-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="c3b77-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="c3b77-151">RELATED LINKS</span></span>

