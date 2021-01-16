---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 5e50ad3dc1ce2396dfb7a2b498efc82c4e95e430
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98284716"
---
# <span data-ttu-id="932a8-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="932a8-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="932a8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="932a8-102">SYNOPSIS</span></span>
<span data-ttu-id="932a8-103">更新 Windows IoT 裝置服務的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="932a8-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="932a8-104">修改屬性的一般模式是檢索 Windows IoT 裝置服務中繼資料與安全性中繼資料，然後將它們與新主體中修改過的值合併，以更新 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="932a8-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="932a8-105">句法</span><span class="sxs-lookup"><span data-stu-id="932a8-105">SYNTAX</span></span>

### <span data-ttu-id="932a8-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="932a8-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="932a8-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="932a8-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="932a8-108">說明</span><span class="sxs-lookup"><span data-stu-id="932a8-108">DESCRIPTION</span></span>
<span data-ttu-id="932a8-109">更新 Windows IoT 裝置服務的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="932a8-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="932a8-110">修改屬性的一般模式是檢索 Windows IoT 裝置服務中繼資料與安全性中繼資料，然後將它們與新主體中修改過的值合併，以更新 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="932a8-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="932a8-111">示例</span><span class="sxs-lookup"><span data-stu-id="932a8-111">EXAMPLES</span></span>

### <span data-ttu-id="932a8-112">範例1：依名稱更新 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="932a8-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="932a8-113">這個命令會依名稱更新 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="932a8-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="932a8-114">範例2：依管道更新 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="932a8-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="932a8-115">這個命令會依管道更新 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="932a8-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="932a8-116">參數</span><span class="sxs-lookup"><span data-stu-id="932a8-116">PARAMETERS</span></span>

### <span data-ttu-id="932a8-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="932a8-117">-AdminDomainName</span></span>
<span data-ttu-id="932a8-118">Windows IoT 裝置服務 OEM AAD 網域</span><span class="sxs-lookup"><span data-stu-id="932a8-118">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="932a8-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="932a8-119">-BillingDomainName</span></span>
<span data-ttu-id="932a8-120">Windows IoT 裝置服務 ODM AAD 網域</span><span class="sxs-lookup"><span data-stu-id="932a8-120">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="932a8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="932a8-121">-DefaultProfile</span></span>
<span data-ttu-id="932a8-122">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="932a8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="932a8-123">-Etag</span><span class="sxs-lookup"><span data-stu-id="932a8-123">-Etag</span></span>
<span data-ttu-id="932a8-124">*不* 需要 Etag 欄位。</span><span class="sxs-lookup"><span data-stu-id="932a8-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="932a8-125">如果它是在回應內文中提供，則它也必須以標頭的形式提供給每個標準 ETag 慣例。</span><span class="sxs-lookup"><span data-stu-id="932a8-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="932a8-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="932a8-126">-IfMatch</span></span>
<span data-ttu-id="932a8-127">Windows IoT 裝置服務的 ETag。</span><span class="sxs-lookup"><span data-stu-id="932a8-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="932a8-128">請勿指定建立全新的 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="932a8-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="932a8-129">需要更新現有的 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="932a8-129">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="932a8-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="932a8-130">-InputObject</span></span>
<span data-ttu-id="932a8-131">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="932a8-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="932a8-132">-位置</span><span class="sxs-lookup"><span data-stu-id="932a8-132">-Location</span></span>
<span data-ttu-id="932a8-133">資源所在的 Azure 地區</span><span class="sxs-lookup"><span data-stu-id="932a8-133">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="932a8-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="932a8-134">-Name</span></span>
<span data-ttu-id="932a8-135">Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="932a8-135">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932a8-136">-記事</span><span class="sxs-lookup"><span data-stu-id="932a8-136">-Note</span></span>
<span data-ttu-id="932a8-137">Windows IoT Device Service 記事。</span><span class="sxs-lookup"><span data-stu-id="932a8-137">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="932a8-138">數量</span><span class="sxs-lookup"><span data-stu-id="932a8-138">-Quantity</span></span>
<span data-ttu-id="932a8-139">Windows IoT 裝置服務裝置配置，</span><span class="sxs-lookup"><span data-stu-id="932a8-139">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="932a8-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="932a8-140">-ResourceGroupName</span></span>
<span data-ttu-id="932a8-141">包含 Windows IoT 裝置服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="932a8-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932a8-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="932a8-142">-SubscriptionId</span></span>
<span data-ttu-id="932a8-143">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="932a8-143">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="932a8-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="932a8-144">-Tag</span></span>
<span data-ttu-id="932a8-145">資源標記。</span><span class="sxs-lookup"><span data-stu-id="932a8-145">Resource tags.</span></span>

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

### <span data-ttu-id="932a8-146">-確認</span><span class="sxs-lookup"><span data-stu-id="932a8-146">-Confirm</span></span>
<span data-ttu-id="932a8-147">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="932a8-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="932a8-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="932a8-148">-WhatIf</span></span>
<span data-ttu-id="932a8-149">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="932a8-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="932a8-150">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="932a8-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="932a8-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="932a8-151">CommonParameters</span></span>
<span data-ttu-id="932a8-152">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="932a8-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="932a8-153">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="932a8-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="932a8-154">輸入</span><span class="sxs-lookup"><span data-stu-id="932a8-154">INPUTS</span></span>

### <span data-ttu-id="932a8-155">IWindowsIotServicesIdentity （WindowsIotServices）的</span><span class="sxs-lookup"><span data-stu-id="932a8-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="932a8-156">輸出</span><span class="sxs-lookup"><span data-stu-id="932a8-156">OUTPUTS</span></span>

### <span data-ttu-id="932a8-157">IDeviceService （WindowsIotServices）。 Api20190601。</span><span class="sxs-lookup"><span data-stu-id="932a8-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="932a8-158">筆記</span><span class="sxs-lookup"><span data-stu-id="932a8-158">NOTES</span></span>

<span data-ttu-id="932a8-159">別名</span><span class="sxs-lookup"><span data-stu-id="932a8-159">ALIASES</span></span>

<span data-ttu-id="932a8-160">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="932a8-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="932a8-161">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="932a8-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="932a8-162">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="932a8-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="932a8-163">INPUTOBJECT <IWindowsIotServicesIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="932a8-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="932a8-164">`[DeviceName <String>]`： Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="932a8-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="932a8-165">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="932a8-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="932a8-166">`[ResourceGroupName <String>]`：包含 Windows IoT 裝置服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="932a8-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="932a8-167">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="932a8-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="932a8-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="932a8-168">RELATED LINKS</span></span>

