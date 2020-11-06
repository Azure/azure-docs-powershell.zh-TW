---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/New-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 8dcfe4adedd7da375e888dade108125d7899d7d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456147"
---
# <span data-ttu-id="9871c-101">New-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="9871c-101">New-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="9871c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9871c-102">SYNOPSIS</span></span>
<span data-ttu-id="9871c-103">建立圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="9871c-103">Create a gallery image definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9871c-104">句法</span><span class="sxs-lookup"><span data-stu-id="9871c-104">SYNTAX</span></span>

```
New-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [-Name] <String>
 [-AsJob] [-Location] <String> -Publisher <String> -Offer <String> -Sku <String>
 -OsState <OperatingSystemStateTypes> -OsType <OperatingSystemTypes> [-Description <String>] [-Eula <String>]
 [-PrivacyStatementUri <String>] [-ReleaseNoteUri <String>] [-EndOfLifeDate <DateTime>] [-Tag <Hashtable>]
 [-MinimumVCPU <Int32>] [-MaximumVCPU <Int32>] [-MinimumMemory <Int32>] [-MaximumMemory <Int32>]
 [-DisallowedDiskType <String[]>] [-PurchasePlanName <String>] [-PurchasePlanPublisher <String>]
 [-PurchasePlanProduct <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9871c-105">說明</span><span class="sxs-lookup"><span data-stu-id="9871c-105">DESCRIPTION</span></span>
<span data-ttu-id="9871c-106">建立圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="9871c-106">Create a gallery image definition.</span></span>

## <span data-ttu-id="9871c-107">示例</span><span class="sxs-lookup"><span data-stu-id="9871c-107">EXAMPLES</span></span>

### <span data-ttu-id="9871c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="9871c-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmGalleryImageDefinition -ResourceGroupName $resourceGroupName -GalleryName $galleryName -Name $galleryImageDefinitionName -Location $location -Publisher $publisherName -Offer $offerName -Sku $skuName -OsState "Generalized" -OsType "Linux" -Description $description -Eula $eula -PrivacyStatementUri $privacyStatementUri -ReleaseNoteUri $releaseNoteUri -DisallowedDiskType $disallowedDiskTypes -EndOfLifeDate $endOfLifeDate -MinimumMemory $minMemory -MaximumMemory $maxMemory -MinimumVCPU $minVCPU -MaximumVCPU $maxVCPU -PurchasePlanName $purchasePlanName -PurchasePlanProduct $purchasePlanProduct -PurchasePlanPublisher $purchasePlanPublisher
```

<span data-ttu-id="9871c-109">建立圖庫影像定義。</span><span class="sxs-lookup"><span data-stu-id="9871c-109">Create a gallery image definition.</span></span>

## <span data-ttu-id="9871c-110">參數</span><span class="sxs-lookup"><span data-stu-id="9871c-110">PARAMETERS</span></span>

### <span data-ttu-id="9871c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9871c-111">-AsJob</span></span>
<span data-ttu-id="9871c-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9871c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9871c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9871c-113">-DefaultProfile</span></span>
<span data-ttu-id="9871c-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9871c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9871c-115">-描述</span><span class="sxs-lookup"><span data-stu-id="9871c-115">-Description</span></span>
<span data-ttu-id="9871c-116">圖庫影像定義資源的描述。</span><span class="sxs-lookup"><span data-stu-id="9871c-116">The description of the gallery image Definition resource.</span></span> 

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

### <span data-ttu-id="9871c-117">-DisallowedDiskType</span><span class="sxs-lookup"><span data-stu-id="9871c-117">-DisallowedDiskType</span></span>
<span data-ttu-id="9871c-118">非許可的磁片類型。</span><span class="sxs-lookup"><span data-stu-id="9871c-118">The disallowed disk types.</span></span>

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

### <span data-ttu-id="9871c-119">-EndOfLifeDate</span><span class="sxs-lookup"><span data-stu-id="9871c-119">-EndOfLifeDate</span></span>
<span data-ttu-id="9871c-120">圖庫影像定義的生命循環結束日期</span><span class="sxs-lookup"><span data-stu-id="9871c-120">The end of life date of the gallery Image Definition</span></span>

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

