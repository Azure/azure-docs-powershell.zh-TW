---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/powershell/module/az.windowsiotservices/get-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
ms.openlocfilehash: 51e828245c62ddfcbaa925b3a22a916fd9148ada
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916792"
---
# <span data-ttu-id="2a173-101">Get-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="2a173-101">Get-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="2a173-102">簡介</span><span class="sxs-lookup"><span data-stu-id="2a173-102">SYNOPSIS</span></span>
<span data-ttu-id="2a173-103">取得 Windows IoT 裝置服務的非安全性相關中繼資料。</span><span class="sxs-lookup"><span data-stu-id="2a173-103">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="2a173-104">語法</span><span class="sxs-lookup"><span data-stu-id="2a173-104">SYNTAX</span></span>

### <span data-ttu-id="2a173-105">清單1 (預設) </span><span class="sxs-lookup"><span data-stu-id="2a173-105">List1 (Default)</span></span>
```
Get-AzWindowsIotServicesDevice [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2a173-106">獲取</span><span class="sxs-lookup"><span data-stu-id="2a173-106">Get</span></span>
```
Get-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2a173-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2a173-107">GetViaIdentity</span></span>
```
Get-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a173-108">清單</span><span class="sxs-lookup"><span data-stu-id="2a173-108">List</span></span>
```
Get-AzWindowsIotServicesDevice -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2a173-109">描述</span><span class="sxs-lookup"><span data-stu-id="2a173-109">DESCRIPTION</span></span>
<span data-ttu-id="2a173-110">取得 Windows IoT 裝置服務的非安全性相關中繼資料。</span><span class="sxs-lookup"><span data-stu-id="2a173-110">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="2a173-111">例子</span><span class="sxs-lookup"><span data-stu-id="2a173-111">EXAMPLES</span></span>

### <span data-ttu-id="2a173-112">範例 1：取得訂閱下的所有 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="2a173-112">Example 1: Get all Windows IoT services under a subscription</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="2a173-113">此命令會獲得訂閱下的所有 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="2a173-113">This command gets all Windows IoT services under a subscription.</span></span>

### <span data-ttu-id="2a173-114">範例 2：在資源群組下取得所有 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="2a173-114">Example 2: Get all Windows IoT services under a resource group</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="2a173-115">此命令會獲得資源群組下的所有 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="2a173-115">This command gets all Windows IoT services under a resource group.</span></span>

### <span data-ttu-id="2a173-116">範例 3：按名稱取得 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="2a173-116">Example 3: Get a Windows IoT service by name</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="2a173-117">此命令會按名稱獲得 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="2a173-117">This command gets a Windows IoT service by name.</span></span>

### <span data-ttu-id="2a173-118">範例 4：根據物件取得 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="2a173-118">Example 4: Get a Windows IoT service by object</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'
PS C:\> Get-AzWindowsIotServicesDevice -InputObject $wsi

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="2a173-119">此命令會按物件獲得 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="2a173-119">This command gets a Windows IoT service by object.</span></span>

### <span data-ttu-id="2a173-120">範例 4：根據管線取得 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="2a173-120">Example 4: Get a Windows IoT service by pipeline</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com' | Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="2a173-121">此命令會按管線獲得 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="2a173-121">This command gets a Windows IoT service by pipeline.</span></span>

## <span data-ttu-id="2a173-122">參數</span><span class="sxs-lookup"><span data-stu-id="2a173-122">PARAMETERS</span></span>

### <span data-ttu-id="2a173-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a173-123">-DefaultProfile</span></span>
<span data-ttu-id="2a173-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="2a173-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a173-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a173-125">-InputObject</span></span>
<span data-ttu-id="2a173-126">身分識別參數若要建構，請參閱 INPUTOBJECT 屬性的 NOTES 區段，並建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2a173-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a173-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="2a173-127">-Name</span></span>
<span data-ttu-id="2a173-128">Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a173-128">The name of the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a173-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a173-129">-ResourceGroupName</span></span>
<span data-ttu-id="2a173-130">包含 Windows IoT 裝置服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="2a173-130">The name of the resource group that contains the Windows IoT Device Service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a173-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a173-131">-SubscriptionId</span></span>
<span data-ttu-id="2a173-132">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a173-132">The subscription identifier.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a173-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a173-133">CommonParameters</span></span>
<span data-ttu-id="2a173-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="2a173-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a173-135">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a173-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a173-136">輸入</span><span class="sxs-lookup"><span data-stu-id="2a173-136">INPUTS</span></span>

### <span data-ttu-id="2a173-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.models.IWindowsIotServicesIdentity</span><span class="sxs-lookup"><span data-stu-id="2a173-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="2a173-138">輸出</span><span class="sxs-lookup"><span data-stu-id="2a173-138">OUTPUTS</span></span>

### <span data-ttu-id="2a173-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.models.Api20190601.IDeviceService</span><span class="sxs-lookup"><span data-stu-id="2a173-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="2a173-140">筆記</span><span class="sxs-lookup"><span data-stu-id="2a173-140">NOTES</span></span>

<span data-ttu-id="2a173-141">別名</span><span class="sxs-lookup"><span data-stu-id="2a173-141">ALIASES</span></span>

<span data-ttu-id="2a173-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="2a173-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2a173-143">若要建立下列描述的參數，請建構包含適當屬性的雜湊表。</span><span class="sxs-lookup"><span data-stu-id="2a173-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a173-144">有關雜湊表的資訊，請執行Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="2a173-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2a173-145">INPUTOBJECT： <IWindowsIotServicesIdentity> 身分識別參數</span><span class="sxs-lookup"><span data-stu-id="2a173-145">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2a173-146">`[DeviceName <String>]`：Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="2a173-146">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="2a173-147">`[Id <String>]`：資源識別路徑</span><span class="sxs-lookup"><span data-stu-id="2a173-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2a173-148">`[ResourceGroupName <String>]`：包含 Windows IoT 裝置服務的資源組名。</span><span class="sxs-lookup"><span data-stu-id="2a173-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="2a173-149">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="2a173-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="2a173-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="2a173-150">RELATED LINKS</span></span>

