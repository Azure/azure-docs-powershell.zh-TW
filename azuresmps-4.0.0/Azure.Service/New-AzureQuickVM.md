---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967355"
---
# <span data-ttu-id="a5a68-101">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="a5a68-101">New-AzureQuickVM</span></span>

## <span data-ttu-id="a5a68-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a5a68-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a68-103">配置並建立 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5a68-103">Configures and creates an Azure virtual machine.</span></span>

## <span data-ttu-id="a5a68-104">句法</span><span class="sxs-lookup"><span data-stu-id="a5a68-104">SYNTAX</span></span>

### <span data-ttu-id="a5a68-105">Windows (預設) </span><span class="sxs-lookup"><span data-stu-id="a5a68-105">Windows (Default)</span></span>
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a5a68-106">Linux</span><span class="sxs-lookup"><span data-stu-id="a5a68-106">Linux</span></span>
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a5a68-107">說明</span><span class="sxs-lookup"><span data-stu-id="a5a68-107">DESCRIPTION</span></span>
<span data-ttu-id="a5a68-108">**新的-AzureQuickVM** Cmdlet 會設定並建立 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5a68-108">The **New-AzureQuickVM** cmdlet configures and creates an Azure virtual machine.</span></span>
<span data-ttu-id="a5a68-109">這個 Cmdlet 可以將虛擬機器部署到現有的 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="a5a68-109">This cmdlet can deploy a virtual machine into an existing Azure service.</span></span>
<span data-ttu-id="a5a68-110">這個 Cmdlet 也可以建立託管新虛擬機器的 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="a5a68-110">This cmdlet can alternatively create an Azure service that hosts the new virtual machine.</span></span>

## <span data-ttu-id="a5a68-111">示例</span><span class="sxs-lookup"><span data-stu-id="a5a68-111">EXAMPLES</span></span>

### <span data-ttu-id="a5a68-112">範例1：建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="a5a68-112">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

<span data-ttu-id="a5a68-113">這個命令會建立在現有的服務中執行 Windows 作業系統的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5a68-113">This command creates a virtual machine that runs the Windows operating system in an existing service.</span></span>
<span data-ttu-id="a5a68-114">這個 Cmdlet 會以指定的映射為虛擬機器基礎。</span><span class="sxs-lookup"><span data-stu-id="a5a68-114">The cmdlet bases the virtual machine on the specified image.</span></span>
<span data-ttu-id="a5a68-115">命令會指定 *WaitForBoot* 參數。</span><span class="sxs-lookup"><span data-stu-id="a5a68-115">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="a5a68-116">因此，此 Cmdlet 會等待虛擬機器開始進行。</span><span class="sxs-lookup"><span data-stu-id="a5a68-116">Therefore, the cmdlet waits for the virtual machine to start.</span></span>

### <span data-ttu-id="a5a68-117">範例2：使用憑證建立虛擬機器</span><span class="sxs-lookup"><span data-stu-id="a5a68-117">Example 2: Create a virtual machine that by using certificates</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

<span data-ttu-id="a5a68-118">第一個命令會從書店取得憑證，並將其儲存在 $certs 變數中。</span><span class="sxs-lookup"><span data-stu-id="a5a68-118">The first command gets certificates from a store, and stores them in the $certs variable.</span></span>

<span data-ttu-id="a5a68-119">第二個命令會建立在現有的服務中執行 Windows 作業系統的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5a68-119">The second command creates a virtual machine that runs the Windows operating system in an existing service from an image.</span></span>
<span data-ttu-id="a5a68-120">根據預設，WinRM Https 偵聽程式在虛擬機器上是啟用的。</span><span class="sxs-lookup"><span data-stu-id="a5a68-120">By default, WinRM Https listener is enabled on the virtual machine.</span></span>
<span data-ttu-id="a5a68-121">命令會指定 *WaitForBoot* 參數。</span><span class="sxs-lookup"><span data-stu-id="a5a68-121">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="a5a68-122">因此，此 Cmdlet 會等待虛擬機器開始進行。</span><span class="sxs-lookup"><span data-stu-id="a5a68-122">Therefore, the cmdlet waits for the virtual machine to start.</span></span>
<span data-ttu-id="a5a68-123">該命令會將 WinRM 憑證及 X509Certificates 上傳到託管服務。</span><span class="sxs-lookup"><span data-stu-id="a5a68-123">The command uploads a WinRM Certificate and X509Certificates to the hosted service.</span></span>

