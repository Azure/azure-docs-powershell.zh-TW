---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 16A34F31-1C61-4911-8C1F-9F82683524A1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 775d2deff8a83e758d48fb9328bf4156b142d20c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967839"
---
# <span data-ttu-id="d1609-101">Add-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="d1609-101">Add-AzureDisk</span></span>

## <span data-ttu-id="d1609-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d1609-102">SYNOPSIS</span></span>
<span data-ttu-id="d1609-103">新增磁片至 Azure 磁片庫。</span><span class="sxs-lookup"><span data-stu-id="d1609-103">Adds a disk to the Azure disk repository.</span></span>

## <span data-ttu-id="d1609-104">句法</span><span class="sxs-lookup"><span data-stu-id="d1609-104">SYNTAX</span></span>

```
Add-AzureDisk [-DiskName] <String> [-MediaLocation] <String> [-Label <String>] [-OS <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1609-105">說明</span><span class="sxs-lookup"><span data-stu-id="d1609-105">DESCRIPTION</span></span>
<span data-ttu-id="d1609-106">**AzureDisk** Cmdlet 會在目前訂閱的 Azure 磁片資訊庫中新增磁片。</span><span class="sxs-lookup"><span data-stu-id="d1609-106">The **Add-AzureDisk** cmdlet adds a disk to the Azure disk repository in the current subscription.</span></span>
<span data-ttu-id="d1609-107">這個 Cmdlet 可以新增系統磁片或資料磁片。</span><span class="sxs-lookup"><span data-stu-id="d1609-107">This cmdlet can add a system disk or a data disk.</span></span>
<span data-ttu-id="d1609-108">若要新增系統磁片，請使用 *OS* 參數指定作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="d1609-108">To add a system disk, specify an operating system type by using the *OS* parameter.</span></span>

## <span data-ttu-id="d1609-109">示例</span><span class="sxs-lookup"><span data-stu-id="d1609-109">EXAMPLES</span></span>

### <span data-ttu-id="d1609-110">範例1：新增使用 Windows 作業系統的啟動磁片</span><span class="sxs-lookup"><span data-stu-id="d1609-110">Example 1: Add a startup disk that uses the Windows operating system</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyWinDisk" -MediaLocation "http://contosostorage.blob.core.azure.com/vhds/winserver-system.vhd" -Label "StartupDisk" -OS "Windows"
```

<span data-ttu-id="d1609-111">這個命令會將系統磁片新增到您的磁片存放庫。</span><span class="sxs-lookup"><span data-stu-id="d1609-111">This command adds a system disk to your disk repository.</span></span>
<span data-ttu-id="d1609-112">系統磁片使用 Windows 作業系統。</span><span class="sxs-lookup"><span data-stu-id="d1609-112">The system disk uses the Windows operating system.</span></span>

