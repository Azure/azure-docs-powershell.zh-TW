---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1999C880-F8F9-4CED-91A9-33E9BBDFE27D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09a3d7be7bf71e73443dcbb31464ee6f7f19b43a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967646"
---
# <span data-ttu-id="b467f-101">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="b467f-101">New-AzureVM</span></span>

## <span data-ttu-id="b467f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b467f-102">SYNOPSIS</span></span>
<span data-ttu-id="b467f-103">建立 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b467f-103">Creates an Azure virtual machine.</span></span>

## <span data-ttu-id="b467f-104">句法</span><span class="sxs-lookup"><span data-stu-id="b467f-104">SYNTAX</span></span>

### <span data-ttu-id="b467f-105">ExistingService (預設) </span><span class="sxs-lookup"><span data-stu-id="b467f-105">ExistingService (Default)</span></span>
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b467f-106">CreateService</span><span class="sxs-lookup"><span data-stu-id="b467f-106">CreateService</span></span>
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b467f-107">說明</span><span class="sxs-lookup"><span data-stu-id="b467f-107">DESCRIPTION</span></span>
<span data-ttu-id="b467f-108">**新的-add-azurevm** Cmdlet 會將新的虛擬機器新增至現有的 Azure 服務，或在已指定 *Location* 或 *AffinityGroup* 的情況下，在目前的訂閱中建立虛擬機器和服務。</span><span class="sxs-lookup"><span data-stu-id="b467f-108">The **New-AzureVM** cmdlet adds a new virtual machine to an existing Azure service, or creates a virtual machine and service in the current subscription if either the *Location* or *AffinityGroup* is specified.</span></span>

## <span data-ttu-id="b467f-109">示例</span><span class="sxs-lookup"><span data-stu-id="b467f-109">EXAMPLES</span></span>

### <span data-ttu-id="b467f-110">範例1：建立適用于 Windows 配置的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="b467f-110">Example 1: Create a virtual machine for a Windows configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

<span data-ttu-id="b467f-111">這個命令會根據 Windows 作業系統的虛擬機器設定建立設定設定，並使用它來建立指定地緣群組中的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b467f-111">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="b467f-112">範例2：建立 Linux 配置的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="b467f-112">Example 2: Create a virtual machine for a Linux configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

<span data-ttu-id="b467f-113">這個命令會根據 Linux 的虛擬機器配置來建立設定設定，並使用它來在指定的地緣群組中建立虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b467f-113">This command creates a provisioning configuration based on a virtual machine configuration for Linux, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="b467f-114">範例3：建立虛擬機器並新增資料磁片</span><span class="sxs-lookup"><span data-stu-id="b467f-114">Example 3: Create a virtual machine and add a data disk</span></span>
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

<span data-ttu-id="b467f-115">前兩個命令會使用 **AzureVMImage** Cmdlet 來取得可用的影像，並將其中一個圖像儲存在 $Image 變數中。</span><span class="sxs-lookup"><span data-stu-id="b467f-115">The first two commands get available images by using the **Get-AzureVMImage** cmdlet, and stores one of them in the $Image variable.</span></span>

<span data-ttu-id="b467f-116">這個命令會根據 Windows 作業系統的虛擬機器設定建立配設設定，並使用它來建立擁有 Azure 資料磁片的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b467f-116">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with an Azure data disk.</span></span>

### <span data-ttu-id="b467f-117">範例4：建立具有保留 IP 位址的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="b467f-117">Example 4: Create a virtual machine with a reserved IP address</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

<span data-ttu-id="b467f-118">這個命令會根據 Windows 作業系統的虛擬機器設定建立配設設定，並使用它來建立具有保留 IP 位址的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b467f-118">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with a reserved IP address.</span></span>

## <span data-ttu-id="b467f-119">參數</span><span class="sxs-lookup"><span data-stu-id="b467f-119">PARAMETERS</span></span>