### <span data-ttu-id="a5a68-124">範例3：建立執行 Linux 作業系統的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="a5a68-124">Example 3: Create a virtual machine that runs the Linux operating system</span></span>
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

<span data-ttu-id="a5a68-125">這個命令會建立一個從影像執行 Linux 作業系統的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5a68-125">This command creates a virtual machine that runs the Linux operating system from an image.</span></span>
<span data-ttu-id="a5a68-126">這個命令會建立服務來託管新的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5a68-126">This command creates a service to host the new virtual machine.</span></span>
<span data-ttu-id="a5a68-127">該命令會指定服務的位置。</span><span class="sxs-lookup"><span data-stu-id="a5a68-127">The command specifies a location for the service.</span></span>

### <span data-ttu-id="a5a68-128">範例4：建立虛擬機器並建立服務以託管新的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="a5a68-128">Example 4: Create a virtual machine and create a service to host the new virtual machine</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

<span data-ttu-id="a5a68-129">第一個命令會使用 **AzureLocation** Cmdlet 來取得位置，然後將它們儲存在 $Locations 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="a5a68-129">The first command gets locations by using the **Get-AzureLocation** cmdlet, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="a5a68-130">第二個命令會使用 **AzureVMImage** Cmdlet 取得可用的影像，然後將它們儲存在 $Images 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="a5a68-130">The second command gets available images by using the **Get-AzureVMImage** cmdlet, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="a5a68-131">最後一個命令會建立一個名為 VirtualMachine25 的大型虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5a68-131">The final command creates a large virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="a5a68-132">虛擬機器會執行 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="a5a68-132">The virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="a5a68-133">它是以 $Images 中的其中一個圖像為基礎。</span><span class="sxs-lookup"><span data-stu-id="a5a68-133">It is based on one of the images in $Images.</span></span>
<span data-ttu-id="a5a68-134">此命令會為新的虛擬機器建立名為 ContosoService03 的服務。</span><span class="sxs-lookup"><span data-stu-id="a5a68-134">The command creates a service named ContosoService03 for the new virtual machine.</span></span>
<span data-ttu-id="a5a68-135">服務位於 $Locations 中的位置。</span><span class="sxs-lookup"><span data-stu-id="a5a68-135">The service is in a location in $Locations.</span></span>

### <span data-ttu-id="a5a68-136">範例5：建立擁有保留 IP 名稱的虛擬機器</span><span class="sxs-lookup"><span data-stu-id="a5a68-136">Example 5: Create a virtual machine that has a reserved IP name</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

<span data-ttu-id="a5a68-137">第一個命令會取得位置，然後將它們儲存在 $Locations 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="a5a68-137">The first command gets locations, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="a5a68-138">第二個命令會取得可用的影像，然後將它們儲存在 $Images 陣列變數中。</span><span class="sxs-lookup"><span data-stu-id="a5a68-138">The second command gets available images, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="a5a68-139">最終命令會根據 $Images 中的其中一個圖像，建立一個名為 VirtualMachine27 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5a68-139">The final command creates a virtual machine named VirtualMachine27 based on one of the images in $Images.</span></span>
<span data-ttu-id="a5a68-140">命令會在 $Locations 中的位置建立服務。</span><span class="sxs-lookup"><span data-stu-id="a5a68-140">The command creates a service in a location in $Locations.</span></span>
<span data-ttu-id="a5a68-141">虛擬機器有保留的 IP 名稱，先前儲存在 $ipName 變數中。</span><span class="sxs-lookup"><span data-stu-id="a5a68-141">The virtual machine has a reserved IP name, previously stored in the $ipName variable.</span></span>

