---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967181"
---
# <span data-ttu-id="40779-101">Add-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="40779-101">Add-AzureDataDisk</span></span>

## <span data-ttu-id="40779-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40779-102">SYNOPSIS</span></span>
<span data-ttu-id="40779-103">將資料磁片新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="40779-103">Adds a data disk to a virtual machine.</span></span>

## <span data-ttu-id="40779-104">句法</span><span class="sxs-lookup"><span data-stu-id="40779-104">SYNTAX</span></span>

### <span data-ttu-id="40779-105">CreateNew (預設) </span><span class="sxs-lookup"><span data-stu-id="40779-105">CreateNew (Default)</span></span>
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="40779-106">Import</span><span class="sxs-lookup"><span data-stu-id="40779-106">Import</span></span>
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="40779-107">ImportFrom</span><span class="sxs-lookup"><span data-stu-id="40779-107">ImportFrom</span></span>
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="40779-108">說明</span><span class="sxs-lookup"><span data-stu-id="40779-108">DESCRIPTION</span></span>
<span data-ttu-id="40779-109">**載入 AzureDataDisk** Cmdlet 會將新的或現有的資料磁片新增至 Azure 虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="40779-109">The **Add-AzureDataDisk** cmdlet adds a new or existing data disk to an Azure virtual machine object.</span></span>
<span data-ttu-id="40779-110">使用 *CreateNew* 參數來建立具有指定大小和標籤的新資料磁片。</span><span class="sxs-lookup"><span data-stu-id="40779-110">Use the *CreateNew* parameter to create a new data disk that has a specified size and label.</span></span>
<span data-ttu-id="40779-111">使用匯 *入* 參數，從影像存放庫附加現有的磁片。</span><span class="sxs-lookup"><span data-stu-id="40779-111">Use the *Import* parameter to attach an existing disk from the image repository.</span></span>
<span data-ttu-id="40779-112">使用 *ImportFrom* 參數，在儲存空間帳戶的 blob 中附加現有的磁片。</span><span class="sxs-lookup"><span data-stu-id="40779-112">Use the *ImportFrom* parameter to attach an existing disk from a blob in a storage account.</span></span>
<span data-ttu-id="40779-113">您可以指定附加資料磁片的主機緩存模式。</span><span class="sxs-lookup"><span data-stu-id="40779-113">You can specify the host-cache mode of the attached data disk.</span></span>

## <span data-ttu-id="40779-114">示例</span><span class="sxs-lookup"><span data-stu-id="40779-114">EXAMPLES</span></span>

### <span data-ttu-id="40779-115">範例1：從知識庫中匯入資料磁片</span><span class="sxs-lookup"><span data-stu-id="40779-115">Example 1: Import a data disk from the repository</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="40779-116">這個命令會使用 **VirtualMachine07 Cmdlet，** 在 ContosoService 雲端服務中取得名為的虛擬機器的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="40779-116">This command gets a virtual machine object for the virtual machine named VirtualMachine07 in the ContosoService cloud service by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="40779-117">命令會使用管線運算子將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40779-117">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="40779-118">該命令會將現有的資料磁片從儲存庫附加到虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="40779-118">That command attaches an existing data disk from the repository to the virtual machine.</span></span>
<span data-ttu-id="40779-119">資料磁片的 LUN 為0。</span><span class="sxs-lookup"><span data-stu-id="40779-119">The data disk has a LUN of 0.</span></span>
<span data-ttu-id="40779-120">此命令會使用 **add-azurevm** Cmdlet 來更新虛擬機器以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="40779-120">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

### <span data-ttu-id="40779-121">範例2：新增資料磁片</span><span class="sxs-lookup"><span data-stu-id="40779-121">Example 2: Add a new data disk</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="40779-122">這個命令會取得名為 VirtualMachine08 的虛擬機器的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="40779-122">This command gets a virtual machine object for the virtual machine named VirtualMachine08.</span></span>
<span data-ttu-id="40779-123">命令會將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40779-123">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="40779-124">該命令會附加一個名為 MyNewDisk 的新資料磁片。</span><span class="sxs-lookup"><span data-stu-id="40779-124">That command attaches a new data disk named MyNewDisk.vhd.</span></span>
<span data-ttu-id="40779-125">這個 Cmdlet 會在目前訂閱的預設儲存空間帳戶中，在 vhd 容器中建立磁片。</span><span class="sxs-lookup"><span data-stu-id="40779-125">The cmdlet creates the disk in the vhds container in the default storage account of the current subscription.</span></span>
<span data-ttu-id="40779-126">此命令會更新虛擬機器以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="40779-126">The command updates the virtual machine to reflect your changes.</span></span>