### <span data-ttu-id="b467f-120">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="b467f-120">-AffinityGroup</span></span>
<span data-ttu-id="b467f-121">指定雲端服務所在的 Azure 地緣群組。</span><span class="sxs-lookup"><span data-stu-id="b467f-121">Specifies the Azure affinity group in which the cloud service resides.</span></span>
<span data-ttu-id="b467f-122">只有在這個 Cmdlet 建立雲端服務時，才需要這個參數。</span><span class="sxs-lookup"><span data-stu-id="b467f-122">This parameter is required only when this cmdlet creates a cloud service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-123">-DeploymentLabel</span><span class="sxs-lookup"><span data-stu-id="b467f-123">-DeploymentLabel</span></span>
<span data-ttu-id="b467f-124">指定部署的標籤。</span><span class="sxs-lookup"><span data-stu-id="b467f-124">Specifies a label for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-125">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="b467f-125">-DeploymentName</span></span>
<span data-ttu-id="b467f-126">指定部署名稱。</span><span class="sxs-lookup"><span data-stu-id="b467f-126">Specifies a deployment name.</span></span>
<span data-ttu-id="b467f-127">如果未指定，此 Cmdlet 會使用服務名稱作為部署名稱。</span><span class="sxs-lookup"><span data-stu-id="b467f-127">If not specified, this cmdlet uses the service name as the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-128">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="b467f-128">-DnsSettings</span></span>
<span data-ttu-id="b467f-129">指定定義新部署之 DNS 設定的 DNS 伺服器物件。</span><span class="sxs-lookup"><span data-stu-id="b467f-129">Specifies a DNS Server object that defines the DNS settings for the new deployment.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b467f-130">-InformationAction</span></span>
<span data-ttu-id="b467f-131">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="b467f-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b467f-132">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b467f-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b467f-133">持續</span><span class="sxs-lookup"><span data-stu-id="b467f-133">Continue</span></span>
- <span data-ttu-id="b467f-134">理會</span><span class="sxs-lookup"><span data-stu-id="b467f-134">Ignore</span></span>
- <span data-ttu-id="b467f-135">看</span><span class="sxs-lookup"><span data-stu-id="b467f-135">Inquire</span></span>
- <span data-ttu-id="b467f-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b467f-136">SilentlyContinue</span></span>
- <span data-ttu-id="b467f-137">停止</span><span class="sxs-lookup"><span data-stu-id="b467f-137">Stop</span></span>
- <span data-ttu-id="b467f-138">封存</span><span class="sxs-lookup"><span data-stu-id="b467f-138">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b467f-139">-InformationVariable</span></span>
<span data-ttu-id="b467f-140">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="b467f-140">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-141">-InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="b467f-141">-InternalLoadBalancerConfig</span></span>
<span data-ttu-id="b467f-142">指定內部負載平衡器。</span><span class="sxs-lookup"><span data-stu-id="b467f-142">Specifies an internal load balancer.</span></span>
<span data-ttu-id="b467f-143">不會使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="b467f-143">This parameter is not used.</span></span>