## <span data-ttu-id="a5a68-142">參數</span><span class="sxs-lookup"><span data-stu-id="a5a68-142">PARAMETERS</span></span>

### <span data-ttu-id="a5a68-143">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="a5a68-143">-AdminUsername</span></span>
<span data-ttu-id="a5a68-144">指定此 Cmdlet 在虛擬機器上建立之系統管理員帳戶的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a68-144">Specifies the user name of the Administrator account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-145">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="a5a68-145">-AffinityGroup</span></span>
<span data-ttu-id="a5a68-146">指定虛擬機器的地緣群組。</span><span class="sxs-lookup"><span data-stu-id="a5a68-146">Specifies the affinity group for the virtual machine.</span></span>
<span data-ttu-id="a5a68-147">只有在這個 Cmdlet 為虛擬機器建立 Azure 服務時，才能指定此參數或 *Location* 參數。</span><span class="sxs-lookup"><span data-stu-id="a5a68-147">Specify this parameter or the *Location* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="a5a68-148">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="a5a68-148">-AvailabilitySetName</span></span>
<span data-ttu-id="a5a68-149">指定此 Cmdlet 建立虛擬機器之可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a68-149">Specifies the name of the availability set in which this cmdlet creates the virtual machine.</span></span>

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

### <span data-ttu-id="a5a68-150">-憑證</span><span class="sxs-lookup"><span data-stu-id="a5a68-150">-Certificates</span></span>
<span data-ttu-id="a5a68-151">指定此 Cmdlet 用來建立服務的憑證清單。</span><span class="sxs-lookup"><span data-stu-id="a5a68-151">Specifies a list of certificates that this cmdlet uses to create the service.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-152">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="a5a68-152">-CustomDataFile</span></span>
<span data-ttu-id="a5a68-153">指定虛擬機器的資料檔案。</span><span class="sxs-lookup"><span data-stu-id="a5a68-153">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="a5a68-154">這個 Cmdlet 會將檔案的內容編碼為 Base64。</span><span class="sxs-lookup"><span data-stu-id="a5a68-154">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="a5a68-155">檔案長度必須小於 64 kb。</span><span class="sxs-lookup"><span data-stu-id="a5a68-155">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="a5a68-156">如果客體作業系統是 Windows 作業系統，這個 Cmdlet 會將這個資料儲存為一個名為%SYSTEMDRIVE%\AzureData\CustomData.bin. 的二進位檔案。</span><span class="sxs-lookup"><span data-stu-id="a5a68-156">If the guest operating system is the Windows operating system, this cmdlet saves this data as a binary file that is named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="a5a68-157">如果客體作業系統是 Linux，此 Cmdlet 會使用 ovf-env.xml 檔案傳遞資料。</span><span class="sxs-lookup"><span data-stu-id="a5a68-157">If the guest operating system is Linux, this cmdlet passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="a5a68-158">安裝會將該檔案複製到/var/lib/waagent 目錄。</span><span class="sxs-lookup"><span data-stu-id="a5a68-158">Installation copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="a5a68-159">此代理程式也會在/var/lib/waagent/CustomData. 中儲存 Base64 編碼資料</span><span class="sxs-lookup"><span data-stu-id="a5a68-159">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="a5a68-160">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="a5a68-160">-DisableGuestAgent</span></span>
<span data-ttu-id="a5a68-161">表示此 Cmdlet 會將基礎結構停成服務 (IaaS) 提供來賓代理程式。</span><span class="sxs-lookup"><span data-stu-id="a5a68-161">Indicates that this cmdlet disables the infrastructure as a service (IaaS) provision guest agent.</span></span>

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

