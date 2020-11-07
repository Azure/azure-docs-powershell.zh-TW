---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967612"
---
# <span data-ttu-id="28e6b-101">Remove-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="28e6b-101">Remove-AzureDataDisk</span></span>

## <span data-ttu-id="28e6b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="28e6b-102">SYNOPSIS</span></span>
<span data-ttu-id="28e6b-103">從 Azure 虛擬機器移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="28e6b-103">Removes a data disk from an Azure virtual machine.</span></span>

## <span data-ttu-id="28e6b-104">句法</span><span class="sxs-lookup"><span data-stu-id="28e6b-104">SYNTAX</span></span>

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="28e6b-105">說明</span><span class="sxs-lookup"><span data-stu-id="28e6b-105">DESCRIPTION</span></span>
<span data-ttu-id="28e6b-106">**AzureDataDisk** Cmdlet 會從 Azure 虛擬機器中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="28e6b-106">The **Remove-AzureDataDisk** cmdlet removes a data disk from an Azure virtual machine.</span></span>
<span data-ttu-id="28e6b-107">根據預設，這個 Cmdlet 不會從儲存空間帳戶中移除資料磁片 blob。</span><span class="sxs-lookup"><span data-stu-id="28e6b-107">By default, this cmdlet does not remove the data disk blob from the storage account.</span></span>

## <span data-ttu-id="28e6b-108">示例</span><span class="sxs-lookup"><span data-stu-id="28e6b-108">EXAMPLES</span></span>

### <span data-ttu-id="28e6b-109">範例1：移除資料磁片</span><span class="sxs-lookup"><span data-stu-id="28e6b-109">Example 1: Remove a data disk</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

<span data-ttu-id="28e6b-110">這個命令會透過使用 **VirtualMachine07 Cmdlet，** 在名為 ContosoService 的服務中，取得名為的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="28e6b-110">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="28e6b-111">命令會使用管線運算子，將虛擬機器傳至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28e6b-111">The command passes the virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="28e6b-112">目前的 Cmdlet 會移除擁有 LUN 0 的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="28e6b-112">The current cmdlet removes the data disk that has the LUN 0.</span></span>

### <span data-ttu-id="28e6b-113">範例2：移除資料磁片與虛擬硬碟檔案</span><span class="sxs-lookup"><span data-stu-id="28e6b-113">Example 2: Remove a data disk and the virtual hard disk file</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

<span data-ttu-id="28e6b-114">這個命令會在名為 ContosoService 的服務中取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="28e6b-114">This command gets the virtual machine named VirtualMachine07 in the service named ContosoService.</span></span>
<span data-ttu-id="28e6b-115">該命令會將虛擬機器傳遞至目前的 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28e6b-115">The command passes the virtual machine to the current cmdlet.</span></span>
<span data-ttu-id="28e6b-116">目前的 Cmdlet 會移除擁有 LUN 0 的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="28e6b-116">The current cmdlet removes the data disk that has the LUN 0.</span></span>
<span data-ttu-id="28e6b-117">此命令包括 *DeleteVHD* 參數。</span><span class="sxs-lookup"><span data-stu-id="28e6b-117">The command includes the *DeleteVHD* parameter.</span></span>
<span data-ttu-id="28e6b-118">因此，它也會刪除基礎虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="28e6b-118">Therefore, it also deletes the underlying virtual hard disk.</span></span>
<span data-ttu-id="28e6b-119">此命令會使用 **add-azurevm** Cmdlet 來更新虛擬機器以反映您所做的變更。</span><span class="sxs-lookup"><span data-stu-id="28e6b-119">The command updates the virtual machine to reflect your changes by using the **Update-AzureVM** cmdlet.</span></span>

## <span data-ttu-id="28e6b-120">參數</span><span class="sxs-lookup"><span data-stu-id="28e6b-120">PARAMETERS</span></span>

