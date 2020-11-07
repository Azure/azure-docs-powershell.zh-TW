---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967800"
---
# <span data-ttu-id="3d3ca-101">Get-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="3d3ca-101">Get-AzureDisk</span></span>

## <span data-ttu-id="3d3ca-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3d3ca-102">SYNOPSIS</span></span>
<span data-ttu-id="3d3ca-103">取得有關 Azure 磁片資訊庫中磁片的資訊。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-103">Gets information about disks in the Azure disk repository.</span></span>

## <span data-ttu-id="3d3ca-104">句法</span><span class="sxs-lookup"><span data-stu-id="3d3ca-104">SYNTAX</span></span>

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3d3ca-105">說明</span><span class="sxs-lookup"><span data-stu-id="3d3ca-105">DESCRIPTION</span></span>
<span data-ttu-id="3d3ca-106">**AzureDisk** Cmdlet 會取得儲存在目前訂閱之 Azure 磁片資訊庫中之磁片的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-106">The **Get-AzureDisk** cmdlet gets information about the disks that are stored in the Azure disk repository for the current subscription.</span></span>
<span data-ttu-id="3d3ca-107">這個 Cmdlet 會傳回儲備庫中所有磁片的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-107">This cmdlet returns a list of information for all disks in the repository.</span></span>
<span data-ttu-id="3d3ca-108">若要查看特定磁片的資訊，請指定磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-108">To view information for a specific disk, specify the name of the disk.</span></span>

## <span data-ttu-id="3d3ca-109">示例</span><span class="sxs-lookup"><span data-stu-id="3d3ca-109">EXAMPLES</span></span>

### <span data-ttu-id="3d3ca-110">範例1：取得磁片相關資訊</span><span class="sxs-lookup"><span data-stu-id="3d3ca-110">Example 1: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

<span data-ttu-id="3d3ca-111">這個命令會從磁片資訊庫取得名為 ContosoDataDisk 磁片的資訊資料。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-111">This command gets information data about the disk named ContosoDataDisk from the disk repository.</span></span>

### <span data-ttu-id="3d3ca-112">範例2：取得所有磁片的相關資訊</span><span class="sxs-lookup"><span data-stu-id="3d3ca-112">Example 2: Get information about all disks</span></span>
```
PS C:\> Get-AzureDisk
```

<span data-ttu-id="3d3ca-113">這個命令會取得磁片資訊庫中所有磁片的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-113">This command gets information about all the disks in the disk repository.</span></span>

### <span data-ttu-id="3d3ca-114">範例3：取得磁片相關資訊</span><span class="sxs-lookup"><span data-stu-id="3d3ca-114">Example 3: Get information about a disk</span></span>
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

<span data-ttu-id="3d3ca-115">這個命令會取得磁片資訊庫中目前未連接至虛擬機器之所有磁片的資料。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-115">This command gets data for all of the disks in the disk repository that are not currently attached to a virtual machine.</span></span>
<span data-ttu-id="3d3ca-116">此命令會取得所有磁片的相關資訊，並將每個物件傳遞到 **物件** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-116">The command gets information about all of the disks, and passes each object to the **Where-Object** cmdlet.</span></span>
<span data-ttu-id="3d3ca-117">該 Cmdlet 會刪除 **AttachedTo** 屬性的值不是 $Null 的任何磁片。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-117">That cmdlet drops any disk that does not have a value of $Null for the **AttachedTo** property.</span></span>
<span data-ttu-id="3d3ca-118">命令會使用 [ **Format-table** Cmdlet]，將清單格式化為表格。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-118">The command formats the list as a table by using the **Format-Table** cmdlet.</span></span>

## <span data-ttu-id="3d3ca-119">參數</span><span class="sxs-lookup"><span data-stu-id="3d3ca-119">PARAMETERS</span></span>

### <span data-ttu-id="3d3ca-120">-DiskName</span><span class="sxs-lookup"><span data-stu-id="3d3ca-120">-DiskName</span></span>
<span data-ttu-id="3d3ca-121">指定此 Cmdlet 取得資訊之磁片資訊庫中的磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-121">Specifies the name of the disk in the disk repository about which this cmdlet gets information.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d3ca-122">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3d3ca-122">-InformationAction</span></span>
<span data-ttu-id="3d3ca-123">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-123">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3d3ca-124">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="3d3ca-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3d3ca-125">持續</span><span class="sxs-lookup"><span data-stu-id="3d3ca-125">Continue</span></span>
- <span data-ttu-id="3d3ca-126">理會</span><span class="sxs-lookup"><span data-stu-id="3d3ca-126">Ignore</span></span>
- <span data-ttu-id="3d3ca-127">看</span><span class="sxs-lookup"><span data-stu-id="3d3ca-127">Inquire</span></span>
- <span data-ttu-id="3d3ca-128">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3d3ca-128">SilentlyContinue</span></span>
- <span data-ttu-id="3d3ca-129">停止</span><span class="sxs-lookup"><span data-stu-id="3d3ca-129">Stop</span></span>
- <span data-ttu-id="3d3ca-130">封存</span><span class="sxs-lookup"><span data-stu-id="3d3ca-130">Suspend</span></span>

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

### <span data-ttu-id="3d3ca-131">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3d3ca-131">-InformationVariable</span></span>
<span data-ttu-id="3d3ca-132">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-132">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3d3ca-133">-設定檔</span><span class="sxs-lookup"><span data-stu-id="3d3ca-133">-Profile</span></span>
<span data-ttu-id="3d3ca-134">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3d3ca-135">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3d3ca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d3ca-136">CommonParameters</span></span>
<span data-ttu-id="3d3ca-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d3ca-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3d3ca-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d3ca-139">輸入</span><span class="sxs-lookup"><span data-stu-id="3d3ca-139">INPUTS</span></span>

## <span data-ttu-id="3d3ca-140">輸出</span><span class="sxs-lookup"><span data-stu-id="3d3ca-140">OUTPUTS</span></span>

## <span data-ttu-id="3d3ca-141">筆記</span><span class="sxs-lookup"><span data-stu-id="3d3ca-141">NOTES</span></span>

## <span data-ttu-id="3d3ca-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="3d3ca-142">RELATED LINKS</span></span>

[<span data-ttu-id="3d3ca-143">附加 AzureDisk</span><span class="sxs-lookup"><span data-stu-id="3d3ca-143">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="3d3ca-144">移除-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="3d3ca-144">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)

[<span data-ttu-id="3d3ca-145">更新-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="3d3ca-145">Update-AzureDisk</span></span>](./Update-AzureDisk.md)