### <span data-ttu-id="a5a68-162">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="a5a68-162">-DisableWinRMHttps</span></span>
<span data-ttu-id="a5a68-163">表示此 Cmdlet 停用 HTTPS 上的 Windows 遠端系統管理 (WinRM) 。</span><span class="sxs-lookup"><span data-stu-id="a5a68-163">Indicates that this cmdlet disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="a5a68-164">根據預設，WinRM 是透過 HTTPS 啟用的。</span><span class="sxs-lookup"><span data-stu-id="a5a68-164">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-165">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="a5a68-165">-DnsSettings</span></span>
<span data-ttu-id="a5a68-166">指定定義新部署之 DNS 設定的 DNS 伺服器物件陣列。</span><span class="sxs-lookup"><span data-stu-id="a5a68-166">Specifies an array of DNS server objects that defines the DNS settings for the new deployment.</span></span>
<span data-ttu-id="a5a68-167">若要建立 **DnsServer** 物件，請使用 **AzureDns** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a5a68-167">To create a **DnsServer** object, use the **New-AzureDns** cmdlet.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-168">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="a5a68-168">-EnableWinRMHttp</span></span>
<span data-ttu-id="a5a68-169">表示此 Cmdlet 啟用 WinRM over HTTP。</span><span class="sxs-lookup"><span data-stu-id="a5a68-169">Indicates that this cmdlet enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-170">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="a5a68-170">-HostCaching</span></span>
<span data-ttu-id="a5a68-171">指定作業系統磁片的主機緩衝模式。</span><span class="sxs-lookup"><span data-stu-id="a5a68-171">Specifies the host caching mode for the operating system disk.</span></span>
<span data-ttu-id="a5a68-172">有效值為：</span><span class="sxs-lookup"><span data-stu-id="a5a68-172">Valid values are:</span></span> 

- <span data-ttu-id="a5a68-173">唯讀</span><span class="sxs-lookup"><span data-stu-id="a5a68-173">ReadOnly</span></span>
- <span data-ttu-id="a5a68-174">讀</span><span class="sxs-lookup"><span data-stu-id="a5a68-174">ReadWrite</span></span>

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

### <span data-ttu-id="a5a68-175">-ImageName</span><span class="sxs-lookup"><span data-stu-id="a5a68-175">-ImageName</span></span>
<span data-ttu-id="a5a68-176">指定此 Cmdlet 用來建立作業系統磁片的磁片影像名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a68-176">Specifies the name of the disk image this cmdlet uses to create the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-177">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a5a68-177">-InformationAction</span></span>
<span data-ttu-id="a5a68-178">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="a5a68-178">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a5a68-179">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="a5a68-179">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a5a68-180">持續</span><span class="sxs-lookup"><span data-stu-id="a5a68-180">Continue</span></span>
- <span data-ttu-id="a5a68-181">理會</span><span class="sxs-lookup"><span data-stu-id="a5a68-181">Ignore</span></span>
- <span data-ttu-id="a5a68-182">看</span><span class="sxs-lookup"><span data-stu-id="a5a68-182">Inquire</span></span>
- <span data-ttu-id="a5a68-183">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a5a68-183">SilentlyContinue</span></span>
- <span data-ttu-id="a5a68-184">停止</span><span class="sxs-lookup"><span data-stu-id="a5a68-184">Stop</span></span>
- <span data-ttu-id="a5a68-185">封存</span><span class="sxs-lookup"><span data-stu-id="a5a68-185">Suspend</span></span>

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

### <span data-ttu-id="a5a68-186">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a5a68-186">-InformationVariable</span></span>
<span data-ttu-id="a5a68-187">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="a5a68-187">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a5a68-188">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="a5a68-188">-InstanceSize</span></span>
<span data-ttu-id="a5a68-189">指定實例的大小。</span><span class="sxs-lookup"><span data-stu-id="a5a68-189">Specifies the size of the instance.</span></span>
<span data-ttu-id="a5a68-190">有效值為：</span><span class="sxs-lookup"><span data-stu-id="a5a68-190">Valid values are:</span></span> 