```yaml
Type: InternalLoadBalancerConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-144">-位置</span><span class="sxs-lookup"><span data-stu-id="b467f-144">-Location</span></span>
<span data-ttu-id="b467f-145">指定託管新服務的位置。</span><span class="sxs-lookup"><span data-stu-id="b467f-145">Specifies the location that hosts the new service.</span></span>
<span data-ttu-id="b467f-146">如果服務已存在，請勿指定此參數。</span><span class="sxs-lookup"><span data-stu-id="b467f-146">If the service already exists, do not specify this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-147">-設定檔</span><span class="sxs-lookup"><span data-stu-id="b467f-147">-Profile</span></span>
<span data-ttu-id="b467f-148">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b467f-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b467f-149">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="b467f-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-150">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="b467f-150">-ReservedIPName</span></span>
<span data-ttu-id="b467f-151">指定保留 IP 位址的名稱。</span><span class="sxs-lookup"><span data-stu-id="b467f-151">Specifies the name of the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-152">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="b467f-152">-ReverseDnsFqdn</span></span>
<span data-ttu-id="b467f-153">指定反向 DNS 的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="b467f-153">Specifies the fully-qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-154">-ServiceDescription</span><span class="sxs-lookup"><span data-stu-id="b467f-154">-ServiceDescription</span></span>
<span data-ttu-id="b467f-155">指定新服務的描述。</span><span class="sxs-lookup"><span data-stu-id="b467f-155">Specifies a description for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-156">-ServiceLabel</span><span class="sxs-lookup"><span data-stu-id="b467f-156">-ServiceLabel</span></span>
<span data-ttu-id="b467f-157">指定新服務的標籤。</span><span class="sxs-lookup"><span data-stu-id="b467f-157">Specifies a label for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b467f-158">-ServiceName</span></span>
<span data-ttu-id="b467f-159">指定新的或現有的服務名稱。</span><span class="sxs-lookup"><span data-stu-id="b467f-159">Specifies the new or existing service name.</span></span>

<span data-ttu-id="b467f-160">如果服務不存在，這個 Cmdlet 會為您建立。</span><span class="sxs-lookup"><span data-stu-id="b467f-160">If the service does not exist, this cmdlet creates it for you.</span></span>
<span data-ttu-id="b467f-161">使用 *Location* 或 *AffinityGroup* 參數來指定服務的建立位置。</span><span class="sxs-lookup"><span data-stu-id="b467f-161">Use the *Location* or *AffinityGroup* parameter to specify where to create the service.</span></span>

<span data-ttu-id="b467f-162">如果服務存在，則不需要 *Location* 或 *AffinityGroup* 參數。</span><span class="sxs-lookup"><span data-stu-id="b467f-162">If the service exists, the *Location* or *AffinityGroup* parameter is not needed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-163">-Vm</span><span class="sxs-lookup"><span data-stu-id="b467f-163">-VMs</span></span>
<span data-ttu-id="b467f-164">指定要建立的虛擬機器物件清單。</span><span class="sxs-lookup"><span data-stu-id="b467f-164">Specifies a list of virtual machine objects to create.</span></span>

```yaml
Type: PersistentVM[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-165">-VNetName</span><span class="sxs-lookup"><span data-stu-id="b467f-165">-VNetName</span></span>
<span data-ttu-id="b467f-166">指定此 Cmdlet 部署虛擬機器的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="b467f-166">Specifies the virtual network name where this cmdlet deploys the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-167">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="b467f-167">-WaitForBoot</span></span>
<span data-ttu-id="b467f-168">指定此 Cmdlet 會等待虛擬機器達到 **ReadyRole** 狀態。</span><span class="sxs-lookup"><span data-stu-id="b467f-168">Specifies that this cmdlet waits for the virtual machine to reach the **ReadyRole** state.</span></span>
<span data-ttu-id="b467f-169">如果虛擬機器在等待時處於下列其中一種狀態： FailedStartingVM、ProvisioningFailed、ProvisioningTimeout，則此 Cmdlet 會失敗。</span><span class="sxs-lookup"><span data-stu-id="b467f-169">This cmdlet fails if the virtual machine falls in one of the following states while waiting: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b467f-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b467f-170">CommonParameters</span></span>
<span data-ttu-id="b467f-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b467f-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b467f-172">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b467f-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b467f-173">輸入</span><span class="sxs-lookup"><span data-stu-id="b467f-173">INPUTS</span></span>

## <span data-ttu-id="b467f-174">輸出</span><span class="sxs-lookup"><span data-stu-id="b467f-174">OUTPUTS</span></span>

## <span data-ttu-id="b467f-175">筆記</span><span class="sxs-lookup"><span data-stu-id="b467f-175">NOTES</span></span>

## <span data-ttu-id="b467f-176">相關連結</span><span class="sxs-lookup"><span data-stu-id="b467f-176">RELATED LINKS</span></span>

[<span data-ttu-id="b467f-177">附加 AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="b467f-177">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="b467f-178">附加 AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="b467f-178">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="b467f-179">AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="b467f-179">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="b467f-180">新-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="b467f-180">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


