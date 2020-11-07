---
external help file: Microsoft.Azure.Commands.Aks.dll-Help.xml
Module Name: AzureRM.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.aks/new-azurermaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Aks/Commands.Aks/help/New-AzureRmAks.md
ms.openlocfilehash: ed68271ae29c7af0219fa08d1c342b636d7d3fbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625946"
---
# <span data-ttu-id="61556-101">New-AzureRmAks</span><span class="sxs-lookup"><span data-stu-id="61556-101">New-AzureRmAks</span></span>

## <span data-ttu-id="61556-102">摘要</span><span class="sxs-lookup"><span data-stu-id="61556-102">SYNOPSIS</span></span>
<span data-ttu-id="61556-103">建立新的 managed Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="61556-103">Create a new managed Kubernetes cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61556-104">句法</span><span class="sxs-lookup"><span data-stu-id="61556-104">SYNTAX</span></span>

```
New-AzureRmAks [-ResourceGroupName] <String> [-Name] <String> [[-ClientIdAndSecret] <PSCredential>]
 [-Location <String>] [-AdminUserName <String>] [-DnsNamePrefix <String>] [-KubernetesVersion <String>]
 [-NodeCount <Int32>] [-NodeOsDiskSize <Int32>] [-NodeVmSize <String>] [-SshKeyValue <String>] [-Force] [-AsJob]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61556-105">說明</span><span class="sxs-lookup"><span data-stu-id="61556-105">DESCRIPTION</span></span>
<span data-ttu-id="61556-106">建立新的 managed Kubernetes 群集。</span><span class="sxs-lookup"><span data-stu-id="61556-106">Create a new managed Kubernetes cluster.</span></span>

## <span data-ttu-id="61556-107">示例</span><span class="sxs-lookup"><span data-stu-id="61556-107">EXAMPLES</span></span>

### <span data-ttu-id="61556-108">範例1</span><span class="sxs-lookup"><span data-stu-id="61556-108">Example 1</span></span>
<span data-ttu-id="61556-109">使用預設參數建立新的 managed Kubernetes 群集</span><span class="sxs-lookup"><span data-stu-id="61556-109">Create a new managed Kubernetes cluster with default params</span></span>

```
PS C:\> New-AzureRmAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="61556-110">參數</span><span class="sxs-lookup"><span data-stu-id="61556-110">PARAMETERS</span></span>

### <span data-ttu-id="61556-111">-AdminUserName</span><span class="sxs-lookup"><span data-stu-id="61556-111">-AdminUserName</span></span>
<span data-ttu-id="61556-112">Linux 虛擬機器的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="61556-112">User name for the Linux Virtual Machines.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="61556-113">-AsJob</span></span>
<span data-ttu-id="61556-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="61556-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-115">-ClientIdAndSecret</span><span class="sxs-lookup"><span data-stu-id="61556-115">-ClientIdAndSecret</span></span>
<span data-ttu-id="61556-116">與 AAD 應用程式/服務主體相關聯的用戶端識別碼與用戶端密碼。</span><span class="sxs-lookup"><span data-stu-id="61556-116">The client id and client secret associated with the AAD application / service principal.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61556-117">-DefaultProfile</span></span>
<span data-ttu-id="61556-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="61556-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-119">-DnsNamePrefix</span><span class="sxs-lookup"><span data-stu-id="61556-119">-DnsNamePrefix</span></span>
<span data-ttu-id="61556-120">群集的 DNS 名稱首碼。</span><span class="sxs-lookup"><span data-stu-id="61556-120">The DNS name prefix for the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-121">-Force</span><span class="sxs-lookup"><span data-stu-id="61556-121">-Force</span></span>
<span data-ttu-id="61556-122">建立群集（即使已存在）</span><span class="sxs-lookup"><span data-stu-id="61556-122">Create cluster even if it already exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-123">-KubernetesVersion</span><span class="sxs-lookup"><span data-stu-id="61556-123">-KubernetesVersion</span></span>
<span data-ttu-id="61556-124">要用來建立群集的 Kubernetes 版本。</span><span class="sxs-lookup"><span data-stu-id="61556-124">The version of Kubernetes to use for creating the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-125">-位置</span><span class="sxs-lookup"><span data-stu-id="61556-125">-Location</span></span>
<span data-ttu-id="61556-126">群集的 Azure 位置。</span><span class="sxs-lookup"><span data-stu-id="61556-126">Azure location for the cluster.</span></span>
<span data-ttu-id="61556-127">預設為資源群組的位置。</span><span class="sxs-lookup"><span data-stu-id="61556-127">Defaults to the location of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="61556-128">-Name</span></span>
<span data-ttu-id="61556-129">Kubernetes 受管理的群集名稱。</span><span class="sxs-lookup"><span data-stu-id="61556-129">Kubernetes managed cluster Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-130">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="61556-130">-NodeCount</span></span>
<span data-ttu-id="61556-131">節點池的預設節點數。</span><span class="sxs-lookup"><span data-stu-id="61556-131">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-132">-NodeOsDiskSize</span><span class="sxs-lookup"><span data-stu-id="61556-132">-NodeOsDiskSize</span></span>
<span data-ttu-id="61556-133">節點池的預設節點數。</span><span class="sxs-lookup"><span data-stu-id="61556-133">The default number of nodes for the node pools.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-134">-NodeVmSize</span><span class="sxs-lookup"><span data-stu-id="61556-134">-NodeVmSize</span></span>
<span data-ttu-id="61556-135">虛擬機器的大小。</span><span class="sxs-lookup"><span data-stu-id="61556-135">The size of the Virtual Machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61556-136">-ResourceGroupName</span></span>
<span data-ttu-id="61556-137">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="61556-137">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-138">-SshKeyValue</span><span class="sxs-lookup"><span data-stu-id="61556-138">-SshKeyValue</span></span>
<span data-ttu-id="61556-139">SSH 金鑰檔值或金鑰檔路徑。</span><span class="sxs-lookup"><span data-stu-id="61556-139">SSH key file value or key file path.</span></span>
<span data-ttu-id="61556-140">預設值為 {HOME}/.ssh/[id_rsa .pub]。</span><span class="sxs-lookup"><span data-stu-id="61556-140">Defaults to {HOME}/.ssh/id_rsa.pub.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SshKeyPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="61556-141">-Tag</span></span>
<span data-ttu-id="61556-142">要套用至資源的標記</span><span class="sxs-lookup"><span data-stu-id="61556-142">Tags to be applied to the resource</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-143">-確認</span><span class="sxs-lookup"><span data-stu-id="61556-143">-Confirm</span></span>
<span data-ttu-id="61556-144">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="61556-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61556-145">-WhatIf</span></span>
<span data-ttu-id="61556-146">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="61556-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="61556-147">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="61556-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61556-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61556-148">CommonParameters</span></span>
<span data-ttu-id="61556-149">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="61556-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61556-150">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="61556-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61556-151">輸入</span><span class="sxs-lookup"><span data-stu-id="61556-151">INPUTS</span></span>

### <span data-ttu-id="61556-152">所有</span><span class="sxs-lookup"><span data-stu-id="61556-152">None</span></span>

## <span data-ttu-id="61556-153">輸出</span><span class="sxs-lookup"><span data-stu-id="61556-153">OUTPUTS</span></span>

### <span data-ttu-id="61556-154">PSKubernetesCluster 中的 Aks。</span><span class="sxs-lookup"><span data-stu-id="61556-154">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="61556-155">筆記</span><span class="sxs-lookup"><span data-stu-id="61556-155">NOTES</span></span>

## <span data-ttu-id="61556-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="61556-156">RELATED LINKS</span></span>