- <span data-ttu-id="a5a68-191">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="a5a68-191">ExtraSmall</span></span>
- <span data-ttu-id="a5a68-192">小規模</span><span class="sxs-lookup"><span data-stu-id="a5a68-192">Small</span></span>
- <span data-ttu-id="a5a68-193">深淺</span><span class="sxs-lookup"><span data-stu-id="a5a68-193">Medium</span></span>
- <span data-ttu-id="a5a68-194">大中型</span><span class="sxs-lookup"><span data-stu-id="a5a68-194">Large</span></span>
- <span data-ttu-id="a5a68-195">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="a5a68-195">ExtraLarge</span></span>
- <span data-ttu-id="a5a68-196">A5</span><span class="sxs-lookup"><span data-stu-id="a5a68-196">A5</span></span>
- <span data-ttu-id="a5a68-197">A6</span><span class="sxs-lookup"><span data-stu-id="a5a68-197">A6</span></span>
- <span data-ttu-id="a5a68-198">A7</span><span class="sxs-lookup"><span data-stu-id="a5a68-198">A7</span></span>
- <span data-ttu-id="a5a68-199">A8</span><span class="sxs-lookup"><span data-stu-id="a5a68-199">A8</span></span>
- <span data-ttu-id="a5a68-200">A9</span><span class="sxs-lookup"><span data-stu-id="a5a68-200">A9</span></span>
- <span data-ttu-id="a5a68-201">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="a5a68-201">Basic_A0</span></span>
- <span data-ttu-id="a5a68-202">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="a5a68-202">Basic_A1</span></span>
- <span data-ttu-id="a5a68-203">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="a5a68-203">Basic_A2</span></span>
- <span data-ttu-id="a5a68-204">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="a5a68-204">Basic_A3</span></span>
- <span data-ttu-id="a5a68-205">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="a5a68-205">Basic_A4</span></span>
- <span data-ttu-id="a5a68-206">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="a5a68-206">Standard_D1</span></span>
- <span data-ttu-id="a5a68-207">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="a5a68-207">Standard_D2</span></span>
- <span data-ttu-id="a5a68-208">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="a5a68-208">Standard_D3</span></span>
- <span data-ttu-id="a5a68-209">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="a5a68-209">Standard_D4</span></span>
- <span data-ttu-id="a5a68-210">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="a5a68-210">Standard_D11</span></span>
- <span data-ttu-id="a5a68-211">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="a5a68-211">Standard_D12</span></span>
- <span data-ttu-id="a5a68-212">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="a5a68-212">Standard_D13</span></span>
- <span data-ttu-id="a5a68-213">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="a5a68-213">Standard_D14</span></span>

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

### <span data-ttu-id="a5a68-214">-Linux</span><span class="sxs-lookup"><span data-stu-id="a5a68-214">-Linux</span></span>
<span data-ttu-id="a5a68-215">表示此 Cmdlet 會建立以 Linux 為基礎的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5a68-215">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-216">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="a5a68-216">-LinuxUser</span></span>
<span data-ttu-id="a5a68-217">指定此 Cmdlet 在虛擬機器上建立之 Linux 系統管理員帳戶的使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a68-217">Specifies the user name of the Linux administrative account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-218">-位置</span><span class="sxs-lookup"><span data-stu-id="a5a68-218">-Location</span></span>
<span data-ttu-id="a5a68-219">指定託管虛擬機器的 Azure 資料中心。</span><span class="sxs-lookup"><span data-stu-id="a5a68-219">Specifies the Azure datacenter that hosts the virtual machine.</span></span>
<span data-ttu-id="a5a68-220">如果您指定此參數，則 Cmdlet 會在指定的位置建立 Azure 服務。</span><span class="sxs-lookup"><span data-stu-id="a5a68-220">If you specify this parameter, the cmdlet creates an Azure service in the specified location.</span></span>
<span data-ttu-id="a5a68-221">只有在這個 Cmdlet 為虛擬機器建立 Azure 服務時，才能指定此參數或 *AffinityGroup* 參數。</span><span class="sxs-lookup"><span data-stu-id="a5a68-221">Specify this parameter or the *AffinityGroup* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="a5a68-222">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="a5a68-222">-MediaLocation</span></span>
<span data-ttu-id="a5a68-223">指定此 Cmdlet 建立虛擬機器磁片的 Azure 儲存位置。</span><span class="sxs-lookup"><span data-stu-id="a5a68-223">Specifies the Azure Storage location where this cmdlet creates the virtual machines disks.</span></span>

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

