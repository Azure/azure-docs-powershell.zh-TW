---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 02DB15F5-5CE0-4FF0-8863-AF1B2BA5E775
online version: ''
schema: 2.0.0
ms.openlocfilehash: 41f72ace02132ba4184af08e995404b47f76d0b0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967274"
---
# <span data-ttu-id="95e7b-101">Set-AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="95e7b-101">Set-AzureOSDisk</span></span>

## <span data-ttu-id="95e7b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="95e7b-102">SYNOPSIS</span></span>
<span data-ttu-id="95e7b-103">修改 Azure 虛擬機器的主機緩存模式。</span><span class="sxs-lookup"><span data-stu-id="95e7b-103">Modifies the host cache mode of an Azure virtual machine.</span></span>

## <span data-ttu-id="95e7b-104">句法</span><span class="sxs-lookup"><span data-stu-id="95e7b-104">SYNTAX</span></span>

### <span data-ttu-id="95e7b-105">NoResize</span><span class="sxs-lookup"><span data-stu-id="95e7b-105">NoResize</span></span>
```
Set-AzureOSDisk [-HostCaching] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="95e7b-106">大小</span><span class="sxs-lookup"><span data-stu-id="95e7b-106">Resize</span></span>
```
Set-AzureOSDisk [[-HostCaching] <String>] [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="95e7b-107">說明</span><span class="sxs-lookup"><span data-stu-id="95e7b-107">DESCRIPTION</span></span>
<span data-ttu-id="95e7b-108">**AzureOSDisk** Cmdlet 會修改 Azure 虛擬機器之作業系統磁片的主機緩存模式。</span><span class="sxs-lookup"><span data-stu-id="95e7b-108">The **Set-AzureOSDisk** cmdlet modifies the host cache mode of the operating system disk of an Azure virtual machine.</span></span>
<span data-ttu-id="95e7b-109">支援的 host cache 模式為 ReadOnly 和 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="95e7b-109">The supported host cache modes are ReadOnly and ReadWrite.</span></span>
<span data-ttu-id="95e7b-110">如果您在執行中的虛擬機器上執行這個 Cmdlet，該虛擬機器就會重新開機。</span><span class="sxs-lookup"><span data-stu-id="95e7b-110">If you run this cmdlet on a virtual machine that is running, that virtual machine restarts.</span></span>

## <span data-ttu-id="95e7b-111">示例</span><span class="sxs-lookup"><span data-stu-id="95e7b-111">EXAMPLES</span></span>

### <span data-ttu-id="95e7b-112">範例1：使用管線將主機快取模式設定為 ReadOnly</span><span class="sxs-lookup"><span data-stu-id="95e7b-112">Example 1: Set the host cache mode to ReadOnly by using the pipeline</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02" | Set-AzureOSDisk -HostCaching "ReadOnly"
```

<span data-ttu-id="95e7b-113">這個命令會透過使用 **VirtualMachine02 Cmdlet，** 在名為 ContosoService 的服務中，取得名為的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95e7b-113">This command gets the virtual machine named VirtualMachine02 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="95e7b-114">命令會使用管線運算子，將虛擬機器傳至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95e7b-114">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="95e7b-115">目前的 Cmdlet 會將該虛擬機器的作業系統磁片的主機快取模式設定為 ReadOnly。</span><span class="sxs-lookup"><span data-stu-id="95e7b-115">The current cmdlet sets the host cache mode of the operating system disk of that virtual machine to be ReadOnly.</span></span>

### <span data-ttu-id="95e7b-116">範例2：將主機快取模式設定為 ReadWrite</span><span class="sxs-lookup"><span data-stu-id="95e7b-116">Example 2: Set the host cache mode to ReadWrite</span></span>
```
PS C:\> $VM = Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine02"
PS C:\> Set-AzureOSDisk "ReadWrite" -VM $myVM2
```

<span data-ttu-id="95e7b-117">第一個命令會在名為 ContosoService 的服務中取得名為 VirtualMachine02 的虛擬機器，然後將它儲存在變數中。</span><span class="sxs-lookup"><span data-stu-id="95e7b-117">The first command gets the virtual machine named VirtualMachine02 in the service named ContosoService, and then stores it in the variable.</span></span>

<span data-ttu-id="95e7b-118">第二個命令會將該虛擬機器之作業系統磁片的主機快取模式設定為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="95e7b-118">The second command sets the host cache mode of the operating system disk of that virtual machine to be ReadWrite.</span></span>

## <span data-ttu-id="95e7b-119">參數</span><span class="sxs-lookup"><span data-stu-id="95e7b-119">PARAMETERS</span></span>

### <span data-ttu-id="95e7b-120">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="95e7b-120">-HostCaching</span></span>
<span data-ttu-id="95e7b-121">指定作業系統磁片的 host cache 屬性。</span><span class="sxs-lookup"><span data-stu-id="95e7b-121">Specifies the host cache attribute for the operating system disk.</span></span>
<span data-ttu-id="95e7b-122">有效值為：</span><span class="sxs-lookup"><span data-stu-id="95e7b-122">Valid values are:</span></span> 

- <span data-ttu-id="95e7b-123">唯讀</span><span class="sxs-lookup"><span data-stu-id="95e7b-123">ReadOnly</span></span> 
- <span data-ttu-id="95e7b-124">讀</span><span class="sxs-lookup"><span data-stu-id="95e7b-124">ReadWrite</span></span>

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

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e7b-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="95e7b-125">-InformationAction</span></span>
<span data-ttu-id="95e7b-126">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="95e7b-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="95e7b-127">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="95e7b-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="95e7b-128">持續</span><span class="sxs-lookup"><span data-stu-id="95e7b-128">Continue</span></span>
- <span data-ttu-id="95e7b-129">理會</span><span class="sxs-lookup"><span data-stu-id="95e7b-129">Ignore</span></span>
- <span data-ttu-id="95e7b-130">看</span><span class="sxs-lookup"><span data-stu-id="95e7b-130">Inquire</span></span>
- <span data-ttu-id="95e7b-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="95e7b-131">SilentlyContinue</span></span>
- <span data-ttu-id="95e7b-132">停止</span><span class="sxs-lookup"><span data-stu-id="95e7b-132">Stop</span></span>
- <span data-ttu-id="95e7b-133">封存</span><span class="sxs-lookup"><span data-stu-id="95e7b-133">Suspend</span></span>

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

### <span data-ttu-id="95e7b-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="95e7b-134">-InformationVariable</span></span>
<span data-ttu-id="95e7b-135">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="95e7b-135">Specifies an information variable.</span></span>

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

### <span data-ttu-id="95e7b-136">-設定檔</span><span class="sxs-lookup"><span data-stu-id="95e7b-136">-Profile</span></span>
<span data-ttu-id="95e7b-137">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="95e7b-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="95e7b-138">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="95e7b-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="95e7b-139">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="95e7b-139">-ResizedSizeInGB</span></span>
<span data-ttu-id="95e7b-140">指定作業系統磁片的新大小（以 gb 為位元組）。</span><span class="sxs-lookup"><span data-stu-id="95e7b-140">Specifies a new size, in gigabytes, for the operating system disk.</span></span>
<span data-ttu-id="95e7b-141">大小必須大於目前的大小。</span><span class="sxs-lookup"><span data-stu-id="95e7b-141">The size must be larger than the current size.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95e7b-142">-VM</span><span class="sxs-lookup"><span data-stu-id="95e7b-142">-VM</span></span>
<span data-ttu-id="95e7b-143">指定此 Cmdlet 修改作業系統磁片的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="95e7b-143">Specifies the virtual machine for which this cmdlet modifies the operating system disk.</span></span>
<span data-ttu-id="95e7b-144">若要取得虛擬機器物件，請使用 **add-azurevm** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="95e7b-144">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="95e7b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95e7b-145">CommonParameters</span></span>
<span data-ttu-id="95e7b-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="95e7b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95e7b-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="95e7b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95e7b-148">輸入</span><span class="sxs-lookup"><span data-stu-id="95e7b-148">INPUTS</span></span>

## <span data-ttu-id="95e7b-149">輸出</span><span class="sxs-lookup"><span data-stu-id="95e7b-149">OUTPUTS</span></span>

## <span data-ttu-id="95e7b-150">筆記</span><span class="sxs-lookup"><span data-stu-id="95e7b-150">NOTES</span></span>

## <span data-ttu-id="95e7b-151">相關連結</span><span class="sxs-lookup"><span data-stu-id="95e7b-151">RELATED LINKS</span></span>

[<span data-ttu-id="95e7b-152">附加 AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="95e7b-152">Add-AzureVMImage</span></span>](./Add-AzureVMImage.md)

[<span data-ttu-id="95e7b-153">AzureOSDisk</span><span class="sxs-lookup"><span data-stu-id="95e7b-153">Get-AzureOSDisk</span></span>](./Get-AzureOSDisk.md)

[<span data-ttu-id="95e7b-154">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="95e7b-154">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="95e7b-155">AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="95e7b-155">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="95e7b-156">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="95e7b-156">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="95e7b-157">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="95e7b-157">Update-AzureVM</span></span>](./Update-AzureVM.md)


