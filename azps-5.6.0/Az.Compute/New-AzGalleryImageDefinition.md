---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzGalleryImageDefinition.md
ms.openlocfilehash: fbfb0a10016d81edcffeb62580b1ca0ff9b5b341
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903314"
---
# <span data-ttu-id="7ac56-101">New-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="7ac56-101">New-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="7ac56-102">簡介</span><span class="sxs-lookup"><span data-stu-id="7ac56-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac56-103">建立圖庫圖像定義。</span><span class="sxs-lookup"><span data-stu-id="7ac56-103">Create a gallery image definition.</span></span>

## <span data-ttu-id="7ac56-104">語法</span><span class="sxs-lookup"><span data-stu-id="7ac56-104">SYNTAX</span></span>

```
New-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String> [-AsJob]
 [-Location] <String> -Publisher <String> -Offer <String> -Sku <String> -OsState <OperatingSystemStateTypes>
 -OsType <OperatingSystemTypes> [-Description <String>] [-DisallowedDiskType <String[]>]
 [-EndOfLifeDate <DateTime>] [-Eula <String>] [-HyperVGeneration <String>] [-MinimumMemory <Int32>]
 [-MinimumVCPU <Int32>] [-MaximumMemory <Int32>] [-MaximumVCPU <Int32>] [-PrivacyStatementUri <String>]
 [-PurchasePlanName <String>] [-PurchasePlanProduct <String>] [-PurchasePlanPublisher <String>]
 [-ReleaseNoteUri <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ac56-105">描述</span><span class="sxs-lookup"><span data-stu-id="7ac56-105">DESCRIPTION</span></span>
<span data-ttu-id="7ac56-106">建立圖庫圖像定義。</span><span class="sxs-lookup"><span data-stu-id="7ac56-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="7ac56-107">例子</span><span class="sxs-lookup"><span data-stu-id="7ac56-107">EXAMPLES</span></span>

### <span data-ttu-id="7ac56-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="7ac56-108">Example 1</span></span>
```powershell
PS C:\> New-AzGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="7ac56-109">建立圖庫圖像定義。</span><span class="sxs-lookup"><span data-stu-id="7ac56-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="7ac56-110">參數</span><span class="sxs-lookup"><span data-stu-id="7ac56-110">PARAMETERS</span></span>

### <span data-ttu-id="7ac56-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7ac56-111">-AsJob</span></span>
<span data-ttu-id="7ac56-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7ac56-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7ac56-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac56-113">-DefaultProfile</span></span>
<span data-ttu-id="7ac56-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="7ac56-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ac56-115">-描述</span><span class="sxs-lookup"><span data-stu-id="7ac56-115">-Description</span></span>
<span data-ttu-id="7ac56-116">圖庫圖像定義資源的描述。</span><span class="sxs-lookup"><span data-stu-id="7ac56-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="7ac56-117">-DisallowedType</span><span class="sxs-lookup"><span data-stu-id="7ac56-117">-DisallowedDiskType</span></span>
<span data-ttu-id="7ac56-118">不允許的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="7ac56-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="7ac56-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="7ac56-119">-EndOfLifeDate</span></span>
<span data-ttu-id="7ac56-120">圖庫圖像定義的生命循環結束日期</span><span class="sxs-lookup"><span data-stu-id="7ac56-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="7ac56-121">-Eula</span><span class="sxs-lookup"><span data-stu-id="7ac56-121">-Eula</span></span>
<span data-ttu-id="7ac56-122">圖庫圖像定義的 Eula 協定。</span><span class="sxs-lookup"><span data-stu-id="7ac56-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="7ac56-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="7ac56-123">-GalleryName</span></span>
<span data-ttu-id="7ac56-124">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ac56-124">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac56-125">-HyperVGeneration</span><span class="sxs-lookup"><span data-stu-id="7ac56-125">-HyperVGeneration</span></span>
<span data-ttu-id="7ac56-126">虛擬機器的超虛擬機器代。</span><span class="sxs-lookup"><span data-stu-id="7ac56-126">The hypervisor generation of the Virtual Machine.</span></span> <span data-ttu-id="7ac56-127">僅適用于作業系統磁片。</span><span class="sxs-lookup"><span data-stu-id="7ac56-127">Applicable to OS disks only.</span></span>  <span data-ttu-id="7ac56-128">允許的值為 V1 和 V2。</span><span class="sxs-lookup"><span data-stu-id="7ac56-128">Allowed values are V1 and V2.</span></span>

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

