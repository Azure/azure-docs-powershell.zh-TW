---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/update-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Update-AzGalleryImageDefinition.md
ms.openlocfilehash: 09871f6d7876b5f197af515f531c85b8bf6a3d9b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906938"
---
# <span data-ttu-id="39a30-101">Update-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="39a30-101">Update-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="39a30-102">簡介</span><span class="sxs-lookup"><span data-stu-id="39a30-102">SYNOPSIS</span></span>
<span data-ttu-id="39a30-103">更新圖庫圖像定義。</span><span class="sxs-lookup"><span data-stu-id="39a30-103">Update a gallery image definition.</span></span>

## <span data-ttu-id="39a30-104">語法</span><span class="sxs-lookup"><span data-stu-id="39a30-104">SYNTAX</span></span>

### <span data-ttu-id="39a30-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="39a30-105">DefaultParameter (Default)</span></span>
```
Update-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Description <String>] [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>]
 [-MinimumMemory <Int32>] [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>]
 [-PrivacyStatementUri <String>] [-PurchasePlanName <String>] [-PurchasePlanProduct <String>]
 [-PurchasePlanPublisher <String>] [-ReleaseNoteUri <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39a30-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="39a30-106">ResourceIdParameter</span></span>
```
Update-AzGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="39a30-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="39a30-107">ObjectParameter</span></span>
```
Update-AzGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-DisallowedDiskType <String[]>] [-EndOfLifeDate <DateTime>] [-Eula <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39a30-108">描述</span><span class="sxs-lookup"><span data-stu-id="39a30-108">DESCRIPTION</span></span>
<span data-ttu-id="39a30-109">更新圖庫圖像定義。</span><span class="sxs-lookup"><span data-stu-id="39a30-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="39a30-110">例子</span><span class="sxs-lookup"><span data-stu-id="39a30-110">EXAMPLES</span></span>

### <span data-ttu-id="39a30-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="39a30-111">Example 1</span></span>
```powershell
PS C:\> Update-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="39a30-112">更新圖庫圖像定義。</span><span class="sxs-lookup"><span data-stu-id="39a30-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="39a30-113">參數</span><span class="sxs-lookup"><span data-stu-id="39a30-113">PARAMETERS</span></span>

