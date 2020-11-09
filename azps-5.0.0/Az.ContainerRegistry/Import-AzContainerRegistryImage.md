---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94284487"
---
# <span data-ttu-id="82733-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="82733-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="82733-102">摘要</span><span class="sxs-lookup"><span data-stu-id="82733-102">SYNOPSIS</span></span>
<span data-ttu-id="82733-103">從公用/azure 登錄將圖像匯入至 azure 容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="82733-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="82733-104">句法</span><span class="sxs-lookup"><span data-stu-id="82733-104">SYNTAX</span></span>

### <span data-ttu-id="82733-105">ImportImageByResourceId (預設) </span><span class="sxs-lookup"><span data-stu-id="82733-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="82733-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="82733-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82733-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="82733-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82733-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="82733-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="82733-109">說明</span><span class="sxs-lookup"><span data-stu-id="82733-109">DESCRIPTION</span></span>
<span data-ttu-id="82733-110">從公用/azure 登錄將圖像匯入至 azure 容器註冊表。</span><span class="sxs-lookup"><span data-stu-id="82733-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="82733-111">示例</span><span class="sxs-lookup"><span data-stu-id="82733-111">EXAMPLES</span></span>

### <span data-ttu-id="82733-112">範例1</span><span class="sxs-lookup"><span data-stu-id="82733-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="82733-113">將 busybox 匯入到 ACR。</span><span class="sxs-lookup"><span data-stu-id="82733-113">Import busybox to ACR.</span></span> <span data-ttu-id="82733-114">注</span><span class="sxs-lookup"><span data-stu-id="82733-114">Note:</span></span> 
* <span data-ttu-id="82733-115">"library/" 需要在源影像之前新增。</span><span class="sxs-lookup"><span data-stu-id="82733-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="82733-116">"busybox：最新" => "library/busybox：最新"</span><span class="sxs-lookup"><span data-stu-id="82733-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="82733-117">如果來源註冊表沒有公開提供，則需要認證</span><span class="sxs-lookup"><span data-stu-id="82733-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="82733-118">範例2</span><span class="sxs-lookup"><span data-stu-id="82733-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="82733-119">從來源 ACR 將 busybox 匯入至目標 ACR。</span><span class="sxs-lookup"><span data-stu-id="82733-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="82733-120">注</span><span class="sxs-lookup"><span data-stu-id="82733-120">Note:</span></span> 
* <span data-ttu-id="82733-121">如果來源登錄的管理員使用者已停用，則需要認證。</span><span class="sxs-lookup"><span data-stu-id="82733-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="82733-122">參數</span><span class="sxs-lookup"><span data-stu-id="82733-122">PARAMETERS</span></span>

### <span data-ttu-id="82733-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82733-123">-DefaultProfile</span></span>
<span data-ttu-id="82733-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="82733-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82733-125">模式</span><span class="sxs-lookup"><span data-stu-id="82733-125">-Mode</span></span>
<span data-ttu-id="82733-126">強制會覆寫任何現有的目標標籤。</span><span class="sxs-lookup"><span data-stu-id="82733-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="82733-127">NoForce 時，任何現有的目標標籤都會在任何複製開始前失敗。</span><span class="sxs-lookup"><span data-stu-id="82733-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

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

### <span data-ttu-id="82733-128">-Password</span><span class="sxs-lookup"><span data-stu-id="82733-128">-Password</span></span>
<span data-ttu-id="82733-129">用來針對來源註冊表進行驗證的密碼。</span><span class="sxs-lookup"><span data-stu-id="82733-129">The password used to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="82733-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="82733-130">-RegistryName</span></span>
<span data-ttu-id="82733-131">目標登錄名。</span><span class="sxs-lookup"><span data-stu-id="82733-131">Target registry name.</span></span>

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

### <span data-ttu-id="82733-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82733-132">-ResourceGroupName</span></span>
<span data-ttu-id="82733-133">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="82733-133">Resource group name.</span></span>

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

### <span data-ttu-id="82733-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="82733-134">-SourceImage</span></span>
<span data-ttu-id="82733-135">來源影像的儲存庫名稱。</span><span class="sxs-lookup"><span data-stu-id="82733-135">Repository name of the source image.</span></span>

<span data-ttu-id="82733-136">依資料庫指定影像 ( ' hello-世界」 ) 。</span><span class="sxs-lookup"><span data-stu-id="82733-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="82733-137">這會使用 [最新標誌]。</span><span class="sxs-lookup"><span data-stu-id="82733-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="82733-138">以標籤 ( 「hello-world：最新」 ) 指定影像。</span><span class="sxs-lookup"><span data-stu-id="82733-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="82733-139">根據 sha256 式資訊清單摘要指定影像， ( " hello-world@sha256:abc123 " ) 。</span><span class="sxs-lookup"><span data-stu-id="82733-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

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

### <span data-ttu-id="82733-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="82733-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="82733-141">來源 Azure 容器註冊表的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="82733-141">The resource identifier of the source Azure Container Registry.</span></span>

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

### <span data-ttu-id="82733-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="82733-142">-SourceRegistryUri</span></span>
<span data-ttu-id="82733-143">來源登錄的位址 (（例如 ' mcr.microsoft.com」） ) 。</span><span class="sxs-lookup"><span data-stu-id="82733-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

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

### <span data-ttu-id="82733-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="82733-144">-TargetTag</span></span>
<span data-ttu-id="82733-145">表單存放庫的字串清單 \[ ：標記 \] 。</span><span class="sxs-lookup"><span data-stu-id="82733-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="82733-146">省略 tag 時，會 (使用 [來源] 或 [最新版本] （如果仍省略來源標記）) 。</span><span class="sxs-lookup"><span data-stu-id="82733-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

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

### <span data-ttu-id="82733-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="82733-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="82733-148">要執行資訊清單的字串清單，只複製一個資訊清單。</span><span class="sxs-lookup"><span data-stu-id="82733-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="82733-149">不會建立任何標記。</span><span class="sxs-lookup"><span data-stu-id="82733-149">No tag will be created.</span></span>

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

### <span data-ttu-id="82733-150">-Username</span><span class="sxs-lookup"><span data-stu-id="82733-150">-Username</span></span>
<span data-ttu-id="82733-151">要使用來源註冊表進行驗證的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="82733-151">The username to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="82733-152">-確認</span><span class="sxs-lookup"><span data-stu-id="82733-152">-Confirm</span></span>
<span data-ttu-id="82733-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="82733-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82733-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82733-154">-WhatIf</span></span>
<span data-ttu-id="82733-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="82733-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82733-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="82733-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82733-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82733-157">CommonParameters</span></span>
<span data-ttu-id="82733-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="82733-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82733-159">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="82733-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82733-160">輸入</span><span class="sxs-lookup"><span data-stu-id="82733-160">INPUTS</span></span>

### <span data-ttu-id="82733-161">System.object</span><span class="sxs-lookup"><span data-stu-id="82733-161">System.String</span></span>

## <span data-ttu-id="82733-162">輸出</span><span class="sxs-lookup"><span data-stu-id="82733-162">OUTPUTS</span></span>

### <span data-ttu-id="82733-163">System.object</span><span class="sxs-lookup"><span data-stu-id="82733-163">System.Boolean</span></span>

## <span data-ttu-id="82733-164">筆記</span><span class="sxs-lookup"><span data-stu-id="82733-164">NOTES</span></span>

## <span data-ttu-id="82733-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="82733-165">RELATED LINKS</span></span>
