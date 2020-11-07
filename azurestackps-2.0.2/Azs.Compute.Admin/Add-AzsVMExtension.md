---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsvmextension
schema: 2.0.0
ms.openlocfilehash: a9c5a207d478fe40181150206990cb47ad4e45d5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/08/2020
ms.locfileid: "93968375"
---
# <span data-ttu-id="4e179-101">Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="4e179-101">Add-AzsVMExtension</span></span>

## <span data-ttu-id="4e179-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e179-102">SYNOPSIS</span></span>
<span data-ttu-id="4e179-103">使用 publisher、版本建立虛擬電腦延伸影像。</span><span class="sxs-lookup"><span data-stu-id="4e179-103">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="4e179-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e179-104">SYNTAX</span></span>

### <span data-ttu-id="4e179-105">CreateExpanded (預設) </span><span class="sxs-lookup"><span data-stu-id="4e179-105">CreateExpanded (Default)</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-ComputeRole <String>] [-IsSystemExtension] [-PropertiesPublisher <String>]
 [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>] [-SupportMultipleExtensions]
 [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4e179-106">建立</span><span class="sxs-lookup"><span data-stu-id="4e179-106">Create</span></span>
```
Add-AzsVMExtension -Publisher <String> -Type <String> -Version <String> -Extension <IVMExtensionParameters>
 [-Location <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4e179-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4e179-107">CreateViaIdentity</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> -Extension <IVMExtensionParameters>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4e179-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4e179-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsVMExtension -InputObject <IComputeAdminIdentity> [-Publisher <String>] [-ComputeRole <String>]
 [-IsSystemExtension] [-ProvisioningState <ProvisioningState>] [-SourceBlob <String>]
 [-SupportMultipleExtensions] [-VmOsType <OSType>] [-VMScaleSetEnabled] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e179-109">說明</span><span class="sxs-lookup"><span data-stu-id="4e179-109">DESCRIPTION</span></span>
<span data-ttu-id="4e179-110">使用 publisher、版本建立虛擬電腦延伸影像。</span><span class="sxs-lookup"><span data-stu-id="4e179-110">Create a Virtual Machine Extension Image with publisher, version.</span></span>

## <span data-ttu-id="4e179-111">示例</span><span class="sxs-lookup"><span data-stu-id="4e179-111">EXAMPLES</span></span>

### <span data-ttu-id="4e179-112">範例1： Add-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="4e179-112">Example 1: Add-AzsVMExtension</span></span>
```powershell
PS C:\> Add-AzsVMExtension -Location "local" -Publisher "Microsoft" -Type "MicroExtension" -Version "0.1.0" -ComputeRole "IaaS" -SourceBlob "https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip" -SupportMultipleExtensions -VmOsType "Linux"

ExtensionType            : MicroExtension
TypeHandlerVersion       : 0.1.0
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/local/artifactTypes/VMExtension/publishers/Microsoft/types/MicroExtension/versions/0.1.0
IsSystemExtension        : False
Location                 : local
Name                     :
ProvisioningState        : Creating
Publisher                : Microsoft
SourceBlobUri            : https://github.com/Microsoft/PowerShell-DSC-for-Linux/archive/v1.1.1-294.zip
SupportMultipleExtension : True
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Linux
```

<span data-ttu-id="4e179-113">使用可公開存取的連結，以提供延伸的位置，或使用 SasUri 將 URI 提供給 Azure Blob。</span><span class="sxs-lookup"><span data-stu-id="4e179-113">Use a publicly accessible link to provide the location of the extension, or the URI to an Azure Blob using the SasUri.</span></span>

## <span data-ttu-id="4e179-114">參數</span><span class="sxs-lookup"><span data-stu-id="4e179-114">PARAMETERS</span></span>

### <span data-ttu-id="4e179-115">-ComputeRole</span><span class="sxs-lookup"><span data-stu-id="4e179-115">-ComputeRole</span></span>
<span data-ttu-id="4e179-116">計算角色</span><span class="sxs-lookup"><span data-stu-id="4e179-116">Compute role</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e179-117">-DefaultProfile</span></span>
<span data-ttu-id="4e179-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="4e179-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e179-119">-延伸</span><span class="sxs-lookup"><span data-stu-id="4e179-119">-Extension</span></span>
<span data-ttu-id="4e179-120">用來建立新的虛擬機器延伸影像的參數。</span><span class="sxs-lookup"><span data-stu-id="4e179-120">Parameters used to create a new Virtual Machine Extension Image.</span></span>
<span data-ttu-id="4e179-121">若要建立，請參閱副檔名屬性和建立雜湊資料表的備忘稿區段。</span><span class="sxs-lookup"><span data-stu-id="4e179-121">To construct, see NOTES section for EXTENSION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e179-122">-InputObject</span></span>
<span data-ttu-id="4e179-123">要構造的身分識別參數，請參閱 INPUTOBJECT 屬性的 [記事] 區段，然後建立雜湊表。</span><span class="sxs-lookup"><span data-stu-id="4e179-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-124">-IsSystemExtension</span><span class="sxs-lookup"><span data-stu-id="4e179-124">-IsSystemExtension</span></span>
<span data-ttu-id="4e179-125">表示系統是否有延伸。</span><span class="sxs-lookup"><span data-stu-id="4e179-125">Indicates if the extension is for the system.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-126">-位置</span><span class="sxs-lookup"><span data-stu-id="4e179-126">-Location</span></span>
<span data-ttu-id="4e179-127">資源的位置。</span><span class="sxs-lookup"><span data-stu-id="4e179-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-128">-PropertiesPublisher</span><span class="sxs-lookup"><span data-stu-id="4e179-128">-PropertiesPublisher</span></span>
<span data-ttu-id="4e179-129">VM 延伸的發行者</span><span class="sxs-lookup"><span data-stu-id="4e179-129">The publisher of the VM Extension</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-130">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="4e179-130">-ProvisioningState</span></span>
<span data-ttu-id="4e179-131">已提供延伸的狀態。</span><span class="sxs-lookup"><span data-stu-id="4e179-131">Provisioning state of extension.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="4e179-132">-Publisher</span></span>
<span data-ttu-id="4e179-133">發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e179-133">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-134">-SourceBlob</span><span class="sxs-lookup"><span data-stu-id="4e179-134">-SourceBlob</span></span>
<span data-ttu-id="4e179-135">Azure 或 AzureStack blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="4e179-135">URI to Azure or AzureStack blob.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e179-136">-SubscriptionId</span></span>
<span data-ttu-id="4e179-137">可唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4e179-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4e179-138">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="4e179-138">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-139">-SupportMultipleExtensions</span><span class="sxs-lookup"><span data-stu-id="4e179-139">-SupportMultipleExtensions</span></span>
<span data-ttu-id="4e179-140">如果支援多個延伸，則為 True。</span><span class="sxs-lookup"><span data-stu-id="4e179-140">True if supports multiple extensions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-141">-類型</span><span class="sxs-lookup"><span data-stu-id="4e179-141">-Type</span></span>
<span data-ttu-id="4e179-142">延伸類型。</span><span class="sxs-lookup"><span data-stu-id="4e179-142">Type of extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-143">-版本</span><span class="sxs-lookup"><span data-stu-id="4e179-143">-Version</span></span>
<span data-ttu-id="4e179-144">資源的版本。</span><span class="sxs-lookup"><span data-stu-id="4e179-144">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-145">-VmOsType</span><span class="sxs-lookup"><span data-stu-id="4e179-145">-VmOsType</span></span>
<span data-ttu-id="4e179-146">部署擴充處理常式所需的目標虛擬機器作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="4e179-146">Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-147">-VMScaleSetEnabled</span><span class="sxs-lookup"><span data-stu-id="4e179-147">-VMScaleSetEnabled</span></span>
<span data-ttu-id="4e179-148">指示是否已針對虛擬電腦縮放設定支援啟用延伸的值。</span><span class="sxs-lookup"><span data-stu-id="4e179-148">Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4e179-149">-確認</span><span class="sxs-lookup"><span data-stu-id="4e179-149">-Confirm</span></span>
<span data-ttu-id="4e179-150">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4e179-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e179-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e179-151">-WhatIf</span></span>
<span data-ttu-id="4e179-152">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4e179-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e179-153">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4e179-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e179-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e179-154">CommonParameters</span></span>
<span data-ttu-id="4e179-155">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e179-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e179-156">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e179-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e179-157">輸入</span><span class="sxs-lookup"><span data-stu-id="4e179-157">INPUTS</span></span>

### <span data-ttu-id="4e179-158">IVMExtensionParameters （ComputeAdmin）。 Api20151201Preview。</span><span class="sxs-lookup"><span data-stu-id="4e179-158">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtensionParameters</span></span>

### <span data-ttu-id="4e179-159">IComputeAdminIdentity （ComputeAdmin）的</span><span class="sxs-lookup"><span data-stu-id="4e179-159">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="4e179-160">輸出</span><span class="sxs-lookup"><span data-stu-id="4e179-160">OUTPUTS</span></span>

### <span data-ttu-id="4e179-161">IVMExtension （ComputeAdmin）。 Api20151201Preview。</span><span class="sxs-lookup"><span data-stu-id="4e179-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="4e179-162">筆記</span><span class="sxs-lookup"><span data-stu-id="4e179-162">NOTES</span></span>

<span data-ttu-id="4e179-163">複雜參數屬性若要建立如下所述的參數，請構造包含適當屬性的雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="4e179-163">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e179-164">如需雜湊資料表的詳細資訊，請執行 Get-Help about_Hash_Tables。</span><span class="sxs-lookup"><span data-stu-id="4e179-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4e179-165">[延伸] <IVMExtensionParameters> ：用來建立新的虛擬機器延伸影像的參數。</span><span class="sxs-lookup"><span data-stu-id="4e179-165">EXTENSION <IVMExtensionParameters>: Parameters used to create a new Virtual Machine Extension Image.</span></span>
  - <span data-ttu-id="4e179-166">`[ComputeRole <String>]`：計算角色</span><span class="sxs-lookup"><span data-stu-id="4e179-166">`[ComputeRole <String>]`: Compute role</span></span>
  - <span data-ttu-id="4e179-167">`[IsSystemExtension <Boolean?>]`：表示系統是否有延伸。</span><span class="sxs-lookup"><span data-stu-id="4e179-167">`[IsSystemExtension <Boolean?>]`: Indicates if the extension is for the system.</span></span>
  - <span data-ttu-id="4e179-168">`[ProvisioningState <ProvisioningState?>]`：正在預配延伸的狀態。</span><span class="sxs-lookup"><span data-stu-id="4e179-168">`[ProvisioningState <ProvisioningState?>]`: Provisioning state of extension.</span></span>
  - <span data-ttu-id="4e179-169">`[Publisher <String>]`： VM 延伸的發行者</span><span class="sxs-lookup"><span data-stu-id="4e179-169">`[Publisher <String>]`: The publisher of the VM Extension</span></span>
  - <span data-ttu-id="4e179-170">`[SourceBlobUri <String>]`： Azure 或 AzureStack blob 的 URI。</span><span class="sxs-lookup"><span data-stu-id="4e179-170">`[SourceBlobUri <String>]`: URI to Azure or AzureStack blob.</span></span>
  - <span data-ttu-id="4e179-171">`[SupportMultipleExtension <Boolean?>]`：如果支援多個延伸，則為 True。</span><span class="sxs-lookup"><span data-stu-id="4e179-171">`[SupportMultipleExtension <Boolean?>]`: True if supports multiple extensions.</span></span>
  - <span data-ttu-id="4e179-172">`[VMScaleSetEnabled <Boolean?>]`：值，指出是否已針對虛擬電腦縮放設定支援啟用延伸。</span><span class="sxs-lookup"><span data-stu-id="4e179-172">`[VMScaleSetEnabled <Boolean?>]`: Value indicating whether the extension is enabled for virtual machine scale set support.</span></span>
  - <span data-ttu-id="4e179-173">`[VmosType <OSType?>]`：部署擴充處理常式所需的目標虛擬機器作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="4e179-173">`[VmosType <OSType?>]`: Target virtual machine operating system type necessary for deploying the extension handler.</span></span>

<span data-ttu-id="4e179-174">INPUTOBJECT <IComputeAdminIdentity> ：身分識別參數</span><span class="sxs-lookup"><span data-stu-id="4e179-174">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e179-175">`[DiskId <String>]`：磁片 guid 作為身分識別。</span><span class="sxs-lookup"><span data-stu-id="4e179-175">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="4e179-176">`[Id <String>]`：資源身分識別路徑</span><span class="sxs-lookup"><span data-stu-id="4e179-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e179-177">`[Location <String>]`：資源的位置。</span><span class="sxs-lookup"><span data-stu-id="4e179-177">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4e179-178">`[MigrationId <String>]`：遷移作業 guid 名稱。</span><span class="sxs-lookup"><span data-stu-id="4e179-178">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="4e179-179">`[Offer <String>]`：優惠的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e179-179">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="4e179-180">`[Publisher <String>]`：發行者的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e179-180">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="4e179-181">`[QuotaName <String>]`：配額的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e179-181">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="4e179-182">`[Sku <String>]`： SKU 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e179-182">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="4e179-183">`[SubscriptionId <String>]`：唯一識別 Microsoft Azure 訂閱的訂閱認證。</span><span class="sxs-lookup"><span data-stu-id="4e179-183">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4e179-184">[訂閱識別碼] 會在每個服務呼叫的 URI 中形成一部分。</span><span class="sxs-lookup"><span data-stu-id="4e179-184">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4e179-185">`[Type <String>]`：延伸的類型。</span><span class="sxs-lookup"><span data-stu-id="4e179-185">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="4e179-186">`[Version <String>]`：資源的版本。</span><span class="sxs-lookup"><span data-stu-id="4e179-186">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="4e179-187">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e179-187">RELATED LINKS</span></span>