### <span data-ttu-id="39a30-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="39a30-114">-AsJob</span></span>
<span data-ttu-id="39a30-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="39a30-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="39a30-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a30-116">-DefaultProfile</span></span>
<span data-ttu-id="39a30-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="39a30-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39a30-118">-描述</span><span class="sxs-lookup"><span data-stu-id="39a30-118">-Description</span></span>
<span data-ttu-id="39a30-119">圖庫圖像定義資源的描述。</span><span class="sxs-lookup"><span data-stu-id="39a30-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="39a30-120">-DisallowedType</span><span class="sxs-lookup"><span data-stu-id="39a30-120">-DisallowedDiskType</span></span>
<span data-ttu-id="39a30-121">不允許的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="39a30-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="39a30-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="39a30-122">-EndOfLifeDate</span></span>
<span data-ttu-id="39a30-123">圖庫圖像定義的生命循環結束日期</span><span class="sxs-lookup"><span data-stu-id="39a30-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="39a30-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="39a30-124">-Eula</span></span>
<span data-ttu-id="39a30-125">圖庫圖像定義的 Eula 協定。</span><span class="sxs-lookup"><span data-stu-id="39a30-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="39a30-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="39a30-126">-GalleryName</span></span>
<span data-ttu-id="39a30-127">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="39a30-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="39a30-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="39a30-128">-InputObject</span></span>
<span data-ttu-id="39a30-129">PS 圖庫圖像定義物件。</span><span class="sxs-lookup"><span data-stu-id="39a30-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="39a30-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="39a30-130">-MaximumMemory</span></span>
<span data-ttu-id="39a30-131">建議記憶體的最大值</span><span class="sxs-lookup"><span data-stu-id="39a30-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="39a30-132">-MaximumVPV</span><span class="sxs-lookup"><span data-stu-id="39a30-132">-MaximumVCPU</span></span>
<span data-ttu-id="39a30-133">建議 CPU 核心的最大值</span><span class="sxs-lookup"><span data-stu-id="39a30-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="39a30-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="39a30-134">-MinimumMemory</span></span>
<span data-ttu-id="39a30-135">建議記憶體的最小值</span><span class="sxs-lookup"><span data-stu-id="39a30-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="39a30-136">-MinimumVPV</span><span class="sxs-lookup"><span data-stu-id="39a30-136">-MinimumVCPU</span></span>
<span data-ttu-id="39a30-137">建議 CPU 核心的最小</span><span class="sxs-lookup"><span data-stu-id="39a30-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="39a30-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="39a30-138">-Name</span></span>
<span data-ttu-id="39a30-139">圖庫圖像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="39a30-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="39a30-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="39a30-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="39a30-141">隱私權聲明 uri。</span><span class="sxs-lookup"><span data-stu-id="39a30-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="39a30-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="39a30-142">-PurchasePlanName</span></span>
<span data-ttu-id="39a30-143">購買計畫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="39a30-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="39a30-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="39a30-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="39a30-145">購買方案的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="39a30-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="39a30-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="39a30-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="39a30-147">購買計畫的發行者識別碼。</span><span class="sxs-lookup"><span data-stu-id="39a30-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="39a30-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="39a30-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="39a30-149">版本資訊 uri。</span><span class="sxs-lookup"><span data-stu-id="39a30-149">The release note uri.</span></span>

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

### <span data-ttu-id="39a30-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39a30-150">-ResourceGroupName</span></span>
<span data-ttu-id="39a30-151">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="39a30-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="39a30-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="39a30-152">-ResourceId</span></span>
<span data-ttu-id="39a30-153">影像定義的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="39a30-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="39a30-154">-標記</span><span class="sxs-lookup"><span data-stu-id="39a30-154">-Tag</span></span>
<span data-ttu-id="39a30-155">資源標記</span><span class="sxs-lookup"><span data-stu-id="39a30-155">Resource tags</span></span>

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

### <span data-ttu-id="39a30-156">-確認</span><span class="sxs-lookup"><span data-stu-id="39a30-156">-Confirm</span></span>
<span data-ttu-id="39a30-157">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="39a30-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39a30-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39a30-158">-WhatIf</span></span>
<span data-ttu-id="39a30-159">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="39a30-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39a30-160">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39a30-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39a30-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a30-161">CommonParameters</span></span>
<span data-ttu-id="39a30-162">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="39a30-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a30-163">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39a30-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a30-164">輸入</span><span class="sxs-lookup"><span data-stu-id="39a30-164">INPUTS</span></span>

### <span data-ttu-id="39a30-165">System.String</span><span class="sxs-lookup"><span data-stu-id="39a30-165">System.String</span></span>

### <span data-ttu-id="39a30-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="39a30-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="39a30-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="39a30-167">System.DateTime</span></span>

### <span data-ttu-id="39a30-168">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="39a30-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="39a30-169">System.Int32</span><span class="sxs-lookup"><span data-stu-id="39a30-169">System.Int32</span></span>

### <span data-ttu-id="39a30-170">System.String[]</span><span class="sxs-lookup"><span data-stu-id="39a30-170">System.String[]</span></span>

## <span data-ttu-id="39a30-171">輸出</span><span class="sxs-lookup"><span data-stu-id="39a30-171">OUTPUTS</span></span>

### <span data-ttu-id="39a30-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="39a30-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="39a30-173">筆記</span><span class="sxs-lookup"><span data-stu-id="39a30-173">NOTES</span></span>

## <span data-ttu-id="39a30-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="39a30-174">RELATED LINKS</span></span>
