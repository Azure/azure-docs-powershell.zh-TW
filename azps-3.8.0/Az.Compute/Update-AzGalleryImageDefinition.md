---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 042c29ca079978a4ce740dba7d8ced9b0387eaf4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958525"
---
# <span data-ttu-id="761a1-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="761a1-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="761a1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="761a1-102">SYNOPSIS</span></span>
<span data-ttu-id="761a1-103">更新圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="761a1-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="761a1-104">句法</span><span class="sxs-lookup"><span data-stu-id="761a1-104">SYNTAX</span></span>

### <span data-ttu-id="761a1-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="761a1-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="761a1-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="761a1-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="761a1-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="761a1-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="761a1-108">說明</span><span class="sxs-lookup"><span data-stu-id="761a1-108">DESCRIPTION</span></span>
<span data-ttu-id="761a1-109">更新圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="761a1-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="761a1-110">示例</span><span class="sxs-lookup"><span data-stu-id="761a1-110">EXAMPLES</span></span>

### <span data-ttu-id="761a1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="761a1-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="761a1-112">更新圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="761a1-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="761a1-113">參數</span><span class="sxs-lookup"><span data-stu-id="761a1-113">PARAMETERS</span></span>

### <span data-ttu-id="761a1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="761a1-114">-AsJob</span></span>
<span data-ttu-id="761a1-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="761a1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="761a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="761a1-116">-DefaultProfile</span></span>
<span data-ttu-id="761a1-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="761a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="761a1-118">-描述</span><span class="sxs-lookup"><span data-stu-id="761a1-118">-Description</span></span>
<span data-ttu-id="761a1-119">圖庫影像定義資源的描述。</span><span class="sxs-lookup"><span data-stu-id="761a1-119">The description of the gallery image Definition resource.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="761a1-120">-DisallowedDiskType</span></span>
<span data-ttu-id="761a1-121">非許可的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="761a1-121">The disallowed disk types.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="761a1-122">-EndOfLifeDate</span></span>
<span data-ttu-id="761a1-123">圖庫影像定義的生命循環結束日期</span><span class="sxs-lookup"><span data-stu-id="761a1-123">The end of life date of the gallery Image Definition</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="761a1-124">-Eula</span></span>
<span data-ttu-id="761a1-125">畫廊影像定義的 Eula 合約。</span><span class="sxs-lookup"><span data-stu-id="761a1-125">The Eula agreement for the gallery Image Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="761a1-126">-GalleryName</span></span>
<span data-ttu-id="761a1-127">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="761a1-127">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="761a1-128">-InputObject</span></span>
<span data-ttu-id="761a1-129">PS 圖庫影像定義物件。</span><span class="sxs-lookup"><span data-stu-id="761a1-129">The PS Gallery Image Definition Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage
Parameter Sets: ObjectParameter
Aliases: GalleryImageDefinition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="761a1-130">-MaximumMemory</span></span>
<span data-ttu-id="761a1-131">建議的記憶體上限</span><span class="sxs-lookup"><span data-stu-id="761a1-131">The maximum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="761a1-132">-MaximumVCPU</span></span>
<span data-ttu-id="761a1-133">建議的 CPU 核心最大值</span><span class="sxs-lookup"><span data-stu-id="761a1-133">The maximum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="761a1-134">-MinimumMemory</span></span>
<span data-ttu-id="761a1-135">建議的記憶體最小值</span><span class="sxs-lookup"><span data-stu-id="761a1-135">The minimum of the recommended memory</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="761a1-136">-MinimumVCPU</span></span>
<span data-ttu-id="761a1-137">建議的 CPU 核心最小值</span><span class="sxs-lookup"><span data-stu-id="761a1-137">The minimum of the recommended CPU core</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="761a1-138">-Name</span></span>
<span data-ttu-id="761a1-139">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="761a1-139">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="761a1-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="761a1-141">隱私權語句 uri。</span><span class="sxs-lookup"><span data-stu-id="761a1-141">The privacy statement uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="761a1-142">-PurchasePlanName</span></span>
<span data-ttu-id="761a1-143">採購方案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="761a1-143">The ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="761a1-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="761a1-145">採購方案的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="761a1-145">The product ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="761a1-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="761a1-147">採購方案的發行者識別碼。</span><span class="sxs-lookup"><span data-stu-id="761a1-147">The publisher ID for the purchase plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="761a1-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="761a1-149">版本記事 uri。</span><span class="sxs-lookup"><span data-stu-id="761a1-149">The release note uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="761a1-150">-ResourceGroupName</span></span>
<span data-ttu-id="761a1-151">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="761a1-151">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="761a1-152">-ResourceId</span></span>
<span data-ttu-id="761a1-153">影像定義的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="761a1-153">The resource ID for the image definition</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="761a1-154">-Tag</span></span>
<span data-ttu-id="761a1-155">資源標記</span><span class="sxs-lookup"><span data-stu-id="761a1-155">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="761a1-156">-確認</span><span class="sxs-lookup"><span data-stu-id="761a1-156">-Confirm</span></span>
<span data-ttu-id="761a1-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="761a1-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="761a1-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="761a1-158">-WhatIf</span></span>
<span data-ttu-id="761a1-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="761a1-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="761a1-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="761a1-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="761a1-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="761a1-161">CommonParameters</span></span>
<span data-ttu-id="761a1-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="761a1-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="761a1-163">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="761a1-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="761a1-164">輸入</span><span class="sxs-lookup"><span data-stu-id="761a1-164">INPUTS</span></span>

### <span data-ttu-id="761a1-165">System.object</span><span class="sxs-lookup"><span data-stu-id="761a1-165">System.String</span></span>

### <span data-ttu-id="761a1-166">PSGalleryImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="761a1-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="761a1-167">System.object</span><span class="sxs-lookup"><span data-stu-id="761a1-167">System.DateTime</span></span>

### <span data-ttu-id="761a1-168">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="761a1-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="761a1-169">System.object</span><span class="sxs-lookup"><span data-stu-id="761a1-169">System.Int32</span></span>

### <span data-ttu-id="761a1-170">System.object []</span><span class="sxs-lookup"><span data-stu-id="761a1-170">System.String[]</span></span>

## <span data-ttu-id="761a1-171">輸出</span><span class="sxs-lookup"><span data-stu-id="761a1-171">OUTPUTS</span></span>

### <span data-ttu-id="761a1-172">PSGalleryImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="761a1-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="761a1-173">筆記</span><span class="sxs-lookup"><span data-stu-id="761a1-173">NOTES</span></span>

## <span data-ttu-id="761a1-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="761a1-174">RELATED LINKS</span></span>
