---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/new-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/New-AzAks.md
ms.openlocfilehash: 1de3cef0d14213a52873742f9bf878aaa545e8bf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93614146"
---
# <span data-ttu-id="bba31-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="bba31-101">New-AzAks</span></span>

## <span data-ttu-id="bba31-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bba31-102">SYNOPSIS</span></span>
<span data-ttu-id="bba31-103">建立新的 managed Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="bba31-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="bba31-104">句法</span><span class="sxs-lookup"><span data-stu-id="bba31-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bba31-105">說明</span><span class="sxs-lookup"><span data-stu-id="bba31-105">DESCRIPTION</span></span>

<span data-ttu-id="bba31-106">建立新的 managed Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="bba31-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="bba31-107">示例</span><span class="sxs-lookup"><span data-stu-id="bba31-107">EXAMPLES</span></span>

### <span data-ttu-id="bba31-108">範例1</span><span class="sxs-lookup"><span data-stu-id="bba31-108">Example 1</span></span>

<span data-ttu-id="bba31-109">使用預設的參數建立新的 managed Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="bba31-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="bba31-110">參數</span><span class="sxs-lookup"><span data-stu-id="bba31-110">PARAMETERS</span></span>

### <span data-ttu-id="bba31-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="bba31-111">-AdminUserName</span></span>
<span data-ttu-id="bba31-112">Linux 虛擬機器的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="bba31-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="bba31-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bba31-113">-AsJob</span></span>
<span data-ttu-id="bba31-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="bba31-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bba31-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="bba31-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="bba31-116">與 AAD 應用程式/服務主體相關聯的用戶端識別碼與用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="bba31-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba31-117">-DefaultProfile</span></span>
<span data-ttu-id="bba31-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bba31-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bba31-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="bba31-119">-DnsNamePrefix</span></span>
<span data-ttu-id="bba31-120">群集的 DNS 名稱首碼。</span><span class="sxs-lookup"><span data-stu-id="bba31-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="bba31-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bba31-121">-Force</span></span>
<span data-ttu-id="bba31-122">建立群集（即使已存在）</span><span class="sxs-lookup"><span data-stu-id="bba31-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="bba31-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="bba31-123">-KubernetesVersion</span></span>
<span data-ttu-id="bba31-124">要用來建立群集的 Kubernetes 版本。</span><span class="sxs-lookup"><span data-stu-id="bba31-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="bba31-125">-位置</span><span class="sxs-lookup"><span data-stu-id="bba31-125">-Location</span></span>
<span data-ttu-id="bba31-126">群集的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="bba31-126">Azure location for the cluster.</span></span>
<span data-ttu-id="bba31-127">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="bba31-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="bba31-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="bba31-128">-Name</span></span>
<span data-ttu-id="bba31-129">Kubernetes 受管理的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="bba31-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba31-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="bba31-130">-NodeCount</span></span>
<span data-ttu-id="bba31-131">節點池的預設節點數。</span><span class="sxs-lookup"><span data-stu-id="bba31-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="bba31-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="bba31-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="bba31-133">節點池中每個節點的 OS 磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="bba31-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="bba31-134">最低 30 GB。</span><span class="sxs-lookup"><span data-stu-id="bba31-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="bba31-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="bba31-135">-NodeVmSize</span></span>
<span data-ttu-id="bba31-136">虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="bba31-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="bba31-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bba31-137">-ResourceGroupName</span></span>
<span data-ttu-id="bba31-138">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="bba31-138">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bba31-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="bba31-139">-SshKeyValue</span></span>
<span data-ttu-id="bba31-140">SSH 金鑰檔值或金鑰檔路徑。</span><span class="sxs-lookup"><span data-stu-id="bba31-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="bba31-141">預設值為 {HOME}/.ssh/[id_rsa .pub]。</span><span class="sxs-lookup"><span data-stu-id="bba31-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="bba31-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="bba31-142">-Tag</span></span>
<span data-ttu-id="bba31-143">要套用至資源的標記</span><span class="sxs-lookup"><span data-stu-id="bba31-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="bba31-144">-確認</span><span class="sxs-lookup"><span data-stu-id="bba31-144">-Confirm</span></span>
<span data-ttu-id="bba31-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bba31-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bba31-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bba31-146">-WhatIf</span></span>
<span data-ttu-id="bba31-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bba31-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bba31-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bba31-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bba31-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba31-149">CommonParameters</span></span>
<span data-ttu-id="bba31-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bba31-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba31-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="bba31-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba31-152">輸入</span><span class="sxs-lookup"><span data-stu-id="bba31-152">INPUTS</span></span>

### <span data-ttu-id="bba31-153">所有</span><span class="sxs-lookup"><span data-stu-id="bba31-153">None</span></span>

## <span data-ttu-id="bba31-154">輸出</span><span class="sxs-lookup"><span data-stu-id="bba31-154">OUTPUTS</span></span>

### <span data-ttu-id="bba31-155">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="bba31-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="bba31-156">筆記</span><span class="sxs-lookup"><span data-stu-id="bba31-156">NOTES</span></span>

## <span data-ttu-id="bba31-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="bba31-157">RELATED LINKS</span></span>
