---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/set-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Set-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/Set-AzureRmAks.md
ms.openlocfilehash: b5d3248c81507abf6092aa4354691975c4b4bc13
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447550"
---
# <span data-ttu-id="4cb77-101">Set-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="4cb77-101">Set-AzureRmAks</span></span>

## <span data-ttu-id="4cb77-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4cb77-102">SYNOPSIS</span></span>
<span data-ttu-id="4cb77-103">更新或建立受管理的 Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="4cb77-103">Update or create a managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cb77-104">句法</span><span class="sxs-lookup"><span data-stu-id="4cb77-104">SYNTAX</span></span>

### <span data-ttu-id="4cb77-105">defaultParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="4cb77-105">defaultParameterSet (Default)</span></span>
```
Set-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cb77-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cb77-106">InputObjectParameterSet</span></span>
```
Set-AzureRmAks -InputObject <PSKubernetesCluster> [-Location <String>] [-AdminUserName <String>]
 [-DnsNamePrefix <String>] [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>]
 [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4cb77-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cb77-107">IdParameterSet</span></span>
```
Set-AzureRmAks [-Id] <String> [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>]
 [-KubernetesVersion <String>] [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>]
 [-SshKeyValue <String>] [-AsJob] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4cb77-108">說明</span><span class="sxs-lookup"><span data-stu-id="4cb77-108">DESCRIPTION</span></span>
<span data-ttu-id="4cb77-109">更新或建立受管理的 Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="4cb77-109">Update or create a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="4cb77-110">示例</span><span class="sxs-lookup"><span data-stu-id="4cb77-110">EXAMPLES</span></span>

### <span data-ttu-id="4cb77-111">範例1</span><span class="sxs-lookup"><span data-stu-id="4cb77-111">Example 1</span></span>
```
PS C:\> Get-AzureRmAks -ResourceGroupName group -Name myCluster | Set-AzureRmAks -NodeCount 5
```

<span data-ttu-id="4cb77-112">將 Kubernetes 群集中的節點數設定為5。</span><span class="sxs-lookup"><span data-stu-id="4cb77-112">Set the number of nodes in the Kubernetes cluster to 5.</span></span>

## <span data-ttu-id="4cb77-113">參數</span><span class="sxs-lookup"><span data-stu-id="4cb77-113">PARAMETERS</span></span>

### <span data-ttu-id="4cb77-114">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="4cb77-114">-AdminUserName</span></span>
<span data-ttu-id="4cb77-115">Linux 虛擬機器的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="4cb77-115">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="4cb77-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cb77-116">-AsJob</span></span>
<span data-ttu-id="4cb77-117">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="4cb77-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4cb77-118">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="4cb77-118">-ClientIdAndSecret</span></span>
<span data-ttu-id="4cb77-119">與 AAD 應用程式/服務主體相關聯的用戶端識別碼與用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="4cb77-119">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: defaultParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb77-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cb77-120">-DefaultProfile</span></span>
<span data-ttu-id="4cb77-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4cb77-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb77-122">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="4cb77-122">-DnsNamePrefix</span></span>
<span data-ttu-id="4cb77-123">群集的 DNS 名稱首碼。</span><span class="sxs-lookup"><span data-stu-id="4cb77-123">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="4cb77-124">-識別碼</span><span class="sxs-lookup"><span data-stu-id="4cb77-124">-Id</span></span>
<span data-ttu-id="4cb77-125">受管理的 Kubernetes 群集的 Id</span><span class="sxs-lookup"><span data-stu-id="4cb77-125">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="4cb77-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cb77-126">-InputObject</span></span>
<span data-ttu-id="4cb77-127">PSKubernetesCluster 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="4cb77-127">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cb77-128">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="4cb77-128">-KubernetesVersion</span></span>
<span data-ttu-id="4cb77-129">要用來建立群集的 Kubernetes 版本。</span><span class="sxs-lookup"><span data-stu-id="4cb77-129">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="4cb77-130">-位置</span><span class="sxs-lookup"><span data-stu-id="4cb77-130">-Location</span></span>
<span data-ttu-id="4cb77-131">群集的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="4cb77-131">Azure location for the cluster.</span></span>
<span data-ttu-id="4cb77-132">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="4cb77-132">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="4cb77-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="4cb77-133">-Name</span></span>
<span data-ttu-id="4cb77-134">Kubernetes 受管理的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="4cb77-134">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb77-135">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="4cb77-135">-NodeCount</span></span>
<span data-ttu-id="4cb77-136">節點池的預設節點數。</span><span class="sxs-lookup"><span data-stu-id="4cb77-136">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb77-137">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="4cb77-137">-NodeOsDiskSize</span></span>
<span data-ttu-id="4cb77-138">節點池的預設節點數。</span><span class="sxs-lookup"><span data-stu-id="4cb77-138">The default number of nodes for the node pools.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb77-139">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="4cb77-139">-NodeVmSize</span></span>
<span data-ttu-id="4cb77-140">虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="4cb77-140">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="4cb77-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cb77-141">-ResourceGroupName</span></span>
<span data-ttu-id="4cb77-142">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="4cb77-142">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb77-143">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="4cb77-143">-SshKeyValue</span></span>
<span data-ttu-id="4cb77-144">SSH 金鑰檔值或金鑰檔路徑。</span><span class="sxs-lookup"><span data-stu-id="4cb77-144">SSH key file value or key file path.</span></span>
<span data-ttu-id="4cb77-145">預設值為 {HOME}/.ssh/[id_rsa .pub]。</span><span class="sxs-lookup"><span data-stu-id="4cb77-145">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cb77-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="4cb77-146">-Tag</span></span>
<span data-ttu-id="4cb77-147">要套用至資源的標記</span><span class="sxs-lookup"><span data-stu-id="4cb77-147">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="4cb77-148">-確認</span><span class="sxs-lookup"><span data-stu-id="4cb77-148">-Confirm</span></span>
<span data-ttu-id="4cb77-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4cb77-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cb77-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cb77-150">-WhatIf</span></span>
<span data-ttu-id="4cb77-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4cb77-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cb77-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4cb77-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cb77-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cb77-153">CommonParameters</span></span>
<span data-ttu-id="4cb77-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4cb77-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cb77-155">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4cb77-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cb77-156">輸入</span><span class="sxs-lookup"><span data-stu-id="4cb77-156">INPUTS</span></span>

### <span data-ttu-id="4cb77-157">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="4cb77-157">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>
<span data-ttu-id="4cb77-158">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="4cb77-158">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4cb77-159">System.object</span><span class="sxs-lookup"><span data-stu-id="4cb77-159">System.String</span></span>

## <span data-ttu-id="4cb77-160">輸出</span><span class="sxs-lookup"><span data-stu-id="4cb77-160">OUTPUTS</span></span>

### <span data-ttu-id="4cb77-161">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="4cb77-161">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="4cb77-162">筆記</span><span class="sxs-lookup"><span data-stu-id="4cb77-162">NOTES</span></span>

## <span data-ttu-id="4cb77-163">相關連結</span><span class="sxs-lookup"><span data-stu-id="4cb77-163">RELATED LINKS</span></span>