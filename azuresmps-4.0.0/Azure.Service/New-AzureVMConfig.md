---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6DFD49F-26A5-4199-A844-CA0FC405BEDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f9fc407e2cf7375708fe82253f3d2fb40eb78f60
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967643"
---
# <span data-ttu-id="58882-101">New-AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="58882-101">New-AzureVMConfig</span></span>

## <span data-ttu-id="58882-102">摘要</span><span class="sxs-lookup"><span data-stu-id="58882-102">SYNOPSIS</span></span>
<span data-ttu-id="58882-103">建立 Azure 虛擬機器設定物件。</span><span class="sxs-lookup"><span data-stu-id="58882-103">Creates an Azure virtual machine configuration object.</span></span>

## <span data-ttu-id="58882-104">句法</span><span class="sxs-lookup"><span data-stu-id="58882-104">SYNTAX</span></span>

### <span data-ttu-id="58882-105">ImageName (預設) </span><span class="sxs-lookup"><span data-stu-id="58882-105">ImageName (Default)</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-ImageName] <String> [[-MediaLocation] <String>]
 [[-DiskLabel] <String>] [-DisableBootDiagnostics] [-LicenseType <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="58882-106">DiskName</span><span class="sxs-lookup"><span data-stu-id="58882-106">DiskName</span></span>
```
New-AzureVMConfig [-Name] <String> [-InstanceSize] <String> [[-HostCaching] <String>]
 [[-AvailabilitySetName] <String>] [[-Label] <String>] [-DiskName] <String> [-DisableBootDiagnostics]
 [-LicenseType <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="58882-107">說明</span><span class="sxs-lookup"><span data-stu-id="58882-107">DESCRIPTION</span></span>
<span data-ttu-id="58882-108">**新的-AzureVMConfig** Cmdlet 會建立 Azure 虛擬機器設定物件。</span><span class="sxs-lookup"><span data-stu-id="58882-108">The **New-AzureVMConfig** cmdlet creates an Azure  virtual machine configuration object.</span></span>
<span data-ttu-id="58882-109">您可以使用這個物件來執行新的部署，並將新的虛擬機器新增至現有的部署。</span><span class="sxs-lookup"><span data-stu-id="58882-109">You can use this object to perform a new deployment and add a new virtual machine to an existing deployment.</span></span>

## <span data-ttu-id="58882-110">示例</span><span class="sxs-lookup"><span data-stu-id="58882-110">EXAMPLES</span></span>

### <span data-ttu-id="58882-111">範例1：建立 Windows 虛擬機器設定</span><span class="sxs-lookup"><span data-stu-id="58882-111">Example 1: Create a Windows virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[4].ImageName 
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Windows -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="58882-112">這個命令會建立具有作業系統磁片、資料磁片與設定設定的 Windows 虛擬機器設定。</span><span class="sxs-lookup"><span data-stu-id="58882-112">This command creates a Windows virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="58882-113">然後使用此設定來建立新的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="58882-113">This configuration is then used to create a new virtual machine.</span></span>

### <span data-ttu-id="58882-114">範例2：建立 Linux 虛擬機器配置</span><span class="sxs-lookup"><span data-stu-id="58882-114">Example 2: Create a Linux virtual machine configuration</span></span>
```
PS C:\> $Image = (Get-AzureVMImage)[7].ImageName
C:\PS> New-AzureVMConfig -Name "MyVM1" -InstanceSize ExtraSmall -ImageName $Image | Add-AzureProvisioningConfig -Linux -LinuxUser $LinuxUser -Password $AdminPassword | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "Datadisk1" -LUN 0 | New-AzureVM -ServiceName "MySvc1"
```

<span data-ttu-id="58882-115">這個命令會建立新的 Linux 虛擬機器設定，其中包含作業系統磁片、資料磁片與配設定設定。</span><span class="sxs-lookup"><span data-stu-id="58882-115">This command creates a new Linux virtual machine configuration with operating system disk, data disk and provisioning configuration.</span></span>
<span data-ttu-id="58882-116">然後使用此設定來建立新的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="58882-116">This configuration is then used to create a new virtual machine.</span></span>

## <span data-ttu-id="58882-117">參數</span><span class="sxs-lookup"><span data-stu-id="58882-117">PARAMETERS</span></span>

### <span data-ttu-id="58882-118">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="58882-118">-AvailabilitySetName</span></span>
<span data-ttu-id="58882-119">指定可用性集的名稱。</span><span class="sxs-lookup"><span data-stu-id="58882-119">Specifies the name of the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58882-120">-DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="58882-120">-DisableBootDiagnostics</span></span>
<span data-ttu-id="58882-121">指示設定停用啟動診斷程式。</span><span class="sxs-lookup"><span data-stu-id="58882-121">Indicates that the configuration disables boot diagnostics.</span></span>
<span data-ttu-id="58882-122">根據預設，啟動診斷程式是在虛擬機器上啟用。</span><span class="sxs-lookup"><span data-stu-id="58882-122">By default, boot diagnostics are enabled on the virtual machine.</span></span>

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

### <span data-ttu-id="58882-123">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="58882-123">-DiskLabel</span></span>
<span data-ttu-id="58882-124">指定作業系統磁片的標籤。</span><span class="sxs-lookup"><span data-stu-id="58882-124">Specifies a label for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58882-125">-DiskName</span><span class="sxs-lookup"><span data-stu-id="58882-125">-DiskName</span></span>
<span data-ttu-id="58882-126">指定作業系統磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="58882-126">Specifies a name for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: DiskName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58882-127">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="58882-127">-HostCaching</span></span>
<span data-ttu-id="58882-128">指定作業系統磁片的主機緩衝模式。</span><span class="sxs-lookup"><span data-stu-id="58882-128">Specifies the host caching mode for the operating system disk.</span></span>

<span data-ttu-id="58882-129">有效值為：</span><span class="sxs-lookup"><span data-stu-id="58882-129">Valid values are:</span></span>

- <span data-ttu-id="58882-130">唯讀</span><span class="sxs-lookup"><span data-stu-id="58882-130">ReadOnly</span></span>
- <span data-ttu-id="58882-131">讀</span><span class="sxs-lookup"><span data-stu-id="58882-131">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58882-132">-ImageName</span><span class="sxs-lookup"><span data-stu-id="58882-132">-ImageName</span></span>
<span data-ttu-id="58882-133">指定要用於作業系統磁片的虛擬機器影像名稱。</span><span class="sxs-lookup"><span data-stu-id="58882-133">Specifies the name of the virtual machine image to use for the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58882-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="58882-134">-InformationAction</span></span>
<span data-ttu-id="58882-135">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="58882-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="58882-136">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="58882-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="58882-137">持續</span><span class="sxs-lookup"><span data-stu-id="58882-137">Continue</span></span>
- <span data-ttu-id="58882-138">理會</span><span class="sxs-lookup"><span data-stu-id="58882-138">Ignore</span></span>
- <span data-ttu-id="58882-139">看</span><span class="sxs-lookup"><span data-stu-id="58882-139">Inquire</span></span>
- <span data-ttu-id="58882-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="58882-140">SilentlyContinue</span></span>
- <span data-ttu-id="58882-141">停止</span><span class="sxs-lookup"><span data-stu-id="58882-141">Stop</span></span>
- <span data-ttu-id="58882-142">封存</span><span class="sxs-lookup"><span data-stu-id="58882-142">Suspend</span></span>

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

### <span data-ttu-id="58882-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="58882-143">-InformationVariable</span></span>
<span data-ttu-id="58882-144">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="58882-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="58882-145">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="58882-145">-InstanceSize</span></span>
<span data-ttu-id="58882-146">指定實例的大小。</span><span class="sxs-lookup"><span data-stu-id="58882-146">Specifies the size of the instance.</span></span>

<span data-ttu-id="58882-147">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="58882-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="58882-148">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="58882-148">ExtraSmall</span></span>
- <span data-ttu-id="58882-149">小規模</span><span class="sxs-lookup"><span data-stu-id="58882-149">Small</span></span>
- <span data-ttu-id="58882-150">深淺</span><span class="sxs-lookup"><span data-stu-id="58882-150">Medium</span></span>
- <span data-ttu-id="58882-151">大中型</span><span class="sxs-lookup"><span data-stu-id="58882-151">Large</span></span>
- <span data-ttu-id="58882-152">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="58882-152">ExtraLarge</span></span>
- <span data-ttu-id="58882-153">A5</span><span class="sxs-lookup"><span data-stu-id="58882-153">A5</span></span>
- <span data-ttu-id="58882-154">A6</span><span class="sxs-lookup"><span data-stu-id="58882-154">A6</span></span>
- <span data-ttu-id="58882-155">A7</span><span class="sxs-lookup"><span data-stu-id="58882-155">A7</span></span>
- <span data-ttu-id="58882-156">A8</span><span class="sxs-lookup"><span data-stu-id="58882-156">A8</span></span>
- <span data-ttu-id="58882-157">A9</span><span class="sxs-lookup"><span data-stu-id="58882-157">A9</span></span>
- <span data-ttu-id="58882-158">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="58882-158">Basic_A0</span></span>
- <span data-ttu-id="58882-159">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="58882-159">Basic_A1</span></span>
- <span data-ttu-id="58882-160">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="58882-160">Basic_A2</span></span>
- <span data-ttu-id="58882-161">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="58882-161">Basic_A3</span></span>
- <span data-ttu-id="58882-162">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="58882-162">Basic_A4</span></span>
- <span data-ttu-id="58882-163">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="58882-163">Standard_D1</span></span>
- <span data-ttu-id="58882-164">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="58882-164">Standard_D2</span></span>
- <span data-ttu-id="58882-165">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="58882-165">Standard_D3</span></span>
- <span data-ttu-id="58882-166">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="58882-166">Standard_D4</span></span>
- <span data-ttu-id="58882-167">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="58882-167">Standard_D11</span></span>
- <span data-ttu-id="58882-168">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="58882-168">Standard_D12</span></span>
- <span data-ttu-id="58882-169">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="58882-169">Standard_D13</span></span>
- <span data-ttu-id="58882-170">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="58882-170">Standard_D14</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58882-171">-標籤</span><span class="sxs-lookup"><span data-stu-id="58882-171">-Label</span></span>
<span data-ttu-id="58882-172">指定要指派給虛擬機器的標籤。</span><span class="sxs-lookup"><span data-stu-id="58882-172">Specifies a label to assign to the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58882-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="58882-173">-LicenseType</span></span>
<span data-ttu-id="58882-174">指定授權內部部署的影像或磁片授權類型。</span><span class="sxs-lookup"><span data-stu-id="58882-174">Specifies the type of license for an image or disk that is licensed on-premises.</span></span>
<span data-ttu-id="58882-175">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="58882-175">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="58882-176">Windows_Client</span><span class="sxs-lookup"><span data-stu-id="58882-176">Windows_Client</span></span>
- <span data-ttu-id="58882-177">Windows_Server</span><span class="sxs-lookup"><span data-stu-id="58882-177">Windows_Server</span></span> 

<span data-ttu-id="58882-178">僅針對包含 Windows Server 作業系統的影像指定此參數。</span><span class="sxs-lookup"><span data-stu-id="58882-178">Specify this parameter only for images that contain the Windows Server operating system.</span></span>

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

### <span data-ttu-id="58882-179">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="58882-179">-MediaLocation</span></span>
<span data-ttu-id="58882-180">指定新虛擬機器磁片的 Azure 儲存位置。</span><span class="sxs-lookup"><span data-stu-id="58882-180">Specifies the Azure storage location for the new virtual machine disk.</span></span>

```yaml
Type: String
Parameter Sets: ImageName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58882-181">-名稱</span><span class="sxs-lookup"><span data-stu-id="58882-181">-Name</span></span>
<span data-ttu-id="58882-182">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="58882-182">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58882-183">-設定檔</span><span class="sxs-lookup"><span data-stu-id="58882-183">-Profile</span></span>
<span data-ttu-id="58882-184">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="58882-184">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="58882-185">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="58882-185">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="58882-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58882-186">CommonParameters</span></span>
<span data-ttu-id="58882-187">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="58882-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58882-188">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="58882-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58882-189">輸入</span><span class="sxs-lookup"><span data-stu-id="58882-189">INPUTS</span></span>

## <span data-ttu-id="58882-190">輸出</span><span class="sxs-lookup"><span data-stu-id="58882-190">OUTPUTS</span></span>

## <span data-ttu-id="58882-191">筆記</span><span class="sxs-lookup"><span data-stu-id="58882-191">NOTES</span></span>

## <span data-ttu-id="58882-192">相關連結</span><span class="sxs-lookup"><span data-stu-id="58882-192">RELATED LINKS</span></span>

