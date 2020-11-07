---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsvmextension
schema: 2.0.0
ms.openlocfilehash: c2214f01b35e68ba22f9dbfc6fe9e602badb9ba9
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2020
ms.locfileid: "93966818"
---
# <span data-ttu-id="cf471-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="cf471-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="cf471-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf471-102">SYNOPSIS</span></span>
<span data-ttu-id="cf471-103">傳回符合發行者、類型、版本的要求虛擬機器延伸影像。</span><span class="sxs-lookup"><span data-stu-id="cf471-103">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="cf471-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf471-104">SYNTAX</span></span>

### <span data-ttu-id="cf471-105"> (預設) 清單</span><span class="sxs-lookup"><span data-stu-id="cf471-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="cf471-106">獲取</span><span class="sxs-lookup"><span data-stu-id="cf471-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cf471-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cf471-107">GetViaIdentity</span></span>
```
Get-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cf471-108">說明</span><span class="sxs-lookup"><span data-stu-id="cf471-108">DESCRIPTION</span></span>
<span data-ttu-id="cf471-109">傳回符合發行者、類型、版本的要求虛擬機器延伸影像。</span><span class="sxs-lookup"><span data-stu-id="cf471-109">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="cf471-110">示例</span><span class="sxs-lookup"><span data-stu-id="cf471-110">EXAMPLES</span></span>

### <span data-ttu-id="cf471-111">範例1：取得所有 VM 延伸</span><span class="sxs-lookup"><span data-stu-id="cf471-111">Example 1:  Get All VM Extensions</span></span>
```powershell
PS C:\> Get-AzsVMExtension

ExtensionType            : IaaSDiagnostics
TypeHandlerVersion       : 1.11.3.12
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/northwest/artifactTypes/VMExtension/publishers/Microsoft.Azure.Diagnostics/types/IaaSDia
                           gnostics/versions/1.11.3.12
IsSystemExtension        : False
Location                 : northwest
Name                     :
ProvisioningState        : Succeeded
Publisher                : Microsoft.Azure.Diagnostics
SourceBlobUri            :
SupportMultipleExtension : False
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Windows

...
```

<span data-ttu-id="cf471-112">只要將所有參數留白，即可取得所有 VMExtensions 的清單。</span><span class="sxs-lookup"><span data-stu-id="cf471-112">Get a list of all VMExtensions by leaving all parameters blank.</span></span>

## <span data-ttu-id="cf471-113">參數</span><span class="sxs-lookup"><span data-stu-id="cf471-113">PARAMETERS</span></span>

### <span data-ttu-id="cf471-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf471-114">-DefaultProfile</span></span>
<span data-ttu-id="cf471-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="cf471-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf471-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cf471-116">-InputObject</span></span>
<span data-ttu-id="cf471-117">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="cf471-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cf471-118">-位置</span><span class="sxs-lookup"><span data-stu-id="cf471-118">-Location</span></span>
<span data-ttu-id="cf471-119">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="cf471-119">Location of the resource.</span></span>

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

### <span data-ttu-id="cf471-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="cf471-120">-Publisher</span></span>
<span data-ttu-id="cf471-121">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf471-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="cf471-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cf471-122">-SubscriptionId</span></span>
<span data-ttu-id="cf471-123">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cf471-123">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cf471-124">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cf471-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cf471-125">-類型</span><span class="sxs-lookup"><span data-stu-id="cf471-125">-Type</span></span>
<span data-ttu-id="cf471-126">延伸類型。</span><span class="sxs-lookup"><span data-stu-id="cf471-126">Type of extension.</span></span>

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

### <span data-ttu-id="cf471-127">-版本</span><span class="sxs-lookup"><span data-stu-id="cf471-127">-Version</span></span>
<span data-ttu-id="cf471-128">資源的版本。</span><span class="sxs-lookup"><span data-stu-id="cf471-128">The version of the resource.</span></span>

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

### <span data-ttu-id="cf471-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf471-129">CommonParameters</span></span>
<span data-ttu-id="cf471-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf471-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf471-131">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cf471-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf471-132">輸入</span><span class="sxs-lookup"><span data-stu-id="cf471-132">INPUTS</span></span>

### <span data-ttu-id="cf471-133">IComputeAdminIdentity （ComputeAdmin）的</span><span class="sxs-lookup"><span data-stu-id="cf471-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="cf471-134">輸出</span><span class="sxs-lookup"><span data-stu-id="cf471-134">OUTPUTS</span></span>

### <span data-ttu-id="cf471-135">IVMExtension （ComputeAdmin）。 Api20151201Preview。</span><span class="sxs-lookup"><span data-stu-id="cf471-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="cf471-136">筆記</span><span class="sxs-lookup"><span data-stu-id="cf471-136">NOTES</span></span>

<span data-ttu-id="cf471-137">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="cf471-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cf471-138">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="cf471-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cf471-139">INPUTOBJECT <IComputeAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="cf471-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cf471-140">`[DiskId <String>]`：磁片 guid 作為身分識別。</span><span class="sxs-lookup"><span data-stu-id="cf471-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="cf471-141">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="cf471-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cf471-142">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="cf471-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cf471-143">`[MigrationId <String>]`：遷移作業 guid 名稱。</span><span class="sxs-lookup"><span data-stu-id="cf471-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="cf471-144">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf471-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="cf471-145">`[Publisher <String>]`：發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf471-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="cf471-146">`[QuotaName <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf471-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="cf471-147">`[Sku <String>]`： SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf471-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="cf471-148">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="cf471-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cf471-149">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="cf471-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cf471-150">`[Type <String>]`：延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="cf471-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="cf471-151">`[Version <String>]`：資源的版本。</span><span class="sxs-lookup"><span data-stu-id="cf471-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="cf471-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf471-152">RELATED LINKS</span></span>

