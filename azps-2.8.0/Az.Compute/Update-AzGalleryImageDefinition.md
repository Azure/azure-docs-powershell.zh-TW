---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: d0a149f5ee2e03345cd433952d49748886c066ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613100"
---
# <span data-ttu-id="b391e-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="b391e-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="b391e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b391e-102">SYNOPSIS</span></span>
<span data-ttu-id="b391e-103">更新圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="b391e-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="b391e-104">句法</span><span class="sxs-lookup"><span data-stu-id="b391e-104">SYNTAX</span></span>

### <span data-ttu-id="b391e-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="b391e-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b391e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b391e-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b391e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="b391e-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b391e-108">說明</span><span class="sxs-lookup"><span data-stu-id="b391e-108">DESCRIPTION</span></span>
<span data-ttu-id="b391e-109">更新圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="b391e-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="b391e-110">示例</span><span class="sxs-lookup"><span data-stu-id="b391e-110">EXAMPLES</span></span>

### <span data-ttu-id="b391e-111">範例1</span><span class="sxs-lookup"><span data-stu-id="b391e-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="b391e-112">更新圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="b391e-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="b391e-113">參數</span><span class="sxs-lookup"><span data-stu-id="b391e-113">PARAMETERS</span></span>

### <span data-ttu-id="b391e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b391e-114">-AsJob</span></span>
<span data-ttu-id="b391e-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b391e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b391e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b391e-116">-DefaultProfile</span></span>
<span data-ttu-id="b391e-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b391e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b391e-118">-描述</span><span class="sxs-lookup"><span data-stu-id="b391e-118">-Description</span></span>
<span data-ttu-id="b391e-119">圖庫影像定義資源的描述。</span><span class="sxs-lookup"><span data-stu-id="b391e-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="b391e-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="b391e-120">-DisallowedDiskType</span></span>
<span data-ttu-id="b391e-121">非許可的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="b391e-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="b391e-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="b391e-122">-EndOfLifeDate</span></span>
<span data-ttu-id="b391e-123">圖庫影像定義的生命循環結束日期</span><span class="sxs-lookup"><span data-stu-id="b391e-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="b391e-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="b391e-124">-Eula</span></span>
<span data-ttu-id="b391e-125">畫廊影像定義的 Eula 合約。</span><span class="sxs-lookup"><span data-stu-id="b391e-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="b391e-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="b391e-126">-GalleryName</span></span>
<span data-ttu-id="b391e-127">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="b391e-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="b391e-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b391e-128">-InputObject</span></span>
<span data-ttu-id="b391e-129">PS 圖庫影像定義物件。</span><span class="sxs-lookup"><span data-stu-id="b391e-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="b391e-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="b391e-130">-MaximumMemory</span></span>
<span data-ttu-id="b391e-131">建議的記憶體上限</span><span class="sxs-lookup"><span data-stu-id="b391e-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="b391e-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="b391e-132">-MaximumVCPU</span></span>
<span data-ttu-id="b391e-133">建議的 CPU 核心最大值</span><span class="sxs-lookup"><span data-stu-id="b391e-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="b391e-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="b391e-134">-MinimumMemory</span></span>
<span data-ttu-id="b391e-135">建議的記憶體最小值</span><span class="sxs-lookup"><span data-stu-id="b391e-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="b391e-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="b391e-136">-MinimumVCPU</span></span>
<span data-ttu-id="b391e-137">建議的 CPU 核心最小值</span><span class="sxs-lookup"><span data-stu-id="b391e-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="b391e-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="b391e-138">-Name</span></span>
<span data-ttu-id="b391e-139">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="b391e-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="b391e-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="b391e-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="b391e-141">隱私權語句 uri。</span><span class="sxs-lookup"><span data-stu-id="b391e-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="b391e-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="b391e-142">-PurchasePlanName</span></span>
<span data-ttu-id="b391e-143">採購方案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b391e-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="b391e-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="b391e-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="b391e-145">採購方案的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="b391e-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="b391e-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="b391e-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="b391e-147">採購方案的發行者識別碼。</span><span class="sxs-lookup"><span data-stu-id="b391e-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="b391e-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="b391e-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="b391e-149">版本記事 uri。</span><span class="sxs-lookup"><span data-stu-id="b391e-149">The release note uri.</span></span>

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

### <span data-ttu-id="b391e-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b391e-150">-ResourceGroupName</span></span>
<span data-ttu-id="b391e-151">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b391e-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="b391e-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b391e-152">-ResourceId</span></span>
<span data-ttu-id="b391e-153">影像定義的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="b391e-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="b391e-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="b391e-154">-Tag</span></span>
<span data-ttu-id="b391e-155">資源標記</span><span class="sxs-lookup"><span data-stu-id="b391e-155">Resource tags</span></span>

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

### <span data-ttu-id="b391e-156">-確認</span><span class="sxs-lookup"><span data-stu-id="b391e-156">-Confirm</span></span>
<span data-ttu-id="b391e-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="b391e-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b391e-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b391e-158">-WhatIf</span></span>
<span data-ttu-id="b391e-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b391e-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b391e-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b391e-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b391e-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b391e-161">CommonParameters</span></span>
<span data-ttu-id="b391e-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b391e-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b391e-163">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="b391e-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b391e-164">輸入</span><span class="sxs-lookup"><span data-stu-id="b391e-164">INPUTS</span></span>

### <span data-ttu-id="b391e-165">System.object</span><span class="sxs-lookup"><span data-stu-id="b391e-165">System.String</span></span>

### <span data-ttu-id="b391e-166">PSGalleryImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="b391e-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="b391e-167">System.object</span><span class="sxs-lookup"><span data-stu-id="b391e-167">System.DateTime</span></span>

### <span data-ttu-id="b391e-168">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b391e-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="b391e-169">System.object</span><span class="sxs-lookup"><span data-stu-id="b391e-169">System.Int32</span></span>

### <span data-ttu-id="b391e-170">System.object []</span><span class="sxs-lookup"><span data-stu-id="b391e-170">System.String[]</span></span>

## <span data-ttu-id="b391e-171">輸出</span><span class="sxs-lookup"><span data-stu-id="b391e-171">OUTPUTS</span></span>

### <span data-ttu-id="b391e-172">PSGalleryImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="b391e-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="b391e-173">筆記</span><span class="sxs-lookup"><span data-stu-id="b391e-173">NOTES</span></span>

## <span data-ttu-id="b391e-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="b391e-174">RELATED LINKS</span></span>
