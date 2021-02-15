---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/new-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/New-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 4da60a6d4083992f843121cb141a453b4ef3b4b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100142331"
---
# <span data-ttu-id="338f6-101">New-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="338f6-101">New-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="338f6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="338f6-102">SYNOPSIS</span></span>
<span data-ttu-id="338f6-103">建立或更新 Windows IoT 裝置服務的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="338f6-103">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="338f6-104">修改屬性的一般模式是檢索 Windows IoT 裝置服務中繼資料與安全性中繼資料，然後將它們與新主體中修改過的值合併，以更新 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="338f6-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="338f6-105">句法</span><span class="sxs-lookup"><span data-stu-id="338f6-105">SYNTAX</span></span>

```
New-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="338f6-106">說明</span><span class="sxs-lookup"><span data-stu-id="338f6-106">DESCRIPTION</span></span>
<span data-ttu-id="338f6-107">建立或更新 Windows IoT 裝置服務的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="338f6-107">Create or update the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="338f6-108">修改屬性的一般模式是檢索 Windows IoT 裝置服務中繼資料與安全性中繼資料，然後將它們與新主體中修改過的值合併，以更新 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="338f6-108">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="338f6-109">示例</span><span class="sxs-lookup"><span data-stu-id="338f6-109">EXAMPLES</span></span>

### <span data-ttu-id="338f6-110">範例1：建立新的 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="338f6-110">Example 1: Create a new Windows IoT services</span></span>
```powershell
PS C:\> New-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "6a00eee9-0000-0700-0000-5fab82870000"
```

<span data-ttu-id="338f6-111">這個命令會建立新的 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="338f6-111">This command creates a new Windows IoT services.</span></span>

## <span data-ttu-id="338f6-112">參數</span><span class="sxs-lookup"><span data-stu-id="338f6-112">PARAMETERS</span></span>

### <span data-ttu-id="338f6-113">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="338f6-113">-AdminDomainName</span></span>
<span data-ttu-id="338f6-114">Windows IoT 裝置服務 OEM AAD 網域</span><span class="sxs-lookup"><span data-stu-id="338f6-114">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="338f6-115">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="338f6-115">-BillingDomainName</span></span>
<span data-ttu-id="338f6-116">Windows IoT 裝置服務 ODM AAD 網域</span><span class="sxs-lookup"><span data-stu-id="338f6-116">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="338f6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="338f6-117">-DefaultProfile</span></span>
<span data-ttu-id="338f6-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="338f6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="338f6-119">-Etag</span><span class="sxs-lookup"><span data-stu-id="338f6-119">-Etag</span></span>
<span data-ttu-id="338f6-120">*不* 需要 Etag 欄位。</span><span class="sxs-lookup"><span data-stu-id="338f6-120">The Etag field is *not* required.</span></span>
<span data-ttu-id="338f6-121">如果它是在回應內文中提供，則它也必須以標頭的形式提供給每個標準 ETag 慣例。</span><span class="sxs-lookup"><span data-stu-id="338f6-121">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="338f6-122">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="338f6-122">-IfMatch</span></span>
<span data-ttu-id="338f6-123">Windows IoT 裝置服務的 ETag。</span><span class="sxs-lookup"><span data-stu-id="338f6-123">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="338f6-124">請勿指定建立新的 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="338f6-124">Do not specify for creating a new Windows IoT Device Service.</span></span>
<span data-ttu-id="338f6-125">需要更新現有的 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="338f6-125">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="338f6-126">-位置</span><span class="sxs-lookup"><span data-stu-id="338f6-126">-Location</span></span>
<span data-ttu-id="338f6-127">資源所在的 Azure 地區</span><span class="sxs-lookup"><span data-stu-id="338f6-127">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="338f6-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="338f6-128">-Name</span></span>
<span data-ttu-id="338f6-129">Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="338f6-129">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="338f6-130">-記事</span><span class="sxs-lookup"><span data-stu-id="338f6-130">-Note</span></span>
<span data-ttu-id="338f6-131">Windows IoT Device Service 記事。</span><span class="sxs-lookup"><span data-stu-id="338f6-131">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="338f6-132">數量</span><span class="sxs-lookup"><span data-stu-id="338f6-132">-Quantity</span></span>
<span data-ttu-id="338f6-133">Windows IoT 裝置服務裝置配置，</span><span class="sxs-lookup"><span data-stu-id="338f6-133">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="338f6-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="338f6-134">-ResourceGroupName</span></span>
<span data-ttu-id="338f6-135">包含 Windows IoT 裝置服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="338f6-135">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="338f6-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="338f6-136">-SubscriptionId</span></span>
<span data-ttu-id="338f6-137">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="338f6-137">The subscription identifier.</span></span>

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

### <span data-ttu-id="338f6-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="338f6-138">-Tag</span></span>
<span data-ttu-id="338f6-139">資源標記。</span><span class="sxs-lookup"><span data-stu-id="338f6-139">Resource tags.</span></span>

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

### <span data-ttu-id="338f6-140">-確認</span><span class="sxs-lookup"><span data-stu-id="338f6-140">-Confirm</span></span>
<span data-ttu-id="338f6-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="338f6-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="338f6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="338f6-142">-WhatIf</span></span>
<span data-ttu-id="338f6-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="338f6-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="338f6-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="338f6-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="338f6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="338f6-145">CommonParameters</span></span>
<span data-ttu-id="338f6-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="338f6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="338f6-147">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="338f6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="338f6-148">輸入</span><span class="sxs-lookup"><span data-stu-id="338f6-148">INPUTS</span></span>

## <span data-ttu-id="338f6-149">輸出</span><span class="sxs-lookup"><span data-stu-id="338f6-149">OUTPUTS</span></span>

### <span data-ttu-id="338f6-150">IDeviceService （WindowsIotServices）。 Api20190601。</span><span class="sxs-lookup"><span data-stu-id="338f6-150">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="338f6-151">筆記</span><span class="sxs-lookup"><span data-stu-id="338f6-151">NOTES</span></span>

<span data-ttu-id="338f6-152">別名</span><span class="sxs-lookup"><span data-stu-id="338f6-152">ALIASES</span></span>

## <span data-ttu-id="338f6-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="338f6-153">RELATED LINKS</span></span>

