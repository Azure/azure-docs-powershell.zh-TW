---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 675bc66afd41e5db2ee356ad45ee2fdd9b3482f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904725"
---
# <span data-ttu-id="89d64-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="89d64-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="89d64-102">簡介</span><span class="sxs-lookup"><span data-stu-id="89d64-102">SYNOPSIS</span></span>
<span data-ttu-id="89d64-103">從公用/azure 註冊表將圖像導入 Azure 容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="89d64-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="89d64-104">語法</span><span class="sxs-lookup"><span data-stu-id="89d64-104">SYNTAX</span></span>

### <span data-ttu-id="89d64-105">ImportImageByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="89d64-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="89d64-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="89d64-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89d64-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="89d64-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="89d64-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="89d64-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89d64-109">描述</span><span class="sxs-lookup"><span data-stu-id="89d64-109">DESCRIPTION</span></span>
<span data-ttu-id="89d64-110">從公用/azure 註冊表將圖像導入 Azure 容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="89d64-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="89d64-111">例子</span><span class="sxs-lookup"><span data-stu-id="89d64-111">EXAMPLES</span></span>

### <span data-ttu-id="89d64-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="89d64-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="89d64-113">將忙碌箱匯出至 ACR。</span><span class="sxs-lookup"><span data-stu-id="89d64-113">Import busybox to ACR.</span></span> <span data-ttu-id="89d64-114">注意：</span><span class="sxs-lookup"><span data-stu-id="89d64-114">Note:</span></span> 
* <span data-ttu-id="89d64-115">在來源圖像之前，必須新增「文件庫/」。</span><span class="sxs-lookup"><span data-stu-id="89d64-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="89d64-116">"busybox：latest" =>文件庫/busybox：latest"</span><span class="sxs-lookup"><span data-stu-id="89d64-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="89d64-117">來源登錄無法公開時所需的認證</span><span class="sxs-lookup"><span data-stu-id="89d64-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="89d64-118">範例 2</span><span class="sxs-lookup"><span data-stu-id="89d64-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="89d64-119">從來源 ACR 將忙碌箱匯出至目標 ACR。</span><span class="sxs-lookup"><span data-stu-id="89d64-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="89d64-120">注意：</span><span class="sxs-lookup"><span data-stu-id="89d64-120">Note:</span></span> 
* <span data-ttu-id="89d64-121">如果來源登錄的系統管理員使用者已停用，則需要認證。</span><span class="sxs-lookup"><span data-stu-id="89d64-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="89d64-122">參數</span><span class="sxs-lookup"><span data-stu-id="89d64-122">PARAMETERS</span></span>

### <span data-ttu-id="89d64-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89d64-123">-DefaultProfile</span></span>
<span data-ttu-id="89d64-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="89d64-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89d64-125">-模式</span><span class="sxs-lookup"><span data-stu-id="89d64-125">-Mode</span></span>
<span data-ttu-id="89d64-126">當強制時，任何現有的目標標記都會被覆蓋。</span><span class="sxs-lookup"><span data-stu-id="89d64-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="89d64-127">當 NoForce 時，任何現有的目標標記都會在複製開始之前失敗。</span><span class="sxs-lookup"><span data-stu-id="89d64-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Force, NoForce

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d64-128">-密碼</span><span class="sxs-lookup"><span data-stu-id="89d64-128">-Password</span></span>
<span data-ttu-id="89d64-129">用來向來源登錄進行驗證的密碼。</span><span class="sxs-lookup"><span data-stu-id="89d64-129">The password used to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d64-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="89d64-130">-RegistryName</span></span>
<span data-ttu-id="89d64-131">目標注冊表名稱。</span><span class="sxs-lookup"><span data-stu-id="89d64-131">Target registry name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d64-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89d64-132">-ResourceGroupName</span></span>
<span data-ttu-id="89d64-133">資源組名。</span><span class="sxs-lookup"><span data-stu-id="89d64-133">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d64-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="89d64-134">-SourceImage</span></span>
<span data-ttu-id="89d64-135">來源圖像的存放庫名稱。</span><span class="sxs-lookup"><span data-stu-id="89d64-135">Repository name of the source image.</span></span>

<span data-ttu-id="89d64-136">根據存放庫指定圖像 ( hello-world') 。</span><span class="sxs-lookup"><span data-stu-id="89d64-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="89d64-137">這會使用 'latest' 標記。</span><span class="sxs-lookup"><span data-stu-id="89d64-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="89d64-138">使用標記指定圖像 ( hello-world：latest') 。</span><span class="sxs-lookup"><span data-stu-id="89d64-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="89d64-139">根據 sha256 型的清單摘要來指定影像 (' hello-world@sha256:abc123 ') 。</span><span class="sxs-lookup"><span data-stu-id="89d64-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89d64-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="89d64-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="89d64-141">來源 Azure Container Registry 的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="89d64-141">The resource identifier of the source Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceId, ImportImageByResourceIdWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89d64-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="89d64-142">-SourceRegistryUri</span></span>
<span data-ttu-id="89d64-143">來源註冊表的位址 (例如 'mcr.microsoft.com') 。</span><span class="sxs-lookup"><span data-stu-id="89d64-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByRegistryUri, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89d64-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="89d64-144">-TargetTag</span></span>
<span data-ttu-id="89d64-145">表單 repo ：tag 的字串 \[ 清單 \] 。</span><span class="sxs-lookup"><span data-stu-id="89d64-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="89d64-146">如果省略標記，則來源會 (或 'latest'，如果來源標記也省略) 。</span><span class="sxs-lookup"><span data-stu-id="89d64-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d64-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="89d64-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="89d64-148">存放庫名稱字串清單，以執行僅執行清單副本。</span><span class="sxs-lookup"><span data-stu-id="89d64-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="89d64-149">不會建立任何標記。</span><span class="sxs-lookup"><span data-stu-id="89d64-149">No tag will be created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d64-150">-使用者名稱</span><span class="sxs-lookup"><span data-stu-id="89d64-150">-Username</span></span>
<span data-ttu-id="89d64-151">向來源登錄驗證的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="89d64-151">The username to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89d64-152">-確認</span><span class="sxs-lookup"><span data-stu-id="89d64-152">-Confirm</span></span>
<span data-ttu-id="89d64-153">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="89d64-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89d64-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89d64-154">-WhatIf</span></span>
<span data-ttu-id="89d64-155">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="89d64-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89d64-156">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="89d64-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89d64-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89d64-157">CommonParameters</span></span>
<span data-ttu-id="89d64-158">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="89d64-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89d64-159">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="89d64-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89d64-160">輸入</span><span class="sxs-lookup"><span data-stu-id="89d64-160">INPUTS</span></span>

### <span data-ttu-id="89d64-161">System.String</span><span class="sxs-lookup"><span data-stu-id="89d64-161">System.String</span></span>

## <span data-ttu-id="89d64-162">輸出</span><span class="sxs-lookup"><span data-stu-id="89d64-162">OUTPUTS</span></span>

### <span data-ttu-id="89d64-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="89d64-163">System.Boolean</span></span>

## <span data-ttu-id="89d64-164">筆記</span><span class="sxs-lookup"><span data-stu-id="89d64-164">NOTES</span></span>

## <span data-ttu-id="89d64-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="89d64-165">RELATED LINKS</span></span>