### <span data-ttu-id="a5a68-224">-名稱</span><span class="sxs-lookup"><span data-stu-id="a5a68-224">-Name</span></span>
<span data-ttu-id="a5a68-225">指定此 Cmdlet 所建立之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a68-225">Specifies the name of the virtual machine that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a5a68-226">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="a5a68-226">-NoExportPrivateKey</span></span>
<span data-ttu-id="a5a68-227">指示此設定不會上傳私用金鑰。</span><span class="sxs-lookup"><span data-stu-id="a5a68-227">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-228">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="a5a68-228">-NoWinRMEndpoint</span></span>
<span data-ttu-id="a5a68-229">指示此 Cmdlet 不會為虛擬機器新增 WinRM 端點。</span><span class="sxs-lookup"><span data-stu-id="a5a68-229">Indicates that this cmdlet does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-230">-Password</span><span class="sxs-lookup"><span data-stu-id="a5a68-230">-Password</span></span>
<span data-ttu-id="a5a68-231">指定系統管理帳戶的密碼。</span><span class="sxs-lookup"><span data-stu-id="a5a68-231">Specifies the password for the administrative account.</span></span>

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

### <span data-ttu-id="a5a68-232">-設定檔</span><span class="sxs-lookup"><span data-stu-id="a5a68-232">-Profile</span></span>
<span data-ttu-id="a5a68-233">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="a5a68-233">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a5a68-234">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="a5a68-234">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a5a68-235">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="a5a68-235">-ReservedIPName</span></span>
<span data-ttu-id="a5a68-236">指定保留的 IP 名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a68-236">Specifies the reserved IP name.</span></span>

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

### <span data-ttu-id="a5a68-237">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="a5a68-237">-ReverseDnsFqdn</span></span>
<span data-ttu-id="a5a68-238">指定反向 DNS 查詢的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a68-238">Specifies the fully qualified domain name for reverse DNS look up.</span></span>

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

### <span data-ttu-id="a5a68-239">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a5a68-239">-ServiceName</span></span>
<span data-ttu-id="a5a68-240">指定此 Cmdlet 將新的虛擬機器新增至其中的新或現有 Azure 服務的名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a68-240">Specifies the name of a new or existing Azure service to which this cmdlet adds the new virtual machine.</span></span>

<span data-ttu-id="a5a68-241">如果您指定新服務，此 Cmdlet 會建立它。</span><span class="sxs-lookup"><span data-stu-id="a5a68-241">If you specify a new service, this cmdlets creates it.</span></span>
<span data-ttu-id="a5a68-242">若要建立新的服務，您必須指定 *Location* 或 *AffinityGroup* 參數。</span><span class="sxs-lookup"><span data-stu-id="a5a68-242">To create a new service, you must specify the *Location* or *AffinityGroup* parameter.</span></span>

