---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/remove-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Remove-AzConnectedKubernetes.md
ms.openlocfilehash: 4bc5c82bbfb930484a4a3541e7e97b68ce9be2e1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138197"
---
# <span data-ttu-id="035cf-101">Remove-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="035cf-101">Remove-AzConnectedKubernetes</span></span>

## <span data-ttu-id="035cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="035cf-102">SYNOPSIS</span></span>
<span data-ttu-id="035cf-103">刪除連線的群集，並在 Azure 資源管理器中移除追蹤的資源 (ARM) 。</span><span class="sxs-lookup"><span data-stu-id="035cf-103">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="035cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="035cf-104">SYNTAX</span></span>

### <span data-ttu-id="035cf-105">刪除 (預設) </span><span class="sxs-lookup"><span data-stu-id="035cf-105">Delete (Default)</span></span>
```
Remove-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-KubeConfig <String>] [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="035cf-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="035cf-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-KubeConfig <String>]
 [-KubeContext <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="035cf-107">說明</span><span class="sxs-lookup"><span data-stu-id="035cf-107">DESCRIPTION</span></span>
<span data-ttu-id="035cf-108">刪除連線的群集，並在 Azure 資源管理器中移除追蹤的資源 (ARM) 。</span><span class="sxs-lookup"><span data-stu-id="035cf-108">Delete a connected cluster, removing the tracked resource in Azure Resource Manager (ARM).</span></span>

## <span data-ttu-id="035cf-109">示例</span><span class="sxs-lookup"><span data-stu-id="035cf-109">EXAMPLES</span></span>

### <span data-ttu-id="035cf-110">範例1：移除已連接的 kubernetes</span><span class="sxs-lookup"><span data-stu-id="035cf-110">Example 1: Remove a connected kubernetes</span></span>
```powershell
PS C:\> Remove-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -ClusterName ps-connaks-t01

```

<span data-ttu-id="035cf-111">這個命令會移除已連接的 kubernetes</span><span class="sxs-lookup"><span data-stu-id="035cf-111">This command removes a connected kubernetes</span></span>

### <span data-ttu-id="035cf-112">範例2：移除物件的已連接 kubernetes</span><span class="sxs-lookup"><span data-stu-id="035cf-112">Example 2: Remove a connected kubernetes by object</span></span>
```powershell
PS C:\> $connaks = Get-AzConnectedKubernetes -ResourceGroupName azureps-manual-test -Name ps-connaks-t02
PS C:\> Remove-AzConnectedKubernetes -InputObject $connaks

```

<span data-ttu-id="035cf-113">這個命令會移除依物件連接的 kubernetes</span><span class="sxs-lookup"><span data-stu-id="035cf-113">This command removes a connected kubernetes by object</span></span>

## <span data-ttu-id="035cf-114">參數</span><span class="sxs-lookup"><span data-stu-id="035cf-114">PARAMETERS</span></span>

### <span data-ttu-id="035cf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="035cf-115">-AsJob</span></span>
<span data-ttu-id="035cf-116">執行命令做為工作</span><span class="sxs-lookup"><span data-stu-id="035cf-116">Run the command as a job</span></span>

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

### <span data-ttu-id="035cf-117">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="035cf-117">-ClusterName</span></span>
<span data-ttu-id="035cf-118">呼叫取得之 Kubernetes 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="035cf-118">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="035cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="035cf-119">-DefaultProfile</span></span>
<span data-ttu-id="035cf-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="035cf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="035cf-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="035cf-121">-InputObject</span></span>
<span data-ttu-id="035cf-122">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="035cf-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="035cf-123">-KubeConfig</span><span class="sxs-lookup"><span data-stu-id="035cf-123">-KubeConfig</span></span>
<span data-ttu-id="035cf-124">Kube config 檔案的路徑</span><span class="sxs-lookup"><span data-stu-id="035cf-124">Path to the kube config file</span></span>

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

### <span data-ttu-id="035cf-125">-KubeCoNtext</span><span class="sxs-lookup"><span data-stu-id="035cf-125">-KubeContext</span></span>
<span data-ttu-id="035cf-126">從目前電腦 Kubconfig 內容</span><span class="sxs-lookup"><span data-stu-id="035cf-126">Kubconfig context from current machine</span></span>

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

### <span data-ttu-id="035cf-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="035cf-127">-NoWait</span></span>
<span data-ttu-id="035cf-128">以非同步方式執行命令</span><span class="sxs-lookup"><span data-stu-id="035cf-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="035cf-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="035cf-129">-PassThru</span></span>
<span data-ttu-id="035cf-130">在命令成功時傳回 true</span><span class="sxs-lookup"><span data-stu-id="035cf-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="035cf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="035cf-131">-ResourceGroupName</span></span>
<span data-ttu-id="035cf-132">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="035cf-132">The name of the resource group.</span></span>
<span data-ttu-id="035cf-133">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="035cf-133">The name is case insensitive.</span></span>

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

### <span data-ttu-id="035cf-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="035cf-134">-SubscriptionId</span></span>
<span data-ttu-id="035cf-135">目標訂閱的 ID。</span><span class="sxs-lookup"><span data-stu-id="035cf-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="035cf-136">-確認</span><span class="sxs-lookup"><span data-stu-id="035cf-136">-Confirm</span></span>
<span data-ttu-id="035cf-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="035cf-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="035cf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="035cf-138">-WhatIf</span></span>
<span data-ttu-id="035cf-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="035cf-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="035cf-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="035cf-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="035cf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="035cf-141">CommonParameters</span></span>
<span data-ttu-id="035cf-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="035cf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="035cf-143">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="035cf-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="035cf-144">輸入</span><span class="sxs-lookup"><span data-stu-id="035cf-144">INPUTS</span></span>

### <span data-ttu-id="035cf-145">IConnectedKubernetesIdentity （ConnectedKubernetes）的</span><span class="sxs-lookup"><span data-stu-id="035cf-145">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="035cf-146">輸出</span><span class="sxs-lookup"><span data-stu-id="035cf-146">OUTPUTS</span></span>

### <span data-ttu-id="035cf-147">System.object</span><span class="sxs-lookup"><span data-stu-id="035cf-147">System.Boolean</span></span>

## <span data-ttu-id="035cf-148">筆記</span><span class="sxs-lookup"><span data-stu-id="035cf-148">NOTES</span></span>

<span data-ttu-id="035cf-149">別名</span><span class="sxs-lookup"><span data-stu-id="035cf-149">ALIASES</span></span>

<span data-ttu-id="035cf-150">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="035cf-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="035cf-151">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="035cf-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="035cf-152">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="035cf-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="035cf-153">INPUTOBJECT <IConnectedKubernetesIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="035cf-153">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="035cf-154">`[ClusterName <String>]`：呼叫取得之 Kubernetes 群集的名稱。</span><span class="sxs-lookup"><span data-stu-id="035cf-154">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="035cf-155">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="035cf-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="035cf-156">`[ResourceGroupName <String>]`：資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="035cf-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="035cf-157">名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="035cf-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="035cf-158">`[SubscriptionId <String>]`：目標訂閱的識別碼。</span><span class="sxs-lookup"><span data-stu-id="035cf-158">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="035cf-159">相關連結</span><span class="sxs-lookup"><span data-stu-id="035cf-159">RELATED LINKS</span></span>