### <span data-ttu-id="40779-127">範例3：從指定的位置新增資料磁片</span><span class="sxs-lookup"><span data-stu-id="40779-127">Example 3: Add a data disk from a specified location</span></span>
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

<span data-ttu-id="40779-128">這個命令會取得名為 Database 的虛擬機器的虛擬電腦物件。</span><span class="sxs-lookup"><span data-stu-id="40779-128">This command gets a virtual machine object for the virtual machine named Database.</span></span>
<span data-ttu-id="40779-129">命令會將它傳遞到目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40779-129">The command passes it to the current cmdlet.</span></span>
<span data-ttu-id="40779-130">該命令會從指定的位置附加名為 Disk14 的現有資料磁片。</span><span class="sxs-lookup"><span data-stu-id="40779-130">That command attaches an existing data disk named Disk14.vhd from the specified location.</span></span>
<span data-ttu-id="40779-131">此命令會更新虛擬機器以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="40779-131">The command updates the virtual machine to reflect your changes.</span></span>

## <span data-ttu-id="40779-132">參數</span><span class="sxs-lookup"><span data-stu-id="40779-132">PARAMETERS</span></span>

### <span data-ttu-id="40779-133">-CreateNew</span><span class="sxs-lookup"><span data-stu-id="40779-133">-CreateNew</span></span>
<span data-ttu-id="40779-134">表示此 Cmdlet 會建立資料磁片。</span><span class="sxs-lookup"><span data-stu-id="40779-134">Indicates that this cmdlet creates a data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40779-135">-DiskLabel</span><span class="sxs-lookup"><span data-stu-id="40779-135">-DiskLabel</span></span>
<span data-ttu-id="40779-136">指定新資料磁片的磁片標籤。</span><span class="sxs-lookup"><span data-stu-id="40779-136">Specifies the disk label for a new data disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40779-137">-DiskName</span><span class="sxs-lookup"><span data-stu-id="40779-137">-DiskName</span></span>
<span data-ttu-id="40779-138">指定磁片存放庫中資料磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="40779-138">Specifies the name of a data disk in the disk repository.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40779-139">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="40779-139">-DiskSizeInGB</span></span>
<span data-ttu-id="40779-140">為新的資料磁片指定邏輯磁片大小（以千百萬位元組計）。</span><span class="sxs-lookup"><span data-stu-id="40779-140">Specifies the logical disk size, in gigabytes, for a new data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40779-141">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="40779-141">-HostCaching</span></span>
<span data-ttu-id="40779-142">指定磁片的主機層級快取設定。</span><span class="sxs-lookup"><span data-stu-id="40779-142">Specifies the host level caching settings of the disk.</span></span>
<span data-ttu-id="40779-143">有效值為：</span><span class="sxs-lookup"><span data-stu-id="40779-143">Valid values are:</span></span> 

- <span data-ttu-id="40779-144">所有</span><span class="sxs-lookup"><span data-stu-id="40779-144">None</span></span> 
- <span data-ttu-id="40779-145">唯讀</span><span class="sxs-lookup"><span data-stu-id="40779-145">ReadOnly</span></span> 
- <span data-ttu-id="40779-146">讀</span><span class="sxs-lookup"><span data-stu-id="40779-146">ReadWrite</span></span>

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

