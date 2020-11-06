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
ms.locfileid: "93611688"
---
# <span data-ttu-id="d617e-101">New-AzAks</span><span class="sxs-lookup"><span data-stu-id="d617e-101">New-AzAks</span></span>

## <span data-ttu-id="d617e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d617e-102">SYNOPSIS</span></span>
<span data-ttu-id="d617e-103">建立新的 managed Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="d617e-103">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="d617e-104">句法</span><span class="sxs-lookup"><span data-stu-id="d617e-104">SYNTAX</span></span>

```
New-AzAks [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d617e-105">說明</span><span class="sxs-lookup"><span data-stu-id="d617e-105">DESCRIPTION</span></span>

<span data-ttu-id="d617e-106">建立新的 managed Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="d617e-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="d617e-107">示例</span><span class="sxs-lookup"><span data-stu-id="d617e-107">EXAMPLES</span></span>

### <span data-ttu-id="d617e-108">範例1</span><span class="sxs-lookup"><span data-stu-id="d617e-108">Example 1</span></span>

<span data-ttu-id="d617e-109">使用預設的參數建立新的 managed Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="d617e-109">Create a new managed Kubernetes cluster with default params.</span></span>

```
PS C:\> New-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="d617e-110">參數</span><span class="sxs-lookup"><span data-stu-id="d617e-110">PARAMETERS</span></span>

### <span data-ttu-id="d617e-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="d617e-111">-AdminUserName</span></span>
<span data-ttu-id="d617e-112">Linux 虛擬機器的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="d617e-112">User name for the Linux Virtual Machines.</span></span>

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

### <span data-ttu-id="d617e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d617e-113">-AsJob</span></span>
<span data-ttu-id="d617e-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="d617e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d617e-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="d617e-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="d617e-116">與 AAD 應用程式/服務主體相關聯的用戶端識別碼與用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="d617e-116">The client id and client secret associated with the AAD application / service principal.</span></span>

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

### <span data-ttu-id="d617e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d617e-117">-DefaultProfile</span></span>
<span data-ttu-id="d617e-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d617e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d617e-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="d617e-119">-DnsNamePrefix</span></span>
<span data-ttu-id="d617e-120">群集的 DNS 名稱首碼。</span><span class="sxs-lookup"><span data-stu-id="d617e-120">The DNS name prefix for the cluster.</span></span>

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

### <span data-ttu-id="d617e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d617e-121">-Force</span></span>
<span data-ttu-id="d617e-122">建立群集（即使已存在）</span><span class="sxs-lookup"><span data-stu-id="d617e-122">Create cluster even if it already exists</span></span>

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

### <span data-ttu-id="d617e-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="d617e-123">-KubernetesVersion</span></span>
<span data-ttu-id="d617e-124">要用來建立群集的 Kubernetes 版本。</span><span class="sxs-lookup"><span data-stu-id="d617e-124">The version of Kubernetes to use for creating the cluster.</span></span>

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

### <span data-ttu-id="d617e-125">-位置</span><span class="sxs-lookup"><span data-stu-id="d617e-125">-Location</span></span>
<span data-ttu-id="d617e-126">群集的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="d617e-126">Azure location for the cluster.</span></span>
<span data-ttu-id="d617e-127">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="d617e-127">Defaults to the location of the resource group.</span></span>

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

### <span data-ttu-id="d617e-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="d617e-128">-Name</span></span>
<span data-ttu-id="d617e-129">Kubernetes 受管理的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="d617e-129">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="d617e-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="d617e-130">-NodeCount</span></span>
<span data-ttu-id="d617e-131">節點池的預設節點數。</span><span class="sxs-lookup"><span data-stu-id="d617e-131">The default number of nodes for the node pools.</span></span>

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

### <span data-ttu-id="d617e-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="d617e-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="d617e-133">節點池中每個節點的 OS 磁片大小（GB）。</span><span class="sxs-lookup"><span data-stu-id="d617e-133">Size in GB of the OS disk for each node in the node pool.</span></span> <span data-ttu-id="d617e-134">最低 30 GB。</span><span class="sxs-lookup"><span data-stu-id="d617e-134">Minimum 30 GB.</span></span>

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

### <span data-ttu-id="d617e-135">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="d617e-135">-NodeVmSize</span></span>
<span data-ttu-id="d617e-136">虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="d617e-136">The size of the Virtual Machine.</span></span>

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

### <span data-ttu-id="d617e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d617e-137">-ResourceGroupName</span></span>
<span data-ttu-id="d617e-138">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="d617e-138">Resource Group Name.</span></span>

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

### <span data-ttu-id="d617e-139">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="d617e-139">-SshKeyValue</span></span>
<span data-ttu-id="d617e-140">SSH 金鑰檔值或金鑰檔路徑。</span><span class="sxs-lookup"><span data-stu-id="d617e-140">SSH key file value or key file path.</span></span>
<span data-ttu-id="d617e-141">預設值為 {HOME}/.ssh/[id_rsa .pub]。</span><span class="sxs-lookup"><span data-stu-id="d617e-141">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

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

### <span data-ttu-id="d617e-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="d617e-142">-Tag</span></span>
<span data-ttu-id="d617e-143">要套用至資源的標記</span><span class="sxs-lookup"><span data-stu-id="d617e-143">Tags to be applied to the resource</span></span>

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

### <span data-ttu-id="d617e-144">-確認</span><span class="sxs-lookup"><span data-stu-id="d617e-144">-Confirm</span></span>
<span data-ttu-id="d617e-145">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d617e-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d617e-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d617e-146">-WhatIf</span></span>
<span data-ttu-id="d617e-147">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d617e-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d617e-148">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d617e-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d617e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d617e-149">CommonParameters</span></span>
<span data-ttu-id="d617e-150">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d617e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d617e-151">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d617e-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d617e-152">輸入</span><span class="sxs-lookup"><span data-stu-id="d617e-152">INPUTS</span></span>

### <span data-ttu-id="d617e-153">所有</span><span class="sxs-lookup"><span data-stu-id="d617e-153">None</span></span>

## <span data-ttu-id="d617e-154">輸出</span><span class="sxs-lookup"><span data-stu-id="d617e-154">OUTPUTS</span></span>

### <span data-ttu-id="d617e-155">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="d617e-155">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="d617e-156">筆記</span><span class="sxs-lookup"><span data-stu-id="d617e-156">NOTES</span></span>

## <span data-ttu-id="d617e-157">相關連結</span><span class="sxs-lookup"><span data-stu-id="d617e-157">RELATED LINKS</span></span>
