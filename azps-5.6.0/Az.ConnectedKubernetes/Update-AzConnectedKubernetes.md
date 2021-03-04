---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2e0c7f11592238f11f49e82102c6d58c24f8b9fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917033"
---
# <span data-ttu-id="145cb-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="145cb-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="145cb-102">簡介</span><span class="sxs-lookup"><span data-stu-id="145cb-102">SYNOPSIS</span></span>
<span data-ttu-id="145cb-103">更新已連接之組群資源之特定屬性的 API。</span><span class="sxs-lookup"><span data-stu-id="145cb-103">API to update certain properties of the connected cluster resource.</span></span>

## <span data-ttu-id="145cb-104">語法</span><span class="sxs-lookup"><span data-stu-id="145cb-104">SYNTAX</span></span>

### <span data-ttu-id="145cb-105">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="145cb-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="145cb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="145cb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="145cb-107">描述</span><span class="sxs-lookup"><span data-stu-id="145cb-107">DESCRIPTION</span></span>
<span data-ttu-id="145cb-108">更新已連接之組群資源之特定屬性的 API。</span><span class="sxs-lookup"><span data-stu-id="145cb-108">API to update certain properties of the connected cluster resource.</span></span>

## <span data-ttu-id="145cb-109">例子</span><span class="sxs-lookup"><span data-stu-id="145cb-109">EXAMPLES</span></span>

### <span data-ttu-id="145cb-110">範例 1：更新連接的 kubernetes</span><span class="sxs-lookup"><span data-stu-id="145cb-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="145cb-111">此命令會更新已連接的庫bernetes。</span><span class="sxs-lookup"><span data-stu-id="145cb-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="145cb-112">範例 2：根據物件更新連接的kubernetes</span><span class="sxs-lookup"><span data-stu-id="145cb-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="145cb-113">此命令會更新按物件連接的kubernetes。</span><span class="sxs-lookup"><span data-stu-id="145cb-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="145cb-114">參數</span><span class="sxs-lookup"><span data-stu-id="145cb-114">PARAMETERS</span></span>

### <span data-ttu-id="145cb-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="145cb-115">-ClusterName</span></span>
<span data-ttu-id="145cb-116">稱為Kubernetes 組名的組名。</span><span class="sxs-lookup"><span data-stu-id="145cb-116">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="145cb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="145cb-117">-DefaultProfile</span></span>
<span data-ttu-id="145cb-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="145cb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="145cb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="145cb-119">-InputObject</span></span>
<span data-ttu-id="145cb-120">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="145cb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="145cb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="145cb-121">-ResourceGroupName</span></span>
<span data-ttu-id="145cb-122">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="145cb-122">The name of the resource group.</span></span>
<span data-ttu-id="145cb-123">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="145cb-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="145cb-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="145cb-124">-SubscriptionId</span></span>
<span data-ttu-id="145cb-125">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="145cb-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="145cb-126">-標記</span><span class="sxs-lookup"><span data-stu-id="145cb-126">-Tag</span></span>
<span data-ttu-id="145cb-127">資源標記。</span><span class="sxs-lookup"><span data-stu-id="145cb-127">Resource tags.</span></span>

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

### <span data-ttu-id="145cb-128">-確認</span><span class="sxs-lookup"><span data-stu-id="145cb-128">-Confirm</span></span>
<span data-ttu-id="145cb-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="145cb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="145cb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="145cb-130">-WhatIf</span></span>
<span data-ttu-id="145cb-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="145cb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="145cb-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="145cb-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="145cb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="145cb-133">CommonParameters</span></span>
<span data-ttu-id="145cb-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="145cb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="145cb-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="145cb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="145cb-136">輸入</span><span class="sxs-lookup"><span data-stu-id="145cb-136">INPUTS</span></span>

### <span data-ttu-id="145cb-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="145cb-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="145cb-138">輸出</span><span class="sxs-lookup"><span data-stu-id="145cb-138">OUTPUTS</span></span>

### <span data-ttu-id="145cb-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="145cb-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="145cb-140">筆記</span><span class="sxs-lookup"><span data-stu-id="145cb-140">NOTES</span></span>

<span data-ttu-id="145cb-141">別名</span><span class="sxs-lookup"><span data-stu-id="145cb-141">ALIASES</span></span>

<span data-ttu-id="145cb-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="145cb-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="145cb-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="145cb-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="145cb-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="145cb-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="145cb-145">INPUTOBJECT： <IConnectedKubernetesIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="145cb-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="145cb-146">`[ClusterName <String>]`：稱為Kubernetes 組名。</span><span class="sxs-lookup"><span data-stu-id="145cb-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="145cb-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="145cb-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="145cb-148">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="145cb-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="145cb-149">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="145cb-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="145cb-150">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="145cb-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="145cb-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="145cb-151">RELATED LINKS</span></span>

