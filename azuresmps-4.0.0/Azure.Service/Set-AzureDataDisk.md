---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967512"
---
# <span data-ttu-id="69e03-101">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="69e03-101">Set-AzureDataDisk</span></span>

## <span data-ttu-id="69e03-102">摘要</span><span class="sxs-lookup"><span data-stu-id="69e03-102">SYNOPSIS</span></span>
<span data-ttu-id="69e03-103">修改 Azure 虛擬機器上現有資料磁片的主機緩存。</span><span class="sxs-lookup"><span data-stu-id="69e03-103">Modifies the host caching of an existing data disk on an Azure virtual machine.</span></span>

## <span data-ttu-id="69e03-104">句法</span><span class="sxs-lookup"><span data-stu-id="69e03-104">SYNTAX</span></span>

### <span data-ttu-id="69e03-105">NoResize</span><span class="sxs-lookup"><span data-stu-id="69e03-105">NoResize</span></span>
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="69e03-106">大小</span><span class="sxs-lookup"><span data-stu-id="69e03-106">Resize</span></span>
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="69e03-107">說明</span><span class="sxs-lookup"><span data-stu-id="69e03-107">DESCRIPTION</span></span>
<span data-ttu-id="69e03-108">**AzureDataDisk** Cmdlet 會修改 Azure 虛擬機器上現有資料磁片的快取屬性。</span><span class="sxs-lookup"><span data-stu-id="69e03-108">The **Set-AzureDataDisk** cmdlet modifies the cache attributes of an existing data disk on an Azure virtual machine.</span></span>
<span data-ttu-id="69e03-109">指定要透過其邏輯單元號碼來更新的資料磁片 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="69e03-109">Specify which data disk to update by its logical unit number (LUN).</span></span>

## <span data-ttu-id="69e03-110">示例</span><span class="sxs-lookup"><span data-stu-id="69e03-110">EXAMPLES</span></span>

### <span data-ttu-id="69e03-111">範例1：修改資料磁片的主機緩存</span><span class="sxs-lookup"><span data-stu-id="69e03-111">Example 1: Modify the host caching for a data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

<span data-ttu-id="69e03-112">這個命令會透過使用 **ContosoService Cmdlet 來** 取得在服務上執行的虛擬機器（名為）。</span><span class="sxs-lookup"><span data-stu-id="69e03-112">This command gets the virtual machines that run on the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="69e03-113">命令會使用管線運算子將它們傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69e03-113">The command passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="69e03-114">該 Cmdlet 會將名為 VirtualMachine07 之虛擬機器的 LUN 2 的資料磁片設定為使用 ReadOnly 主機緩存。</span><span class="sxs-lookup"><span data-stu-id="69e03-114">That cmdlet sets the data disk at LUN 2 of the virtual machine named VirtualMachine07 to use ReadOnly host caching.</span></span>
<span data-ttu-id="69e03-115">此命令會使用 **add-azurevm** Cmdlet 來更新虛擬機器以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="69e03-115">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="69e03-116">範例2：修改虛擬機器上所有資料磁片的主機緩存</span><span class="sxs-lookup"><span data-stu-id="69e03-116">Example 2: Modify the host caching for all data disks on a virtual machine</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

<span data-ttu-id="69e03-117">這個命令會針對 ContosoService 雲端服務上名為 VirtualMachine07 的虛擬機器取得物件。</span><span class="sxs-lookup"><span data-stu-id="69e03-117">This command gets an object for the virtual machine named VirtualMachine07 on the ContosoService cloud service.</span></span>
<span data-ttu-id="69e03-118">命令會將它傳遞給 **AzureDataDisk** Cmdlet，以取得該虛擬機器的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="69e03-118">The command passes it to the **Get-AzureDataDisk** cmdlet, which gets the data disks for that virtual machine.</span></span>
<span data-ttu-id="69e03-119">目前的 Cmdlet 會將每個資料磁片的主機緩存模式設定為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="69e03-119">The current cmdlet then sets the host caching mode of each data disks to ReadWrite.</span></span>
<span data-ttu-id="69e03-120">此命令會更新虛擬機器以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="69e03-120">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="69e03-121">參數</span><span class="sxs-lookup"><span data-stu-id="69e03-121">PARAMETERS</span></span>

### <span data-ttu-id="69e03-122">-DiskName</span><span class="sxs-lookup"><span data-stu-id="69e03-122">-DiskName</span></span>
<span data-ttu-id="69e03-123">指定此 Cmdlet 修改的資料磁片配置名稱。</span><span class="sxs-lookup"><span data-stu-id="69e03-123">Specifies the name of the data disk configuration that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e03-124">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="69e03-124">-HostCaching</span></span>