### <span data-ttu-id="28e6b-121">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="28e6b-121">-DeleteVHD</span></span>
<span data-ttu-id="28e6b-122">表示此 Cmdlet 會從 blob 儲存體中移除資料磁片與虛擬硬碟 (VHD) 。</span><span class="sxs-lookup"><span data-stu-id="28e6b-122">Indicates that this cmdlet removes the data disk and the virtual hard disk (VHD) from blob storage.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e6b-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="28e6b-123">-InformationAction</span></span>
<span data-ttu-id="28e6b-124">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="28e6b-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="28e6b-125">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="28e6b-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="28e6b-126">持續</span><span class="sxs-lookup"><span data-stu-id="28e6b-126">Continue</span></span>
- <span data-ttu-id="28e6b-127">理會</span><span class="sxs-lookup"><span data-stu-id="28e6b-127">Ignore</span></span>
- <span data-ttu-id="28e6b-128">看</span><span class="sxs-lookup"><span data-stu-id="28e6b-128">Inquire</span></span>
- <span data-ttu-id="28e6b-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="28e6b-129">SilentlyContinue</span></span>
- <span data-ttu-id="28e6b-130">停止</span><span class="sxs-lookup"><span data-stu-id="28e6b-130">Stop</span></span>
- <span data-ttu-id="28e6b-131">封存</span><span class="sxs-lookup"><span data-stu-id="28e6b-131">Suspend</span></span>

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

### <span data-ttu-id="28e6b-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="28e6b-132">-InformationVariable</span></span>
<span data-ttu-id="28e6b-133">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="28e6b-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="28e6b-134">-LUN</span><span class="sxs-lookup"><span data-stu-id="28e6b-134">-LUN</span></span>
<span data-ttu-id="28e6b-135">指定虛擬機器中資料磁碟機的邏輯單元號碼 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="28e6b-135">Specifies the logical unit number (LUN) for the data drive in the virtual machine.</span></span>
<span data-ttu-id="28e6b-136">有效值為：0到15。</span><span class="sxs-lookup"><span data-stu-id="28e6b-136">Valid values are: 0 through 15.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28e6b-137">-設定檔</span><span class="sxs-lookup"><span data-stu-id="28e6b-137">-Profile</span></span>
<span data-ttu-id="28e6b-138">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="28e6b-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="28e6b-139">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="28e6b-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="28e6b-140">-VM</span><span class="sxs-lookup"><span data-stu-id="28e6b-140">-VM</span></span>
<span data-ttu-id="28e6b-141">指定附加至資料磁片的虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="28e6b-141">Specifies the virtual machine object that is attached to the data disk.</span></span>
<span data-ttu-id="28e6b-142">若要取得虛擬機器物件，請使用 **add-azurevm** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="28e6b-142">To obtain a virtual machine object, use the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="28e6b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28e6b-143">CommonParameters</span></span>
<span data-ttu-id="28e6b-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="28e6b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28e6b-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="28e6b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28e6b-146">輸入</span><span class="sxs-lookup"><span data-stu-id="28e6b-146">INPUTS</span></span>

## <span data-ttu-id="28e6b-147">輸出</span><span class="sxs-lookup"><span data-stu-id="28e6b-147">OUTPUTS</span></span>

## <span data-ttu-id="28e6b-148">筆記</span><span class="sxs-lookup"><span data-stu-id="28e6b-148">NOTES</span></span>

## <span data-ttu-id="28e6b-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="28e6b-149">RELATED LINKS</span></span>

[<span data-ttu-id="28e6b-150">附加 AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="28e6b-150">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="28e6b-151">AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="28e6b-151">Get-AzureDataDisk</span></span>](./Get-AzureDataDisk.md)

[<span data-ttu-id="28e6b-152">Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="28e6b-152">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="28e6b-153">Set-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="28e6b-153">Set-AzureDataDisk</span></span>](./Set-AzureDataDisk.md)

[<span data-ttu-id="28e6b-154">更新-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="28e6b-154">Update-AzureVM</span></span>](./Update-AzureVM.md)