### <span data-ttu-id="9871c-121">-Eula</span><span class="sxs-lookup"><span data-stu-id="9871c-121">-Eula</span></span>
<span data-ttu-id="9871c-122">畫廊影像定義的 Eula 合約。</span><span class="sxs-lookup"><span data-stu-id="9871c-122">The Eula agreement for the gallery Image Definition.</span></span>

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

### <span data-ttu-id="9871c-123">-GalleryName</span><span class="sxs-lookup"><span data-stu-id="9871c-123">-GalleryName</span></span>
<span data-ttu-id="9871c-124">圖庫的名稱。</span><span class="sxs-lookup"><span data-stu-id="9871c-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="9871c-125">-位置</span><span class="sxs-lookup"><span data-stu-id="9871c-125">-Location</span></span>
<span data-ttu-id="9871c-126">資源位置</span><span class="sxs-lookup"><span data-stu-id="9871c-126">Resource location</span></span>

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

### <span data-ttu-id="9871c-127">-MaximumMemory</span><span class="sxs-lookup"><span data-stu-id="9871c-127">-MaximumMemory</span></span>
<span data-ttu-id="9871c-128">建議的記憶體上限</span><span class="sxs-lookup"><span data-stu-id="9871c-128">The maximum of the recommended memory</span></span>

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

### <span data-ttu-id="9871c-129">-MaximumVCPU</span><span class="sxs-lookup"><span data-stu-id="9871c-129">-MaximumVCPU</span></span>
<span data-ttu-id="9871c-130">建議的 CPU 核心最大值</span><span class="sxs-lookup"><span data-stu-id="9871c-130">The maximum of the recommended CPU core</span></span>

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

### <span data-ttu-id="9871c-131">-MinimumMemory</span><span class="sxs-lookup"><span data-stu-id="9871c-131">-MinimumMemory</span></span>
<span data-ttu-id="9871c-132">建議的記憶體最小值</span><span class="sxs-lookup"><span data-stu-id="9871c-132">The minimum of the recommended memory</span></span>

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

### <span data-ttu-id="9871c-133">-MinimumVCPU</span><span class="sxs-lookup"><span data-stu-id="9871c-133">-MinimumVCPU</span></span>
<span data-ttu-id="9871c-134">建議的 CPU 核心最小值</span><span class="sxs-lookup"><span data-stu-id="9871c-134">The minimum of the recommended CPU core</span></span>

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

### <span data-ttu-id="9871c-135">-名稱</span><span class="sxs-lookup"><span data-stu-id="9871c-135">-Name</span></span>
<span data-ttu-id="9871c-136">圖庫影像定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="9871c-136">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="9871c-137">-優惠</span><span class="sxs-lookup"><span data-stu-id="9871c-137">-Offer</span></span>
<span data-ttu-id="9871c-138">圖庫影像定義優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="9871c-138">The name of the gallery Image Definition offer.</span></span>

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

### <span data-ttu-id="9871c-139">-OsState</span><span class="sxs-lookup"><span data-stu-id="9871c-139">-OsState</span></span>
<span data-ttu-id="9871c-140">OS 的狀態</span><span class="sxs-lookup"><span data-stu-id="9871c-140">The state of OS</span></span>

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

### <span data-ttu-id="9871c-141">-OsType</span><span class="sxs-lookup"><span data-stu-id="9871c-141">-OsType</span></span>
<span data-ttu-id="9871c-142">OS 類型</span><span class="sxs-lookup"><span data-stu-id="9871c-142">The type of OS</span></span>

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

### <span data-ttu-id="9871c-143">-PrivacyStatementUri</span><span class="sxs-lookup"><span data-stu-id="9871c-143">-PrivacyStatementUri</span></span>
<span data-ttu-id="9871c-144">隱私權語句 uri。</span><span class="sxs-lookup"><span data-stu-id="9871c-144">The privacy statement uri.</span></span>

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

### <span data-ttu-id="9871c-145">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9871c-145">-Publisher</span></span>
<span data-ttu-id="9871c-146">圖庫影像定義發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="9871c-146">The name of the gallery Image Definition publisher.</span></span>

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