> [!WARNING]
> <span data-ttu-id="69e03-125">磁片 4 TiB 及更大的磁片不支援磁片快取。</span><span class="sxs-lookup"><span data-stu-id="69e03-125">Disk Caching is not supported for disks 4 TiB and larger.</span></span> <span data-ttu-id="69e03-126">如果有多個磁片連接至您的 VM，每個小於 4 TiB 的磁片都會支援快取。</span><span class="sxs-lookup"><span data-stu-id="69e03-126">If multiple disks are attached to your VM, each disk that is smaller than 4 TiB will support caching.</span></span>
>
> <span data-ttu-id="69e03-127">變更 Azure 磁片的快取設定會分離並重新附加目標磁片。</span><span class="sxs-lookup"><span data-stu-id="69e03-127">Changing the cache setting of an Azure disk detaches and re-attaches the target disk.</span></span> <span data-ttu-id="69e03-128">如果是作業系統磁片，則會重新開機 VM。</span><span class="sxs-lookup"><span data-stu-id="69e03-128">If it is the operating system disk, the VM is restarted.</span></span> <span data-ttu-id="69e03-129">在變更磁片快取設定之前，請停止此中斷可能影響的所有應用程式/服務。</span><span class="sxs-lookup"><span data-stu-id="69e03-129">Stop all applications/services that might be affected by this disruption before changing the disk cache setting.</span></span> <span data-ttu-id="69e03-130">如果不遵循這些建議，可能會導致資料損毀。</span><span class="sxs-lookup"><span data-stu-id="69e03-130">Not following those recommendations could lead to data corruption.</span></span>

<span data-ttu-id="69e03-131">指定磁片的主機層級快取設定。</span><span class="sxs-lookup"><span data-stu-id="69e03-131">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="69e03-132">有效值為：</span><span class="sxs-lookup"><span data-stu-id="69e03-132">Valid values are:</span></span>

- <span data-ttu-id="69e03-133">所有</span><span class="sxs-lookup"><span data-stu-id="69e03-133">None</span></span>
- <span data-ttu-id="69e03-134">唯讀</span><span class="sxs-lookup"><span data-stu-id="69e03-134">ReadOnly</span></span>
- <span data-ttu-id="69e03-135">讀</span><span class="sxs-lookup"><span data-stu-id="69e03-135">ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: NoResize
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e03-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="69e03-136">-InformationAction</span></span>
<span data-ttu-id="69e03-137">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="69e03-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="69e03-138">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="69e03-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="69e03-139">持續</span><span class="sxs-lookup"><span data-stu-id="69e03-139">Continue</span></span>
- <span data-ttu-id="69e03-140">理會</span><span class="sxs-lookup"><span data-stu-id="69e03-140">Ignore</span></span>
- <span data-ttu-id="69e03-141">看</span><span class="sxs-lookup"><span data-stu-id="69e03-141">Inquire</span></span>
- <span data-ttu-id="69e03-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="69e03-142">SilentlyContinue</span></span>
- <span data-ttu-id="69e03-143">停止</span><span class="sxs-lookup"><span data-stu-id="69e03-143">Stop</span></span>
- <span data-ttu-id="69e03-144">封存</span><span class="sxs-lookup"><span data-stu-id="69e03-144">Suspend</span></span>

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

### <span data-ttu-id="69e03-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="69e03-145">-InformationVariable</span></span>
<span data-ttu-id="69e03-146">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="69e03-146">Specifies an information variable.</span></span>

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

### <span data-ttu-id="69e03-147">-LUN</span><span class="sxs-lookup"><span data-stu-id="69e03-147">-LUN</span></span>
<span data-ttu-id="69e03-148">指定虛擬機器中資料磁碟機的 LUN。</span><span class="sxs-lookup"><span data-stu-id="69e03-148">Specifies the LUN for the data drive in the virtual machine.</span></span>
<span data-ttu-id="69e03-149">有效值為：0到15。</span><span class="sxs-lookup"><span data-stu-id="69e03-149">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e03-150">-設定檔</span><span class="sxs-lookup"><span data-stu-id="69e03-150">-Profile</span></span>
<span data-ttu-id="69e03-151">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="69e03-151">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="69e03-152">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="69e03-152">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="69e03-153">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="69e03-153">-ResizedSizeInGB</span></span>
<span data-ttu-id="69e03-154">指定資料磁片的新大小（以 gb 為位元組）。</span><span class="sxs-lookup"><span data-stu-id="69e03-154">Specifies the new size, in gigabytes, for the data disk.</span></span>
<span data-ttu-id="69e03-155">新大小必須大於目前的大小。</span><span class="sxs-lookup"><span data-stu-id="69e03-155">The new size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69e03-156">-VM</span><span class="sxs-lookup"><span data-stu-id="69e03-156">-VM</span></span>
<span data-ttu-id="69e03-157">指定附加至資料磁片的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="69e03-157">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="69e03-158">若要取得虛擬機器物件，請使用 **add-azurevm** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="69e03-158">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69e03-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69e03-159">CommonParameters</span></span>
<span data-ttu-id="69e03-160">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="69e03-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69e03-161">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="69e03-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69e03-162">輸入</span><span class="sxs-lookup"><span data-stu-id="69e03-162">INPUTS</span></span>

## <span data-ttu-id="69e03-163">輸出</span><span class="sxs-lookup"><span data-stu-id="69e03-163">OUTPUTS</span></span>

## <span data-ttu-id="69e03-164">筆記</span><span class="sxs-lookup"><span data-stu-id="69e03-164">NOTES</span></span>

## <span data-ttu-id="69e03-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="69e03-165">RELATED LINKS</span></span>

[<span data-ttu-id="69e03-166">附加 AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="69e03-166">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="69e03-167">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="69e03-167">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="69e03-168">AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="69e03-168">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="69e03-169">移除-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="69e03-169">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="69e03-170">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="69e03-170">Update-AzureVM</span></span>](./Update-AzureVM.md)


