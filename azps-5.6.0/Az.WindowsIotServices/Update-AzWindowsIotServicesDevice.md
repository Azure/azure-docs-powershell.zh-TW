---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/update-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Update-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 27eecabc9bb144270b86a26e5128b9a0d63d346b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906818"
---
# <span data-ttu-id="4324f-101">Update-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="4324f-101">Update-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="4324f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="4324f-102">SYNOPSIS</span></span>
<span data-ttu-id="4324f-103">更新 Windows IoT 裝置服務的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="4324f-103">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="4324f-104">修改屬性的一般模式是，要取回 Windows IoT 裝置服務中繼資料和安全性中繼資料，然後將它們與新內體中的修改值合併，以更新 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="4324f-104">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="4324f-105">語法</span><span class="sxs-lookup"><span data-stu-id="4324f-105">SYNTAX</span></span>

### <span data-ttu-id="4324f-106">UpdateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="4324f-106">UpdateExpanded (Default)</span></span>
```
Update-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-IfMatch <String>] [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>]
 [-Location <String>] [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4324f-107">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4324f-107">UpdateViaIdentityExpanded</span></span>
```
Update-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-IfMatch <String>]
 [-AdminDomainName <String>] [-BillingDomainName <String>] [-Etag <String>] [-Location <String>]
 [-Note <String>] [-Quantity <Int64>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4324f-108">描述</span><span class="sxs-lookup"><span data-stu-id="4324f-108">DESCRIPTION</span></span>
<span data-ttu-id="4324f-109">更新 Windows IoT 裝置服務的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="4324f-109">Updates the metadata of a Windows IoT Device Service.</span></span>
<span data-ttu-id="4324f-110">修改屬性的一般模式是，要取回 Windows IoT 裝置服務中繼資料和安全性中繼資料，然後將它們與新內體中的修改值合併，以更新 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="4324f-110">The usual pattern to modify a property is to retrieve the Windows IoT Device Service metadata and security metadata, and then combine them with the modified values in a new body to update the Windows IoT Device Service.</span></span>

## <span data-ttu-id="4324f-111">例子</span><span class="sxs-lookup"><span data-stu-id="4324f-111">EXAMPLES</span></span>

### <span data-ttu-id="4324f-112">範例 1：根據名稱更新 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="4324f-112">Example 1: Update a Windows IoT services by name</span></span>
```powershell
PS C:\> Update-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test -Quantity 10

Location Name    Type                                Etag
-------- ----    ----                                ----
eastus   wsi-t03 Microsoft.WindowsIoT/DeviceServices "5d006a5c-0000-0700-0000-5faa46760000"
```

<span data-ttu-id="4324f-113">此命令會按名稱更新 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="4324f-113">This command updates a Windows IoT services by name.</span></span>

### <span data-ttu-id="4324f-114">範例 2：根據管線更新 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="4324f-114">Example 2: Update a Windows IoT services by pipeline</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -Name wsi-t03 -ResourceGroupName azure-rg-test | Update-AzWindowsIotServicesDevice-Quantity 100 -Tag @{'oper'='update'}

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5d005f5f-0000-0700-0000-5faa46ae0000"
```

<span data-ttu-id="4324f-115">此命令會按管線更新 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="4324f-115">This command updates a Windows IoT services by pipeline.</span></span>

## <span data-ttu-id="4324f-116">參數</span><span class="sxs-lookup"><span data-stu-id="4324f-116">PARAMETERS</span></span>

### <span data-ttu-id="4324f-117">-AdminDomainName</span><span class="sxs-lookup"><span data-stu-id="4324f-117">-AdminDomainName</span></span>
<span data-ttu-id="4324f-118">Windows IoT 裝置服務 OEM AAD 網域</span><span class="sxs-lookup"><span data-stu-id="4324f-118">Windows IoT Device Service OEM AAD domain</span></span>

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

### <span data-ttu-id="4324f-119">-BillingDomainName</span><span class="sxs-lookup"><span data-stu-id="4324f-119">-BillingDomainName</span></span>
<span data-ttu-id="4324f-120">Windows IoT 裝置服務 ODM AAD 網域</span><span class="sxs-lookup"><span data-stu-id="4324f-120">Windows IoT Device Service ODM AAD domain</span></span>

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

### <span data-ttu-id="4324f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4324f-121">-DefaultProfile</span></span>
<span data-ttu-id="4324f-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="4324f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4324f-123">-Etag</span><span class="sxs-lookup"><span data-stu-id="4324f-123">-Etag</span></span>
<span data-ttu-id="4324f-124">不需要 Etag *欄位。*</span><span class="sxs-lookup"><span data-stu-id="4324f-124">The Etag field is *not* required.</span></span>
<span data-ttu-id="4324f-125">如果這是在回應內內容中提供，也必須根據一般 ETag 慣例提供做為標頭。</span><span class="sxs-lookup"><span data-stu-id="4324f-125">If it is provided in the response body, it must also be provided as a header per the normal ETag convention.</span></span>

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

### <span data-ttu-id="4324f-126">-IfMatch</span><span class="sxs-lookup"><span data-stu-id="4324f-126">-IfMatch</span></span>
<span data-ttu-id="4324f-127">Windows IoT 裝置服務的 ETag。</span><span class="sxs-lookup"><span data-stu-id="4324f-127">ETag of the Windows IoT Device Service.</span></span>
<span data-ttu-id="4324f-128">請勿指定要建立全新 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="4324f-128">Do not specify for creating a brand new Windows IoT Device Service.</span></span>
<span data-ttu-id="4324f-129">需要更新現有的 Windows IoT 裝置服務。</span><span class="sxs-lookup"><span data-stu-id="4324f-129">Required to update an existing Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="4324f-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4324f-130">-InputObject</span></span>
<span data-ttu-id="4324f-131">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4324f-131">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4324f-132">-位置</span><span class="sxs-lookup"><span data-stu-id="4324f-132">-Location</span></span>
<span data-ttu-id="4324f-133">資源所在地的 Azure 區域</span><span class="sxs-lookup"><span data-stu-id="4324f-133">The Azure Region where the resource lives</span></span>

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

### <span data-ttu-id="4324f-134">-名稱</span><span class="sxs-lookup"><span data-stu-id="4324f-134">-Name</span></span>
<span data-ttu-id="4324f-135">Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="4324f-135">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="4324f-136">-注意</span><span class="sxs-lookup"><span data-stu-id="4324f-136">-Note</span></span>
<span data-ttu-id="4324f-137">Windows IoT 裝置服務附注。</span><span class="sxs-lookup"><span data-stu-id="4324f-137">Windows IoT Device Service notes.</span></span>

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

### <span data-ttu-id="4324f-138">-數量</span><span class="sxs-lookup"><span data-stu-id="4324f-138">-Quantity</span></span>
<span data-ttu-id="4324f-139">Windows IoT 裝置服務裝置配置，</span><span class="sxs-lookup"><span data-stu-id="4324f-139">Windows IoT Device Service device allocation,</span></span>

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

### <span data-ttu-id="4324f-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4324f-140">-ResourceGroupName</span></span>
<span data-ttu-id="4324f-141">包含 Windows IoT 裝置服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4324f-141">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="4324f-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4324f-142">-SubscriptionId</span></span>
<span data-ttu-id="4324f-143">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="4324f-143">The subscription identifier.</span></span>

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

### <span data-ttu-id="4324f-144">-標記</span><span class="sxs-lookup"><span data-stu-id="4324f-144">-Tag</span></span>
<span data-ttu-id="4324f-145">資源標記。</span><span class="sxs-lookup"><span data-stu-id="4324f-145">Resource tags.</span></span>

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

### <span data-ttu-id="4324f-146">-確認</span><span class="sxs-lookup"><span data-stu-id="4324f-146">-Confirm</span></span>
<span data-ttu-id="4324f-147">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="4324f-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4324f-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4324f-148">-WhatIf</span></span>
<span data-ttu-id="4324f-149">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4324f-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4324f-150">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4324f-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4324f-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4324f-151">CommonParameters</span></span>
<span data-ttu-id="4324f-152">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="4324f-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4324f-153">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4324f-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4324f-154">輸入</span><span class="sxs-lookup"><span data-stu-id="4324f-154">INPUTS</span></span>

### <span data-ttu-id="4324f-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="4324f-155">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="4324f-156">輸出</span><span class="sxs-lookup"><span data-stu-id="4324f-156">OUTPUTS</span></span>

### <span data-ttu-id="4324f-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="4324f-157">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="4324f-158">筆記</span><span class="sxs-lookup"><span data-stu-id="4324f-158">NOTES</span></span>

<span data-ttu-id="4324f-159">別名</span><span class="sxs-lookup"><span data-stu-id="4324f-159">ALIASES</span></span>

<span data-ttu-id="4324f-160">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="4324f-160">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4324f-161">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4324f-161">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4324f-162">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4324f-162">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4324f-163">INPUTOBJECT： <IWindowsIotServicesIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4324f-163">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4324f-164">`[DeviceName <String>]`：Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="4324f-164">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="4324f-165">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="4324f-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4324f-166">`[ResourceGroupName <String>]`：包含 Windows IoT 裝置服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="4324f-166">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="4324f-167">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="4324f-167">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="4324f-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="4324f-168">RELATED LINKS</span></span>

