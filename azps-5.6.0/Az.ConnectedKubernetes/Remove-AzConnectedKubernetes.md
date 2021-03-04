---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 7abbe244e702c80f18d2c9e97236f74d60f094bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917042"
---
# <span data-ttu-id="41079-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="41079-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="41079-102">簡介</span><span class="sxs-lookup"><span data-stu-id="41079-102">SYNOPSIS</span></span>
<span data-ttu-id="41079-103">刪除已連接的組，移除 Azure Resource Manager 中的追蹤資源 (ARM) 。</span><span class="sxs-lookup"><span data-stu-id="41079-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="41079-104">語法</span><span class="sxs-lookup"><span data-stu-id="41079-104">SYNTAX</span></span>

### <span data-ttu-id="41079-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="41079-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="41079-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="41079-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="41079-107">描述</span><span class="sxs-lookup"><span data-stu-id="41079-107">DESCRIPTION</span></span>
<span data-ttu-id="41079-108">刪除已連接的組，移除 Azure Resource Manager 中的追蹤資源 (ARM) 。</span><span class="sxs-lookup"><span data-stu-id="41079-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="41079-109">例子</span><span class="sxs-lookup"><span data-stu-id="41079-109">EXAMPLES</span></span>

### <span data-ttu-id="41079-110">範例 1：移除連接的kubernetes</span><span class="sxs-lookup"><span data-stu-id="41079-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="41079-111">此命令會移除已連接的庫bernetes</span><span class="sxs-lookup"><span data-stu-id="41079-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="41079-112">範例 2：移除已連接的kubernetes by object</span><span class="sxs-lookup"><span data-stu-id="41079-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="41079-113">此命令會移除按物件連接的庫bernetes</span><span class="sxs-lookup"><span data-stu-id="41079-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="41079-114">參數</span><span class="sxs-lookup"><span data-stu-id="41079-114">PARAMETERS</span></span>

### <span data-ttu-id="41079-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41079-115">-AsJob</span></span>
<span data-ttu-id="41079-116">以工作執行命令</span><span class="sxs-lookup"><span data-stu-id="41079-116">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41079-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="41079-117">-ClusterName</span></span>
<span data-ttu-id="41079-118">稱為Kubernetes 組名的組名。</span><span class="sxs-lookup"><span data-stu-id="41079-118">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41079-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41079-119">-DefaultProfile</span></span>
<span data-ttu-id="41079-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="41079-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41079-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41079-121">-InputObject</span></span>
<span data-ttu-id="41079-122">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="41079-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41079-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="41079-123">-KubeConfig</span></span>
<span data-ttu-id="41079-124">kube 設定檔的路徑</span><span class="sxs-lookup"><span data-stu-id="41079-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="41079-125">-KubeCoNtext</span><span class="sxs-lookup"><span data-stu-id="41079-125">-KubeContext</span></span>
<span data-ttu-id="41079-126">目前電腦中的 Kubconfig 內容</span><span class="sxs-lookup"><span data-stu-id="41079-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="41079-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="41079-127">-NoWait</span></span>
<span data-ttu-id="41079-128">非同步執行命令</span><span class="sxs-lookup"><span data-stu-id="41079-128">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41079-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41079-129">-PassThru</span></span>
<span data-ttu-id="41079-130">命令成功時，會返回 True</span><span class="sxs-lookup"><span data-stu-id="41079-130">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41079-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41079-131">-ResourceGroupName</span></span>
<span data-ttu-id="41079-132">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="41079-132">The name of the resource group.</span></span>
<span data-ttu-id="41079-133">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="41079-133">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41079-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="41079-134">-SubscriptionId</span></span>
<span data-ttu-id="41079-135">目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="41079-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41079-136">-確認</span><span class="sxs-lookup"><span data-stu-id="41079-136">-Confirm</span></span>
<span data-ttu-id="41079-137">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="41079-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41079-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41079-138">-WhatIf</span></span>
<span data-ttu-id="41079-139">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41079-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41079-140">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41079-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41079-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41079-141">CommonParameters</span></span>
<span data-ttu-id="41079-142">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="41079-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41079-143">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="41079-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41079-144">輸入</span><span class="sxs-lookup"><span data-stu-id="41079-144">INPUTS</span></span>

### <span data-ttu-id="41079-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="41079-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="41079-146">輸出</span><span class="sxs-lookup"><span data-stu-id="41079-146">OUTPUTS</span></span>

### <span data-ttu-id="41079-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="41079-147">System.Boolean</span></span>

## <span data-ttu-id="41079-148">筆記</span><span class="sxs-lookup"><span data-stu-id="41079-148">NOTES</span></span>

<span data-ttu-id="41079-149">別名</span><span class="sxs-lookup"><span data-stu-id="41079-149">ALIASES</span></span>

<span data-ttu-id="41079-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="41079-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="41079-151">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="41079-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="41079-152">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="41079-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="41079-153">INPUTOBJECT： <IConnectedKubernetesIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="41079-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="41079-154">`[ClusterName <String>]`：稱為Kubernetes 組名。</span><span class="sxs-lookup"><span data-stu-id="41079-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="41079-155">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="41079-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="41079-156">`[ResourceGroupName <String>]`：資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="41079-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="41079-157">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="41079-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="41079-158">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="41079-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="41079-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="41079-159">RELATED LINKS</span></span>