### <span data-ttu-id="d1609-113">範例2：新增資料磁片</span><span class="sxs-lookup"><span data-stu-id="d1609-113">Example 2: Add a data disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyDataDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/winserver-data.vhd" -Label "DataDisk"
```

<span data-ttu-id="d1609-114">這個命令會新增資料磁片。</span><span class="sxs-lookup"><span data-stu-id="d1609-114">This command adds a data disk.</span></span>

### <span data-ttu-id="d1609-115">範例3：新增 Linux 系統磁片</span><span class="sxs-lookup"><span data-stu-id="d1609-115">Example 3: Add a Linux system disk</span></span>
```
PS C:\> Add-AzureDisk -DiskName "MyLinuxDisk" -MediaLocation "http://yourstorageaccount.blob.core.azure.com/vhds/linuxsys.vhd" -OS "Linux"
```

<span data-ttu-id="d1609-116">這個命令會新增 Linux 系統磁片。</span><span class="sxs-lookup"><span data-stu-id="d1609-116">This command adds a Linux system disk.</span></span>

## <span data-ttu-id="d1609-117">參數</span><span class="sxs-lookup"><span data-stu-id="d1609-117">PARAMETERS</span></span>

### <span data-ttu-id="d1609-118">-DiskName</span><span class="sxs-lookup"><span data-stu-id="d1609-118">-DiskName</span></span>
<span data-ttu-id="d1609-119">指定此 Cmdlet 新增的磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="d1609-119">Specifies the name of the disk that this cmdlet adds.</span></span>

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

### <span data-ttu-id="d1609-120">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="d1609-120">-InformationAction</span></span>
<span data-ttu-id="d1609-121">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="d1609-121">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="d1609-122">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="d1609-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d1609-123">持續</span><span class="sxs-lookup"><span data-stu-id="d1609-123">Continue</span></span>
- <span data-ttu-id="d1609-124">理會</span><span class="sxs-lookup"><span data-stu-id="d1609-124">Ignore</span></span>
- <span data-ttu-id="d1609-125">看</span><span class="sxs-lookup"><span data-stu-id="d1609-125">Inquire</span></span>
- <span data-ttu-id="d1609-126">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="d1609-126">SilentlyContinue</span></span>
- <span data-ttu-id="d1609-127">停止</span><span class="sxs-lookup"><span data-stu-id="d1609-127">Stop</span></span>
- <span data-ttu-id="d1609-128">封存</span><span class="sxs-lookup"><span data-stu-id="d1609-128">Suspend</span></span>

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

### <span data-ttu-id="d1609-129">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="d1609-129">-InformationVariable</span></span>
<span data-ttu-id="d1609-130">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="d1609-130">Specifies an information variable.</span></span>

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

### <span data-ttu-id="d1609-131">-標籤</span><span class="sxs-lookup"><span data-stu-id="d1609-131">-Label</span></span>
<span data-ttu-id="d1609-132">指定此 Cmdlet 所新增之磁片的磁片標籤。</span><span class="sxs-lookup"><span data-stu-id="d1609-132">Specifies a disk label for the disk that this cmdlet adds.</span></span>

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

### <span data-ttu-id="d1609-133">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="d1609-133">-MediaLocation</span></span>
<span data-ttu-id="d1609-134">指定 Azure 儲存空間中磁片的物理位置。</span><span class="sxs-lookup"><span data-stu-id="d1609-134">Specifies the physical location of the disk in Azure Storage.</span></span>
<span data-ttu-id="d1609-135">此值會參照目前訂閱和儲存空間帳戶中的 blob 頁面。</span><span class="sxs-lookup"><span data-stu-id="d1609-135">This value refers to a blob page in the current subscription and storage account.</span></span>

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

### <span data-ttu-id="d1609-136">-OS</span><span class="sxs-lookup"><span data-stu-id="d1609-136">-OS</span></span>
<span data-ttu-id="d1609-137">指定系統磁片的作業系統類型。</span><span class="sxs-lookup"><span data-stu-id="d1609-137">Specifies the operating system type for a system disk.</span></span>
<span data-ttu-id="d1609-138">有效值為：</span><span class="sxs-lookup"><span data-stu-id="d1609-138">Valid values are:</span></span> 

- <span data-ttu-id="d1609-139">時間</span><span class="sxs-lookup"><span data-stu-id="d1609-139">Windows</span></span> 
- <span data-ttu-id="d1609-140">Linux</span><span class="sxs-lookup"><span data-stu-id="d1609-140">Linux</span></span> 

<span data-ttu-id="d1609-141">如果您沒有指定此參數，Cmdlet 會將磁片新增為數據磁片。</span><span class="sxs-lookup"><span data-stu-id="d1609-141">If you do not specify this parameter, the cmdlet adds the disk as a data disk.</span></span>

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

### <span data-ttu-id="d1609-142">-設定檔</span><span class="sxs-lookup"><span data-stu-id="d1609-142">-Profile</span></span>
<span data-ttu-id="d1609-143">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="d1609-143">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d1609-144">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="d1609-144">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d1609-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1609-145">CommonParameters</span></span>
<span data-ttu-id="d1609-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d1609-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1609-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d1609-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1609-148">輸入</span><span class="sxs-lookup"><span data-stu-id="d1609-148">INPUTS</span></span>

## <span data-ttu-id="d1609-149">輸出</span><span class="sxs-lookup"><span data-stu-id="d1609-149">OUTPUTS</span></span>

### <span data-ttu-id="d1609-150">DiskCoNtext</span><span class="sxs-lookup"><span data-stu-id="d1609-150">DiskContext</span></span>

## <span data-ttu-id="d1609-151">筆記</span><span class="sxs-lookup"><span data-stu-id="d1609-151">NOTES</span></span>

## <span data-ttu-id="d1609-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="d1609-152">RELATED LINKS</span></span>

[<span data-ttu-id="d1609-153">AzureDisk</span><span class="sxs-lookup"><span data-stu-id="d1609-153">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="d1609-154">移除-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="d1609-154">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="d1609-155">更新-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="d1609-155">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