### <span data-ttu-id="40779-147">匯入</span><span class="sxs-lookup"><span data-stu-id="40779-147">-Import</span></span>
<span data-ttu-id="40779-148">表示此 Cmdlet 會從影像存放庫中匯入現有的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="40779-148">Indicates that this cmdlet imports an existing data disk from the image repository.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40779-149">-ImportFrom</span><span class="sxs-lookup"><span data-stu-id="40779-149">-ImportFrom</span></span>
<span data-ttu-id="40779-150">表示此 Cmdlet 會從儲存空間帳戶的 blob 中匯入現有的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="40779-150">Indicates that this cmdlet imports an existing data disk from a blob in a storage account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40779-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="40779-151">-InformationAction</span></span>
<span data-ttu-id="40779-152">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="40779-152">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="40779-153">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="40779-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="40779-154">持續</span><span class="sxs-lookup"><span data-stu-id="40779-154">Continue</span></span>
- <span data-ttu-id="40779-155">理會</span><span class="sxs-lookup"><span data-stu-id="40779-155">Ignore</span></span>
- <span data-ttu-id="40779-156">看</span><span class="sxs-lookup"><span data-stu-id="40779-156">Inquire</span></span>
- <span data-ttu-id="40779-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="40779-157">SilentlyContinue</span></span>
- <span data-ttu-id="40779-158">停止</span><span class="sxs-lookup"><span data-stu-id="40779-158">Stop</span></span>
- <span data-ttu-id="40779-159">封存</span><span class="sxs-lookup"><span data-stu-id="40779-159">Suspend</span></span>

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

### <span data-ttu-id="40779-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="40779-160">-InformationVariable</span></span>
<span data-ttu-id="40779-161">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="40779-161">Specifies an information variable.</span></span>

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

### <span data-ttu-id="40779-162">-LUN</span><span class="sxs-lookup"><span data-stu-id="40779-162">-LUN</span></span>
<span data-ttu-id="40779-163">指定虛擬機器中資料磁碟機的邏輯單元號碼 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="40779-163">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="40779-164">有效值為：0到15。</span><span class="sxs-lookup"><span data-stu-id="40779-164">Valid values are: 0 through 15.</span></span>
<span data-ttu-id="40779-165">每個資料磁片都必須有唯一的 LUN。</span><span class="sxs-lookup"><span data-stu-id="40779-165">Each data disk must have a unique LUN.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40779-166">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="40779-166">-MediaLocation</span></span>
<span data-ttu-id="40779-167">指定此 Cmdlet 儲存資料磁片的 Azure 儲存空間帳戶中的 blob 位置。</span><span class="sxs-lookup"><span data-stu-id="40779-167">Specifies the location of the blob in an Azure storage account where this cmdlet stores the data disk.</span></span>
<span data-ttu-id="40779-168">如果您沒有指定位置，此 Cmdlet 會將資料磁片儲存在目前訂閱預設儲存空間帳戶的 vhd 容器中。</span><span class="sxs-lookup"><span data-stu-id="40779-168">If you do not specify a location, the cmdlet stores the data disk in the vhds container in the default storage account for the current subscription.</span></span>
<span data-ttu-id="40779-169">如果 vhd 容器不存在，則 Cmdlet 會建立 vhd 容器。</span><span class="sxs-lookup"><span data-stu-id="40779-169">If a vhds container does not exist, the cmdlet creates a vhds container.</span></span>

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40779-170">-設定檔</span><span class="sxs-lookup"><span data-stu-id="40779-170">-Profile</span></span>
<span data-ttu-id="40779-171">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="40779-171">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="40779-172">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="40779-172">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="40779-173">-VM</span><span class="sxs-lookup"><span data-stu-id="40779-173">-VM</span></span>
<span data-ttu-id="40779-174">指定此 Cmdlet 附加資料磁片的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="40779-174">Specifies the virtual machine object to which this cmdlet attaches a data disk.</span></span>
<span data-ttu-id="40779-175">若要取得虛擬機器物件，請使用 **add-azurevm** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40779-175">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="40779-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40779-176">CommonParameters</span></span>
<span data-ttu-id="40779-177">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40779-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40779-178">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40779-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40779-179">輸入</span><span class="sxs-lookup"><span data-stu-id="40779-179">INPUTS</span></span>

## <span data-ttu-id="40779-180">輸出</span><span class="sxs-lookup"><span data-stu-id="40779-180">OUTPUTS</span></span>

## <span data-ttu-id="40779-181">筆記</span><span class="sxs-lookup"><span data-stu-id="40779-181">NOTES</span></span>

## <span data-ttu-id="40779-182">相關連結</span><span class="sxs-lookup"><span data-stu-id="40779-182">RELATED LINKS</span></span>

[<span data-ttu-id="40779-183">AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="40779-183">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="40779-184">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="40779-184">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="40779-185">移除-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="40779-185">Remove-AzureDataDisk</span></span>](./Remove-AzureDataDisk.md)

[<span data-ttu-id="40779-186">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="40779-186">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="40779-187">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="40779-187">Update-AzureVM</span></span>](./Update-AzureVM.md)


