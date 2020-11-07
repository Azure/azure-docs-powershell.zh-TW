---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 75A50C59-28D1-4D29-A420-D24BF479F79E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 29e5e7e0bc2fcc0ce93186cf966f18d6c9c3e372
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967603"
---
# <span data-ttu-id="8fabb-101">Remove-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="8fabb-101">Remove-AzureDisk</span></span>

## <span data-ttu-id="8fabb-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8fabb-102">SYNOPSIS</span></span>
<span data-ttu-id="8fabb-103">從 Azure 磁片資訊庫移除磁片。</span><span class="sxs-lookup"><span data-stu-id="8fabb-103">Removes a disk from the Azure disk repository.</span></span>

## <span data-ttu-id="8fabb-104">句法</span><span class="sxs-lookup"><span data-stu-id="8fabb-104">SYNTAX</span></span>

```
Remove-AzureDisk [-DiskName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="8fabb-105">說明</span><span class="sxs-lookup"><span data-stu-id="8fabb-105">DESCRIPTION</span></span>
<span data-ttu-id="8fabb-106">**AzureDisk** Cmdlet 會從目前訂閱的 Azure 磁片資訊庫中移除磁片。</span><span class="sxs-lookup"><span data-stu-id="8fabb-106">The **Remove-AzureDisk** cmdlet removes a disk from the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="8fabb-107">根據預設，這個 Cmdlet 不會從 blob 儲存體中刪除虛擬硬碟 (VHD) 檔案。</span><span class="sxs-lookup"><span data-stu-id="8fabb-107">By default, this cmdlet does not delete the virtual hard disk (VHD) file from blob storage.</span></span>
<span data-ttu-id="8fabb-108">若要刪除 VHD，請指定 *DeleteVHD* 參數。</span><span class="sxs-lookup"><span data-stu-id="8fabb-108">To delete the VHD, specify the *DeleteVHD* parameter.</span></span>

## <span data-ttu-id="8fabb-109">示例</span><span class="sxs-lookup"><span data-stu-id="8fabb-109">EXAMPLES</span></span>

### <span data-ttu-id="8fabb-110">範例1：移除磁片</span><span class="sxs-lookup"><span data-stu-id="8fabb-110">Example 1: Remove a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="8fabb-111">這個命令會從磁片存放庫中移除名為 ContosoDataDisk 磁片的磁片。</span><span class="sxs-lookup"><span data-stu-id="8fabb-111">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="8fabb-112">該命令不會刪除 VHD。</span><span class="sxs-lookup"><span data-stu-id="8fabb-112">The command does not delete the VHD.</span></span>

### <span data-ttu-id="8fabb-113">範例2：移除並刪除磁片</span><span class="sxs-lookup"><span data-stu-id="8fabb-113">Example 2: Remove and delete a disk</span></span>
```
PS C:\> Remove-AzureDisk -DiskName "ContosoDataDisk" -DeleteVHD
```

<span data-ttu-id="8fabb-114">這個命令會從磁片存放庫中移除名為 ContosoDataDisk 磁片的磁片。</span><span class="sxs-lookup"><span data-stu-id="8fabb-114">This command removes the disk named ContosoDataDisk disk from the disk repository.</span></span>
<span data-ttu-id="8fabb-115">這個命令會指定 DeleteVHD 參數。</span><span class="sxs-lookup"><span data-stu-id="8fabb-115">This command specifies the DeleteVHD parameter.</span></span>
<span data-ttu-id="8fabb-116">因此，命令會從 Azure 儲存空間中刪除 VHD。</span><span class="sxs-lookup"><span data-stu-id="8fabb-116">Therefore, the command deletes the VHD from Azure Storage.</span></span>

## <span data-ttu-id="8fabb-117">參數</span><span class="sxs-lookup"><span data-stu-id="8fabb-117">PARAMETERS</span></span>

### <span data-ttu-id="8fabb-118">-DeleteVHD</span><span class="sxs-lookup"><span data-stu-id="8fabb-118">-DeleteVHD</span></span>
<span data-ttu-id="8fabb-119">表示此 Cmdlet 會從 blob 儲存體中移除 VHD。</span><span class="sxs-lookup"><span data-stu-id="8fabb-119">Indicates that this cmdlet removes the VHD from blob storage.</span></span>

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

### <span data-ttu-id="8fabb-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="8fabb-120">-DiskName</span></span>
<span data-ttu-id="8fabb-121">指定此 Cmdlet 移除之磁片儲備庫中的資料磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="8fabb-121">Specifies the name of the data disk in the disk repository that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8fabb-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="8fabb-122">-InformationAction</span></span>
<span data-ttu-id="8fabb-123">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="8fabb-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="8fabb-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="8fabb-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8fabb-125">持續</span><span class="sxs-lookup"><span data-stu-id="8fabb-125">Continue</span></span>
- <span data-ttu-id="8fabb-126">理會</span><span class="sxs-lookup"><span data-stu-id="8fabb-126">Ignore</span></span>
- <span data-ttu-id="8fabb-127">看</span><span class="sxs-lookup"><span data-stu-id="8fabb-127">Inquire</span></span>
- <span data-ttu-id="8fabb-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="8fabb-128">SilentlyContinue</span></span>
- <span data-ttu-id="8fabb-129">停止</span><span class="sxs-lookup"><span data-stu-id="8fabb-129">Stop</span></span>
- <span data-ttu-id="8fabb-130">封存</span><span class="sxs-lookup"><span data-stu-id="8fabb-130">Suspend</span></span>

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

### <span data-ttu-id="8fabb-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="8fabb-131">-InformationVariable</span></span>
<span data-ttu-id="8fabb-132">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="8fabb-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="8fabb-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="8fabb-133">-Profile</span></span>
<span data-ttu-id="8fabb-134">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="8fabb-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8fabb-135">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="8fabb-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8fabb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fabb-136">CommonParameters</span></span>
<span data-ttu-id="8fabb-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8fabb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fabb-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8fabb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fabb-139">輸入</span><span class="sxs-lookup"><span data-stu-id="8fabb-139">INPUTS</span></span>

## <span data-ttu-id="8fabb-140">輸出</span><span class="sxs-lookup"><span data-stu-id="8fabb-140">OUTPUTS</span></span>

## <span data-ttu-id="8fabb-141">筆記</span><span class="sxs-lookup"><span data-stu-id="8fabb-141">NOTES</span></span>

## <span data-ttu-id="8fabb-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="8fabb-142">RELATED LINKS</span></span>

[<span data-ttu-id="8fabb-143">附加 AzureDisk</span><span class="sxs-lookup"><span data-stu-id="8fabb-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="8fabb-144">AzureDisk</span><span class="sxs-lookup"><span data-stu-id="8fabb-144">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="8fabb-145">更新-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="8fabb-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


