---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 445029c41e27cce14bff2ac14d826adf28f3c9ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623427"
---
# <span data-ttu-id="ddc63-101">Update-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="ddc63-101">Update-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="ddc63-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ddc63-102">SYNOPSIS</span></span>
<span data-ttu-id="ddc63-103">更新圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="ddc63-103">Update a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ddc63-104">句法</span><span class="sxs-lookup"><span data-stu-id="ddc63-104">SYNTAX</span></span>

### <span data-ttu-id="ddc63-105">DefaultParameter (預設) </span><span class="sxs-lookup"><span data-stu-id="ddc63-105">DefaultParameter (Default)</span></span>
```
Update-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-AsJob] [-Description <String>] [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>]
 [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>]
 [-MinimumMemory <Int32>] [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>]
 [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddc63-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ddc63-106">ResourceIdParameter</span></span>
```
Update-AzureRmGalleryImageDefinition [-ResourceId] <String> [-AsJob] [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ddc63-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="ddc63-107">ObjectParameter</span></span>
```
Update-AzureRmGalleryImageDefinition [-InputObject] <PSGalleryImage> [-AsJob] [-Description <String>]
 [-Eula <String>] [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>]
 [-Tag <Hashtable>] [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>]
 [-MaximumMemory <Int32>] [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>]
 [-PurchasePlanPublisher <String>] [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddc63-108">說明</span><span class="sxs-lookup"><span data-stu-id="ddc63-108">DESCRIPTION</span></span>
<span data-ttu-id="ddc63-109">更新圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="ddc63-109">Update a gallery image definition.</span></span>

## <span data-ttu-id="ddc63-110">示例</span><span class="sxs-lookup"><span data-stu-id="ddc63-110">EXAMPLES</span></span>

### <span data-ttu-id="ddc63-111">範例1</span><span class="sxs-lookup"><span data-stu-id="ddc63-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="ddc63-112">更新圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="ddc63-112">Update a gallery image definition.</span></span>

## <span data-ttu-id="ddc63-113">參數</span><span class="sxs-lookup"><span data-stu-id="ddc63-113">PARAMETERS</span></span>

### <span data-ttu-id="ddc63-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ddc63-114">-AsJob</span></span>
<span data-ttu-id="ddc63-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="ddc63-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ddc63-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddc63-116">-DefaultProfile</span></span>
<span data-ttu-id="ddc63-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ddc63-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddc63-118">-描述</span><span class="sxs-lookup"><span data-stu-id="ddc63-118">-Description</span></span>
<span data-ttu-id="ddc63-119">圖庫影像定義資源的描述。</span><span class="sxs-lookup"><span data-stu-id="ddc63-119">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="ddc63-120">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="ddc63-120">-DisallowedDiskType</span></span>
<span data-ttu-id="ddc63-121">非許可的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="ddc63-121">The disallowed disk types.</span></span>

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

### <span data-ttu-id="ddc63-122">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="ddc63-122">-EndOfLifeDate</span></span>
<span data-ttu-id="ddc63-123">圖庫影像定義的生命循環結束日期</span><span class="sxs-lookup"><span data-stu-id="ddc63-123">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="ddc63-124">-Eula</span><span class="sxs-lookup"><span data-stu-id="ddc63-124">-Eula</span></span>
<span data-ttu-id="ddc63-125">畫廊影像定義的 Eula 合約。</span><span class="sxs-lookup"><span data-stu-id="ddc63-125">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="ddc63-126">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="ddc63-126">-GalleryName</span></span>
<span data-ttu-id="ddc63-127">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddc63-127">The name of the gallery.</span></span>

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

### <span data-ttu-id="ddc63-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddc63-128">-InputObject</span></span>
<span data-ttu-id="ddc63-129">PS 圖庫影像定義物件。</span><span class="sxs-lookup"><span data-stu-id="ddc63-129">The PS Gallery Image Definition Object.</span></span>

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

### <span data-ttu-id="ddc63-130">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="ddc63-130">-MaximumMemory</span></span>
<span data-ttu-id="ddc63-131">建議的記憶體上限</span><span class="sxs-lookup"><span data-stu-id="ddc63-131">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="ddc63-132">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="ddc63-132">-MaximumVCPU</span></span>
<span data-ttu-id="ddc63-133">建議的 CPU 核心最大值</span><span class="sxs-lookup"><span data-stu-id="ddc63-133">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="ddc63-134">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="ddc63-134">-MinimumMemory</span></span>
<span data-ttu-id="ddc63-135">建議的記憶體最小值</span><span class="sxs-lookup"><span data-stu-id="ddc63-135">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="ddc63-136">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="ddc63-136">-MinimumVCPU</span></span>
<span data-ttu-id="ddc63-137">建議的 CPU 核心最小值</span><span class="sxs-lookup"><span data-stu-id="ddc63-137">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="ddc63-138">-名稱</span><span class="sxs-lookup"><span data-stu-id="ddc63-138">-Name</span></span>
<span data-ttu-id="ddc63-139">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddc63-139">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="ddc63-140">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="ddc63-140">-PrivacyStatementUri</span></span>
<span data-ttu-id="ddc63-141">隱私權語句 uri。</span><span class="sxs-lookup"><span data-stu-id="ddc63-141">The privacy statement uri.</span></span>

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

### <span data-ttu-id="ddc63-142">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="ddc63-142">-PurchasePlanName</span></span>
<span data-ttu-id="ddc63-143">採購方案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ddc63-143">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ddc63-144">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="ddc63-144">-PurchasePlanProduct</span></span>
<span data-ttu-id="ddc63-145">採購方案的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="ddc63-145">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ddc63-146">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="ddc63-146">-PurchasePlanPublisher</span></span>
<span data-ttu-id="ddc63-147">採購方案的發行者識別碼。</span><span class="sxs-lookup"><span data-stu-id="ddc63-147">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="ddc63-148">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="ddc63-148">-ReleaseNoteUri</span></span>
<span data-ttu-id="ddc63-149">版本記事 uri。</span><span class="sxs-lookup"><span data-stu-id="ddc63-149">The release note uri.</span></span>

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

### <span data-ttu-id="ddc63-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddc63-150">-ResourceGroupName</span></span>
<span data-ttu-id="ddc63-151">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ddc63-151">The name of the resource group.</span></span>

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

### <span data-ttu-id="ddc63-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddc63-152">-ResourceId</span></span>
<span data-ttu-id="ddc63-153">影像定義的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="ddc63-153">The resource ID for the image definition</span></span>

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

### <span data-ttu-id="ddc63-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="ddc63-154">-Tag</span></span>
<span data-ttu-id="ddc63-155">資源標記</span><span class="sxs-lookup"><span data-stu-id="ddc63-155">Resource tags</span></span>

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

### <span data-ttu-id="ddc63-156">-確認</span><span class="sxs-lookup"><span data-stu-id="ddc63-156">-Confirm</span></span>
<span data-ttu-id="ddc63-157">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ddc63-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddc63-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddc63-158">-WhatIf</span></span>
<span data-ttu-id="ddc63-159">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ddc63-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddc63-160">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ddc63-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddc63-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddc63-161">CommonParameters</span></span>
<span data-ttu-id="ddc63-162">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ddc63-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddc63-163">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ddc63-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddc63-164">輸入</span><span class="sxs-lookup"><span data-stu-id="ddc63-164">INPUTS</span></span>

### <span data-ttu-id="ddc63-165">System.object</span><span class="sxs-lookup"><span data-stu-id="ddc63-165">System.String</span></span>

### <span data-ttu-id="ddc63-166">PSGalleryImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="ddc63-166">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

### <span data-ttu-id="ddc63-167">System.object</span><span class="sxs-lookup"><span data-stu-id="ddc63-167">System.DateTime</span></span>

### <span data-ttu-id="ddc63-168">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ddc63-168">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ddc63-169">System.object</span><span class="sxs-lookup"><span data-stu-id="ddc63-169">System.Int32</span></span>

### <span data-ttu-id="ddc63-170">System.object []</span><span class="sxs-lookup"><span data-stu-id="ddc63-170">System.String[]</span></span>

## <span data-ttu-id="ddc63-171">輸出</span><span class="sxs-lookup"><span data-stu-id="ddc63-171">OUTPUTS</span></span>

### <span data-ttu-id="ddc63-172">PSGalleryImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="ddc63-172">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="ddc63-173">筆記</span><span class="sxs-lookup"><span data-stu-id="ddc63-173">NOTES</span></span>

## <span data-ttu-id="ddc63-174">相關連結</span><span class="sxs-lookup"><span data-stu-id="ddc63-174">RELATED LINKS</span></span>