### <span data-ttu-id="7ac56-129">-位置</span><span class="sxs-lookup"><span data-stu-id="7ac56-129">-Location</span></span>
<span data-ttu-id="7ac56-130">資源位置</span><span class="sxs-lookup"><span data-stu-id="7ac56-130">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac56-131">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="7ac56-131">-MaximumMemory</span></span>
<span data-ttu-id="7ac56-132">建議記憶體的最大值</span><span class="sxs-lookup"><span data-stu-id="7ac56-132">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="7ac56-133">-MaximumVPV</span><span class="sxs-lookup"><span data-stu-id="7ac56-133">-MaximumVCPU</span></span>
<span data-ttu-id="7ac56-134">建議 CPU 核心的最大值</span><span class="sxs-lookup"><span data-stu-id="7ac56-134">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="7ac56-135">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="7ac56-135">-MinimumMemory</span></span>
<span data-ttu-id="7ac56-136">建議記憶體的最小值</span><span class="sxs-lookup"><span data-stu-id="7ac56-136">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="7ac56-137">-MinimumVPV</span><span class="sxs-lookup"><span data-stu-id="7ac56-137">-MinimumVCPU</span></span>
<span data-ttu-id="7ac56-138">建議 CPU 核心的最小</span><span class="sxs-lookup"><span data-stu-id="7ac56-138">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="7ac56-139">-名稱</span><span class="sxs-lookup"><span data-stu-id="7ac56-139">-Name</span></span>
<span data-ttu-id="7ac56-140">圖庫圖像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ac56-140">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GalleryImageDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac56-141">-優惠</span><span class="sxs-lookup"><span data-stu-id="7ac56-141">-Offer</span></span>
<span data-ttu-id="7ac56-142">圖庫圖像定義優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ac56-142">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="7ac56-143">-OsState</span><span class="sxs-lookup"><span data-stu-id="7ac56-143">-OsState</span></span>
<span data-ttu-id="7ac56-144">作業系統狀態</span><span class="sxs-lookup"><span data-stu-id="7ac56-144">The state of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes
Parameter Sets: (All)
Aliases:
Accepted values: Generalized, Specialized

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac56-145">-OsType</span><span class="sxs-lookup"><span data-stu-id="7ac56-145">-OsType</span></span>
<span data-ttu-id="7ac56-146">作業系統類型</span><span class="sxs-lookup"><span data-stu-id="7ac56-146">The type of OS</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Linux

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac56-147">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="7ac56-147">-PrivacyStatementUri</span></span>
<span data-ttu-id="7ac56-148">隱私權聲明 uri。</span><span class="sxs-lookup"><span data-stu-id="7ac56-148">The privacy statement uri.</span></span>

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

### <span data-ttu-id="7ac56-149">-Publisher</span><span class="sxs-lookup"><span data-stu-id="7ac56-149">-Publisher</span></span>
<span data-ttu-id="7ac56-150">圖庫圖像定義發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ac56-150">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="7ac56-151">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="7ac56-151">-PurchasePlanName</span></span>
<span data-ttu-id="7ac56-152">購買計畫的識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ac56-152">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="7ac56-153">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="7ac56-153">-PurchasePlanProduct</span></span>
<span data-ttu-id="7ac56-154">購買方案的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ac56-154">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="7ac56-155">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="7ac56-155">-PurchasePlanPublisher</span></span>
<span data-ttu-id="7ac56-156">購買計畫的發行者識別碼。</span><span class="sxs-lookup"><span data-stu-id="7ac56-156">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="7ac56-157">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="7ac56-157">-ReleaseNoteUri</span></span>
<span data-ttu-id="7ac56-158">版本資訊 uri。</span><span class="sxs-lookup"><span data-stu-id="7ac56-158">The release note uri.</span></span>

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

### <span data-ttu-id="7ac56-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ac56-159">-ResourceGroupName</span></span>
<span data-ttu-id="7ac56-160">資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ac56-160">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac56-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="7ac56-161">-Sku</span></span>
<span data-ttu-id="7ac56-162">圖庫圖像定義 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="7ac56-162">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="7ac56-163">-標記</span><span class="sxs-lookup"><span data-stu-id="7ac56-163">-Tag</span></span>
<span data-ttu-id="7ac56-164">資源標記</span><span class="sxs-lookup"><span data-stu-id="7ac56-164">Resource tags</span></span>

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

### <span data-ttu-id="7ac56-165">-確認</span><span class="sxs-lookup"><span data-stu-id="7ac56-165">-Confirm</span></span>
<span data-ttu-id="7ac56-166">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="7ac56-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ac56-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ac56-167">-WhatIf</span></span>
<span data-ttu-id="7ac56-168">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7ac56-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ac56-169">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7ac56-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ac56-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac56-170">CommonParameters</span></span>
<span data-ttu-id="7ac56-171">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="7ac56-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac56-172">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7ac56-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac56-173">輸入</span><span class="sxs-lookup"><span data-stu-id="7ac56-173">INPUTS</span></span>

### <span data-ttu-id="7ac56-174">System.String</span><span class="sxs-lookup"><span data-stu-id="7ac56-174">System.String</span></span>

### <span data-ttu-id="7ac56-175">Microsoft.Azure.management.Compute.models.OperatingSystemStateTypes</span><span class="sxs-lookup"><span data-stu-id="7ac56-175">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="7ac56-176">Microsoft.Azure.management.Compute.models.OperatingSystemTypes</span><span class="sxs-lookup"><span data-stu-id="7ac56-176">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="7ac56-177">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="7ac56-177">System.DateTime</span></span>

### <span data-ttu-id="7ac56-178">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="7ac56-178">System.Collections.Hashtable</span></span>

### <span data-ttu-id="7ac56-179">System.Int32</span><span class="sxs-lookup"><span data-stu-id="7ac56-179">System.Int32</span></span>

### <span data-ttu-id="7ac56-180">System.String[]</span><span class="sxs-lookup"><span data-stu-id="7ac56-180">System.String[]</span></span>

## <span data-ttu-id="7ac56-181">輸出</span><span class="sxs-lookup"><span data-stu-id="7ac56-181">OUTPUTS</span></span>

### <span data-ttu-id="7ac56-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="7ac56-182">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="7ac56-183">筆記</span><span class="sxs-lookup"><span data-stu-id="7ac56-183">NOTES</span></span>

## <span data-ttu-id="7ac56-184">相關連結</span><span class="sxs-lookup"><span data-stu-id="7ac56-184">RELATED LINKS</span></span>