### <span data-ttu-id="9871c-147">-PurchasePlanName</span><span class="sxs-lookup"><span data-stu-id="9871c-147">-PurchasePlanName</span></span>
<span data-ttu-id="9871c-148">採購方案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9871c-148">The ID for the purchase plan.</span></span>

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

### <span data-ttu-id="9871c-149">-PurchasePlanProduct</span><span class="sxs-lookup"><span data-stu-id="9871c-149">-PurchasePlanProduct</span></span>
<span data-ttu-id="9871c-150">採購方案的產品識別碼。</span><span class="sxs-lookup"><span data-stu-id="9871c-150">The product ID for the purchase plan.</span></span>

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

### <span data-ttu-id="9871c-151">-PurchasePlanPublisher</span><span class="sxs-lookup"><span data-stu-id="9871c-151">-PurchasePlanPublisher</span></span>
<span data-ttu-id="9871c-152">採購方案的發行者識別碼。</span><span class="sxs-lookup"><span data-stu-id="9871c-152">The publisher ID for the purchase plan.</span></span>

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

### <span data-ttu-id="9871c-153">-ReleaseNoteUri</span><span class="sxs-lookup"><span data-stu-id="9871c-153">-ReleaseNoteUri</span></span>
<span data-ttu-id="9871c-154">版本記事 uri。</span><span class="sxs-lookup"><span data-stu-id="9871c-154">The release note uri.</span></span>

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

### <span data-ttu-id="9871c-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9871c-155">-ResourceGroupName</span></span>
<span data-ttu-id="9871c-156">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9871c-156">The name of the resource group.</span></span>

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

### <span data-ttu-id="9871c-157">-Sku</span><span class="sxs-lookup"><span data-stu-id="9871c-157">-Sku</span></span>
<span data-ttu-id="9871c-158">圖庫影像定義 SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="9871c-158">The name of the gallery Image Definition SKU.</span></span>

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

### <span data-ttu-id="9871c-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="9871c-159">-Tag</span></span>
<span data-ttu-id="9871c-160">資源標記</span><span class="sxs-lookup"><span data-stu-id="9871c-160">Resource tags</span></span>

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

### <span data-ttu-id="9871c-161">-確認</span><span class="sxs-lookup"><span data-stu-id="9871c-161">-Confirm</span></span>
<span data-ttu-id="9871c-162">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9871c-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9871c-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9871c-163">-WhatIf</span></span>
<span data-ttu-id="9871c-164">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9871c-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9871c-165">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9871c-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9871c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9871c-166">CommonParameters</span></span>
<span data-ttu-id="9871c-167">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9871c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9871c-168">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9871c-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9871c-169">輸入</span><span class="sxs-lookup"><span data-stu-id="9871c-169">INPUTS</span></span>

### <span data-ttu-id="9871c-170">System.object</span><span class="sxs-lookup"><span data-stu-id="9871c-170">System.String</span></span>

### <span data-ttu-id="9871c-171">OperatingSystemStateTypes 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="9871c-171">Microsoft.Azure.Management.Compute.Models.OperatingSystemStateTypes</span></span>

### <span data-ttu-id="9871c-172">OperatingSystemTypes 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="9871c-172">Microsoft.Azure.Management.Compute.Models.OperatingSystemTypes</span></span>

### <span data-ttu-id="9871c-173">System.object</span><span class="sxs-lookup"><span data-stu-id="9871c-173">System.DateTime</span></span>

### <span data-ttu-id="9871c-174">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9871c-174">System.Collections.Hashtable</span></span>

### <span data-ttu-id="9871c-175">System.object</span><span class="sxs-lookup"><span data-stu-id="9871c-175">System.Int32</span></span>

### <span data-ttu-id="9871c-176">System.object []</span><span class="sxs-lookup"><span data-stu-id="9871c-176">System.String[]</span></span>

## <span data-ttu-id="9871c-177">輸出</span><span class="sxs-lookup"><span data-stu-id="9871c-177">OUTPUTS</span></span>

### <span data-ttu-id="9871c-178">PSGalleryImage 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="9871c-178">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="9871c-179">筆記</span><span class="sxs-lookup"><span data-stu-id="9871c-179">NOTES</span></span>

## <span data-ttu-id="9871c-180">相關連結</span><span class="sxs-lookup"><span data-stu-id="9871c-180">RELATED LINKS</span></span>
