---
external help file: ''
Module Name: Az.WindowsIotServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.windowsiotservices/get-azwindowsiotservicesdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/WindowsIotServices/help/Get-AzWindowsIotServicesDevice.md
ms.openlocfilehash: b9236dc7c3e4a12c9be6b72cd63874044ee49065
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98435934"
---
# <span data-ttu-id="36027-101">Get-AzWindowsIotServicesDevice</span><span class="sxs-lookup"><span data-stu-id="36027-101">Get-AzWindowsIotServicesDevice</span></span>

## <span data-ttu-id="36027-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36027-102">SYNOPSIS</span></span>
<span data-ttu-id="36027-103">取得 Windows IoT 裝置服務的非安全性相關中繼資料。</span><span class="sxs-lookup"><span data-stu-id="36027-103">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="36027-104">句法</span><span class="sxs-lookup"><span data-stu-id="36027-104">SYNTAX</span></span>

### <span data-ttu-id="36027-105">List1 (預設) </span><span class="sxs-lookup"><span data-stu-id="36027-105">List1 (Default)</span></span>
```
Get-AzWindowsIotServicesDevice [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36027-106">獲取</span><span class="sxs-lookup"><span data-stu-id="36027-106">Get</span></span>
```
Get-AzWindowsIotServicesDevice -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="36027-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="36027-107">GetViaIdentity</span></span>
```
Get-AzWindowsIotServicesDevice -InputObject <IWindowsIotServicesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="36027-108">清單</span><span class="sxs-lookup"><span data-stu-id="36027-108">List</span></span>
```
Get-AzWindowsIotServicesDevice -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="36027-109">說明</span><span class="sxs-lookup"><span data-stu-id="36027-109">DESCRIPTION</span></span>
<span data-ttu-id="36027-110">取得 Windows IoT 裝置服務的非安全性相關中繼資料。</span><span class="sxs-lookup"><span data-stu-id="36027-110">Get the non-security related metadata of a Windows IoT Device Service.</span></span>

## <span data-ttu-id="36027-111">示例</span><span class="sxs-lookup"><span data-stu-id="36027-111">EXAMPLES</span></span>

### <span data-ttu-id="36027-112">範例1：取得訂閱下的所有 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="36027-112">Example 1: Get all Windows IoT services under a subscription</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="36027-113">這個命令會取得訂閱下的所有 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="36027-113">This command gets all Windows IoT services under a subscription.</span></span>

### <span data-ttu-id="36027-114">範例2：取得資源群組底下的所有 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="36027-114">Example 2: Get all Windows IoT services under a resource group</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
eastus   wsi-t02 Microsoft.WindowsIoT/DeviceServices "5c006ad2-0000-0700-0000-5faa3e090000"
```

<span data-ttu-id="36027-115">這個命令會取得資源群組底下的所有 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="36027-115">This command gets all Windows IoT services under a resource group.</span></span>

### <span data-ttu-id="36027-116">範例3：依名稱取得 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="36027-116">Example 3: Get a Windows IoT service by name</span></span>
```powershell
PS C:\> Get-AzWindowsIotServicesDevice -ResourceGroupName azure-rg-test -Name wsi-t01

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="36027-117">這個命令會透過名稱取得 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="36027-117">This command gets a Windows IoT service by name.</span></span>

### <span data-ttu-id="36027-118">範例4：透過物件取得 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="36027-118">Example 4: Get a Windows IoT service by object</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com'
PS C:\> Get-AzWindowsIotServicesDevice -InputObject $wsi

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="36027-119">這個命令會透過物件取得 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="36027-119">This command gets a Windows IoT service by object.</span></span>

### <span data-ttu-id="36027-120">範例4：透過管道取得 Windows IoT 服務</span><span class="sxs-lookup"><span data-stu-id="36027-120">Example 4: Get a Windows IoT service by pipeline</span></span>
```powershell
PS C:\> $wsi = New-AzWindowsIotServicesDevice -Name wsi-t01 -ResourceGroupName azure-rg-test -Location eastus -Quantity 10 -BillingDomainName 'microsoft.onmicrosoft.com' -AdminDomainName 'microsoft.onmicrosoft.com' | Get-AzWindowsIotServicesDevice

Location Name    Type                                Etag
-------- ----    ----                                ----
West US  wsi-t01 Microsoft.WindowsIoT/DeviceServices "5c006e63-0000-0700-0000-5faa37830000"
```

<span data-ttu-id="36027-121">這個命令會透過管線取得 Windows IoT 服務。</span><span class="sxs-lookup"><span data-stu-id="36027-121">This command gets a Windows IoT service by pipeline.</span></span>

## <span data-ttu-id="36027-122">參數</span><span class="sxs-lookup"><span data-stu-id="36027-122">PARAMETERS</span></span>

### <span data-ttu-id="36027-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36027-123">-DefaultProfile</span></span>
<span data-ttu-id="36027-124">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="36027-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36027-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36027-125">-InputObject</span></span>
<span data-ttu-id="36027-126">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="36027-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="36027-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="36027-127">-Name</span></span>
<span data-ttu-id="36027-128">Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="36027-128">The name of the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="36027-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36027-129">-ResourceGroupName</span></span>
<span data-ttu-id="36027-130">包含 Windows IoT 裝置服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36027-130">The name of the resource group that contains the Windows IoT Device Service.</span></span>

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

### <span data-ttu-id="36027-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="36027-131">-SubscriptionId</span></span>
<span data-ttu-id="36027-132">訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="36027-132">The subscription identifier.</span></span>

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

### <span data-ttu-id="36027-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36027-133">CommonParameters</span></span>
<span data-ttu-id="36027-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36027-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36027-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="36027-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36027-136">輸入</span><span class="sxs-lookup"><span data-stu-id="36027-136">INPUTS</span></span>

### <span data-ttu-id="36027-137">IWindowsIotServicesIdentity （WindowsIotServices）的</span><span class="sxs-lookup"><span data-stu-id="36027-137">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.IWindowsIotServicesIdentity</span></span>

## <span data-ttu-id="36027-138">輸出</span><span class="sxs-lookup"><span data-stu-id="36027-138">OUTPUTS</span></span>

### <span data-ttu-id="36027-139">IDeviceService （WindowsIotServices）。 Api20190601。</span><span class="sxs-lookup"><span data-stu-id="36027-139">Microsoft.Azure.PowerShell.Cmdlets.WindowsIotServices.Models.Api20190601.IDeviceService</span></span>

## <span data-ttu-id="36027-140">筆記</span><span class="sxs-lookup"><span data-stu-id="36027-140">NOTES</span></span>

<span data-ttu-id="36027-141">別名</span><span class="sxs-lookup"><span data-stu-id="36027-141">ALIASES</span></span>

<span data-ttu-id="36027-142">複雜的參數屬性</span><span class="sxs-lookup"><span data-stu-id="36027-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="36027-143">若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="36027-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="36027-144">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="36027-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="36027-145">INPUTOBJECT <IWindowsIotServicesIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="36027-145">INPUTOBJECT <IWindowsIotServicesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="36027-146">`[DeviceName <String>]`： Windows IoT 裝置服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="36027-146">`[DeviceName <String>]`: The name of the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="36027-147">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="36027-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="36027-148">`[ResourceGroupName <String>]`：包含 Windows IoT 裝置服務之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="36027-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the Windows IoT Device Service.</span></span>
  - <span data-ttu-id="36027-149">`[SubscriptionId <String>]`：訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="36027-149">`[SubscriptionId <String>]`: The subscription identifier.</span></span>

## <span data-ttu-id="36027-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="36027-150">RELATED LINKS</span></span>

