---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: d91e930c486fea5c7a17e5a8f7d8f8d30a88b351
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968190"
---
# <span data-ttu-id="e7904-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="e7904-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="e7904-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e7904-102">SYNOPSIS</span></span>
<span data-ttu-id="e7904-103">傳回符合發行者、優惠、sku 與版本的特定平臺影像。</span><span class="sxs-lookup"><span data-stu-id="e7904-103">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="e7904-104">句法</span><span class="sxs-lookup"><span data-stu-id="e7904-104">SYNTAX</span></span>

### <span data-ttu-id="e7904-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="e7904-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="e7904-106">獲取</span><span class="sxs-lookup"><span data-stu-id="e7904-106">Get</span></span>
```
Get-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e7904-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e7904-107">GetViaIdentity</span></span>
```
Get-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e7904-108">說明</span><span class="sxs-lookup"><span data-stu-id="e7904-108">DESCRIPTION</span></span>
<span data-ttu-id="e7904-109">傳回符合發行者、優惠、sku 與版本的特定平臺影像。</span><span class="sxs-lookup"><span data-stu-id="e7904-109">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="e7904-110">示例</span><span class="sxs-lookup"><span data-stu-id="e7904-110">EXAMPLES</span></span>

### <span data-ttu-id="e7904-111">範例1：取得所有平臺影像</span><span class="sxs-lookup"><span data-stu-id="e7904-111">Example 1: Get All Platform Images</span></span>
```powershell
PS C:\> Get-AzsPlatformImage

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/loc
                    al/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=r
                    wdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="e7904-112">只要將所有的參數留白，即可取得所有平臺影像的清單。</span><span class="sxs-lookup"><span data-stu-id="e7904-112">Get a list of all Platform Images by leaving all parameters blank.</span></span>

### <span data-ttu-id="e7904-113">範例2：取得特定的平臺影像</span><span class="sxs-lookup"><span data-stu-id="e7904-113">Example 2: Get Specific Platform Image</span></span>
```powershell
PS C:\> Get-AzsPlatformImage -Offer ExampleOffer -Publisher ExamplePublisher -Location local -Sku ExampleSku -Version 1.0.0

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifa
                    ctTypes/platformImage/publishers/ExamplePublisher/offers/ExampleOffer/skus/ExampleSku/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&s
                    e=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="e7904-114">指定優惠、發行者、位置、Sku 及版本，以取得平臺影像。</span><span class="sxs-lookup"><span data-stu-id="e7904-114">Specify the Offer, Publisher, Location, Sku, and Version to retrieve a Platform Image.</span></span>

## <span data-ttu-id="e7904-115">參數</span><span class="sxs-lookup"><span data-stu-id="e7904-115">PARAMETERS</span></span>

### <span data-ttu-id="e7904-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7904-116">-DefaultProfile</span></span>
<span data-ttu-id="e7904-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="e7904-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7904-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7904-118">-InputObject</span></span>
<span data-ttu-id="e7904-119">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="e7904-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e7904-120">-位置</span><span class="sxs-lookup"><span data-stu-id="e7904-120">-Location</span></span>
<span data-ttu-id="e7904-121">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="e7904-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7904-122">-優惠</span><span class="sxs-lookup"><span data-stu-id="e7904-122">-Offer</span></span>
<span data-ttu-id="e7904-123">優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7904-123">Name of the offer.</span></span>

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

### <span data-ttu-id="e7904-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="e7904-124">-Publisher</span></span>
<span data-ttu-id="e7904-125">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7904-125">Name of the publisher.</span></span>

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

### <span data-ttu-id="e7904-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="e7904-126">-Sku</span></span>
<span data-ttu-id="e7904-127">SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7904-127">Name of the SKU.</span></span>

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

### <span data-ttu-id="e7904-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7904-128">-SubscriptionId</span></span>
<span data-ttu-id="e7904-129">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e7904-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e7904-130">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e7904-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7904-131">-版本</span><span class="sxs-lookup"><span data-stu-id="e7904-131">-Version</span></span>
<span data-ttu-id="e7904-132">資源的版本。</span><span class="sxs-lookup"><span data-stu-id="e7904-132">The version of the resource.</span></span>

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

### <span data-ttu-id="e7904-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7904-133">CommonParameters</span></span>
<span data-ttu-id="e7904-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e7904-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7904-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="e7904-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7904-136">輸入</span><span class="sxs-lookup"><span data-stu-id="e7904-136">INPUTS</span></span>

### <span data-ttu-id="e7904-137">IComputeAdminIdentity （ComputeAdmin）的</span><span class="sxs-lookup"><span data-stu-id="e7904-137">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="e7904-138">輸出</span><span class="sxs-lookup"><span data-stu-id="e7904-138">OUTPUTS</span></span>

### <span data-ttu-id="e7904-139">IPlatformImage （ComputeAdmin）。 Api20151201Preview。</span><span class="sxs-lookup"><span data-stu-id="e7904-139">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="e7904-140">筆記</span><span class="sxs-lookup"><span data-stu-id="e7904-140">NOTES</span></span>

<span data-ttu-id="e7904-141">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="e7904-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e7904-142">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="e7904-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e7904-143">INPUTOBJECT <IComputeAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="e7904-143">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e7904-144">`[DiskId <String>]`：磁片 guid 作為身分識別。</span><span class="sxs-lookup"><span data-stu-id="e7904-144">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="e7904-145">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="e7904-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e7904-146">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="e7904-146">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e7904-147">`[MigrationId <String>]`：遷移作業 guid 名稱。</span><span class="sxs-lookup"><span data-stu-id="e7904-147">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="e7904-148">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7904-148">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="e7904-149">`[Publisher <String>]`：發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7904-149">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="e7904-150">`[QuotaName <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7904-150">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e7904-151">`[Sku <String>]`： SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="e7904-151">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="e7904-152">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="e7904-152">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e7904-153">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="e7904-153">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e7904-154">`[Type <String>]`：延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="e7904-154">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="e7904-155">`[Version <String>]`：資源的版本。</span><span class="sxs-lookup"><span data-stu-id="e7904-155">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="e7904-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7904-156">RELATED LINKS</span></span>

