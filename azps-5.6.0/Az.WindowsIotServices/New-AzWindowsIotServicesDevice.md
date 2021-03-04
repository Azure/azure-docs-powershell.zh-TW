---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 40256025817e4f840f8d65ff8bdf6bc92c5b3d10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101914237"
---
# <span data-ttu-id="84c58-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="84c58-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="84c58-102">簡介</span><span class="sxs-lookup"><span data-stu-id="84c58-102">SYNOPSIS</span></span>
<span data-ttu-id="84c58-103">建立或更新 Windows IoT 裝置服務的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="84c58-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="84c58-104">修改屬性的一般模式是，要取回 Windows IoT 裝置服務中繼資料和安全性中繼資料，然後將它們與新內體中的修改值合併，以更新 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="84c58-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="84c58-105">語法</span><span class="sxs-lookup"><span data-stu-id="84c58-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="84c58-106">描述</span><span class="sxs-lookup"><span data-stu-id="84c58-106">DESCRIPTION</span></span>
<span data-ttu-id="84c58-107">建立或更新 Windows IoT 裝置服務的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="84c58-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="84c58-108">修改屬性的一般模式是，要取回 Windows IoT 裝置服務中繼資料和安全性中繼資料，然後將它們與新內體中的修改值合併，以更新 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="84c58-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="84c58-109">例子</span><span class="sxs-lookup"><span data-stu-id="84c58-109">EXAMPLES</span></span>

### <span data-ttu-id="84c58-110">範例 1：建立新 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="84c58-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="84c58-111">此命令會建立新的 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="84c58-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="84c58-112">參數</span><span class="sxs-lookup"><span data-stu-id="84c58-112">PARAMETERS</span></span>

### <span data-ttu-id="84c58-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="84c58-113">-AdminDomainName</span></span>
<span data-ttu-id="84c58-114">Windows IoT 裝置服務 OEM AAD 網域</span><span class="sxs-lookup"><span data-stu-id="84c58-114">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="84c58-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="84c58-115">-BillingDomainName</span></span>
<span data-ttu-id="84c58-116">Windows IoT 裝置服務 ODM AAD 網域</span><span class="sxs-lookup"><span data-stu-id="84c58-116">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="84c58-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c58-117">-DefaultProfile</span></span>
<span data-ttu-id="84c58-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="84c58-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c58-119">-Etag</span><span class="sxs-lookup"><span data-stu-id="84c58-119">-Etag</span></span>
<span data-ttu-id="84c58-120">不需要 Etag *欄位。*</span><span class="sxs-lookup"><span data-stu-id="84c58-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="84c58-121">如果這是在回應內內容中提供，也必須根據一般 ETag 慣例提供做為標頭。</span><span class="sxs-lookup"><span data-stu-id="84c58-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="84c58-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="84c58-122">-IfMatch</span></span>
<span data-ttu-id="84c58-123">Windows IoT 裝置服務的 ETag。</span><span class="sxs-lookup"><span data-stu-id="84c58-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="84c58-124">請勿指定要建立新 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="84c58-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="84c58-125">需要更新現有的 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="84c58-125">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="84c58-126">-位置</span><span class="sxs-lookup"><span data-stu-id="84c58-126">-Location</span></span>
<span data-ttu-id="84c58-127">資源所在地的 Azure 區域</span><span class="sxs-lookup"><span data-stu-id="84c58-127">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="84c58-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="84c58-128">-Name</span></span>
<span data-ttu-id="84c58-129">Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="84c58-129">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="84c58-130">-注意</span><span class="sxs-lookup"><span data-stu-id="84c58-130">-Note</span></span>
<span data-ttu-id="84c58-131">Windows IoT 裝置服務附注。</span><span class="sxs-lookup"><span data-stu-id="84c58-131">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="84c58-132">-數量</span><span class="sxs-lookup"><span data-stu-id="84c58-132">-Quantity</span></span>
<span data-ttu-id="84c58-133">Windows IoT 裝置服務裝置配置，</span><span class="sxs-lookup"><span data-stu-id="84c58-133">Windows IoT Device Service device allocation,</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c58-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84c58-134">-ResourceGroupName</span></span>
<span data-ttu-id="84c58-135">包含 Windows IoT 裝置服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="84c58-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="84c58-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="84c58-136">-SubscriptionId</span></span>
<span data-ttu-id="84c58-137">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="84c58-137">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84c58-138">-標記</span><span class="sxs-lookup"><span data-stu-id="84c58-138">-Tag</span></span>
<span data-ttu-id="84c58-139">資源標記。</span><span class="sxs-lookup"><span data-stu-id="84c58-139">Resource tags.</span></span>

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

### <span data-ttu-id="84c58-140">-確認</span><span class="sxs-lookup"><span data-stu-id="84c58-140">-Confirm</span></span>
<span data-ttu-id="84c58-141">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="84c58-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84c58-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84c58-142">-WhatIf</span></span>
<span data-ttu-id="84c58-143">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="84c58-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84c58-144">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="84c58-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84c58-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c58-145">CommonParameters</span></span>
<span data-ttu-id="84c58-146">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="84c58-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c58-147">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84c58-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c58-148">輸入</span><span class="sxs-lookup"><span data-stu-id="84c58-148">INPUTS</span></span>

## <span data-ttu-id="84c58-149">輸出</span><span class="sxs-lookup"><span data-stu-id="84c58-149">OUTPUTS</span></span>

### <span data-ttu-id="84c58-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="84c58-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="84c58-151">筆記</span><span class="sxs-lookup"><span data-stu-id="84c58-151">NOTES</span></span>

<span data-ttu-id="84c58-152">別名</span><span class="sxs-lookup"><span data-stu-id="84c58-152">ALIASES</span></span>

## <span data-ttu-id="84c58-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="84c58-153">RELATED LINKS</span></span>