<span data-ttu-id="a5a68-243">如果您指定現有的服務，請勿指定 *Location* 或 *AffinityGroup* 。</span><span class="sxs-lookup"><span data-stu-id="a5a68-243">If you specify an existing service, do not specify *Location* or *AffinityGroup*.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-244">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="a5a68-244">-SSHKeyPairs</span></span>
<span data-ttu-id="a5a68-245">指定 SSH 金鑰組。</span><span class="sxs-lookup"><span data-stu-id="a5a68-245">Specifies SSH key pairs.</span></span>

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-246">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="a5a68-246">-SSHPublicKeys</span></span>
<span data-ttu-id="a5a68-247">指定 SSH 公開金鑰。</span><span class="sxs-lookup"><span data-stu-id="a5a68-247">Specifies SSH public keys.</span></span>

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-248">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="a5a68-248">-SubnetNames</span></span>
<span data-ttu-id="a5a68-249">指定虛擬機器子網的名稱陣列。</span><span class="sxs-lookup"><span data-stu-id="a5a68-249">Specifies an array of names of subnet for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-250">-VNetName</span><span class="sxs-lookup"><span data-stu-id="a5a68-250">-VNetName</span></span>
<span data-ttu-id="a5a68-251">指定虛擬機器的虛擬網路名稱。</span><span class="sxs-lookup"><span data-stu-id="a5a68-251">Specifies the name of a virtual network for the virtual machine.</span></span>

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

### <span data-ttu-id="a5a68-252">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="a5a68-252">-WaitForBoot</span></span>
<span data-ttu-id="a5a68-253">表示此 Cmdlet 會等待虛擬機器到達狀態 ReadyRole。</span><span class="sxs-lookup"><span data-stu-id="a5a68-253">Indicates that this cmdlet waits for the virtual machine to reach the state ReadyRole.</span></span>
<span data-ttu-id="a5a68-254">如果虛擬機器達到下列其中一種狀態，則 Cmdlet 會失敗： FailedStartingVM、ProvisioningFailed 或 ProvisioningTimeout。</span><span class="sxs-lookup"><span data-stu-id="a5a68-254">If the virtual machine reaches one of the following states, the cmdlet fails: FailedStartingVM, ProvisioningFailed, or ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="a5a68-255">-Windows</span><span class="sxs-lookup"><span data-stu-id="a5a68-255">-Windows</span></span>
<span data-ttu-id="a5a68-256">表示此 Cmdlet 會建立 Windows 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="a5a68-256">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-257">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="a5a68-257">-WinRMCertificate</span></span>
<span data-ttu-id="a5a68-258">指定此 Cmdlet 與 WinRM 端點相關聯的憑證。</span><span class="sxs-lookup"><span data-stu-id="a5a68-258">Specifies a certificate that this cmdlet associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-259">-X509Certificates</span><span class="sxs-lookup"><span data-stu-id="a5a68-259">-X509Certificates</span></span>
<span data-ttu-id="a5a68-260">指定部署至託管服務的 X509 憑證陣列。</span><span class="sxs-lookup"><span data-stu-id="a5a68-260">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a68-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a68-261">CommonParameters</span></span>
<span data-ttu-id="a5a68-262">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a5a68-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a68-263">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a5a68-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a68-264">輸入</span><span class="sxs-lookup"><span data-stu-id="a5a68-264">INPUTS</span></span>

## <span data-ttu-id="a5a68-265">輸出</span><span class="sxs-lookup"><span data-stu-id="a5a68-265">OUTPUTS</span></span>

## <span data-ttu-id="a5a68-266">筆記</span><span class="sxs-lookup"><span data-stu-id="a5a68-266">NOTES</span></span>

## <span data-ttu-id="a5a68-267">相關連結</span><span class="sxs-lookup"><span data-stu-id="a5a68-267">RELATED LINKS</span></span>

[<span data-ttu-id="a5a68-268">AzureLocation</span><span class="sxs-lookup"><span data-stu-id="a5a68-268">Get-AzureLocation</span></span>](./Get-AzureLocation.md)

[<span data-ttu-id="a5a68-269">AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="a5a68-269">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="a5a68-270">新-AzureDns</span><span class="sxs-lookup"><span data-stu-id="a5a68-270">New-AzureDns</span></span>](./New-AzureDns.md)


