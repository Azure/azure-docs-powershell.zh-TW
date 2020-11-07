---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 849714BC-8B19-453E-B790-A9C38F9D48CB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8ef8bd3b1fef6a3af01193a104f6917c4131064f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966871"
---
# <span data-ttu-id="1d2af-101">Update-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="1d2af-101">Update-AzureDisk</span></span>

## <span data-ttu-id="1d2af-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d2af-102">SYNOPSIS</span></span>
<span data-ttu-id="1d2af-103">變更 Azure 磁片資訊庫中磁片的標籤。</span><span class="sxs-lookup"><span data-stu-id="1d2af-103">Changes the label of a disk in the Azure disk repository.</span></span>

## <span data-ttu-id="1d2af-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d2af-104">SYNTAX</span></span>

### <span data-ttu-id="1d2af-105">大小</span><span class="sxs-lookup"><span data-stu-id="1d2af-105">Resize</span></span>
```
Update-AzureDisk [-DiskName] <String> [[-Label] <String>] [-ResizedSizeInGB] <Int32>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1d2af-106">NoResize</span><span class="sxs-lookup"><span data-stu-id="1d2af-106">NoResize</span></span>
```
Update-AzureDisk [-DiskName] <String> [-Label] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1d2af-107">說明</span><span class="sxs-lookup"><span data-stu-id="1d2af-107">DESCRIPTION</span></span>
<span data-ttu-id="1d2af-108">**AzureDisk** Cmdlet 會變更與目前 Azure 訂閱之磁片資訊庫中之磁片相關聯的標籤。</span><span class="sxs-lookup"><span data-stu-id="1d2af-108">The **Update-AzureDisk** cmdlet changes the label that is associated with a disk in the disk repository of the current Azure subscription.</span></span>

## <span data-ttu-id="1d2af-109">示例</span><span class="sxs-lookup"><span data-stu-id="1d2af-109">EXAMPLES</span></span>

### <span data-ttu-id="1d2af-110">範例1：變更磁片標籤</span><span class="sxs-lookup"><span data-stu-id="1d2af-110">Example 1: Change the label of a disk</span></span>
```
PS C:\> Update-AzureDisk ?DiskName "ContosoOSDisk" -Label "DoNotUse"
```

<span data-ttu-id="1d2af-111">這個命令會將名為 ContosoOSDisk 的磁片標籤改為 [DoNotUse]。</span><span class="sxs-lookup"><span data-stu-id="1d2af-111">This command changes the label of the disk named ContosoOSDisk to DoNotUse.</span></span>

## <span data-ttu-id="1d2af-112">參數</span><span class="sxs-lookup"><span data-stu-id="1d2af-112">PARAMETERS</span></span>

### <span data-ttu-id="1d2af-113">-DiskName</span><span class="sxs-lookup"><span data-stu-id="1d2af-113">-DiskName</span></span>
<span data-ttu-id="1d2af-114">指定此 Cmdlet 所修改之磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d2af-114">Specifies the name of the disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1d2af-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1d2af-115">-InformationAction</span></span>
<span data-ttu-id="1d2af-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="1d2af-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1d2af-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1d2af-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d2af-118">持續</span><span class="sxs-lookup"><span data-stu-id="1d2af-118">Continue</span></span>
- <span data-ttu-id="1d2af-119">理會</span><span class="sxs-lookup"><span data-stu-id="1d2af-119">Ignore</span></span>
- <span data-ttu-id="1d2af-120">看</span><span class="sxs-lookup"><span data-stu-id="1d2af-120">Inquire</span></span>
- <span data-ttu-id="1d2af-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1d2af-121">SilentlyContinue</span></span>
- <span data-ttu-id="1d2af-122">停止</span><span class="sxs-lookup"><span data-stu-id="1d2af-122">Stop</span></span>
- <span data-ttu-id="1d2af-123">封存</span><span class="sxs-lookup"><span data-stu-id="1d2af-123">Suspend</span></span>

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

### <span data-ttu-id="1d2af-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1d2af-124">-InformationVariable</span></span>
<span data-ttu-id="1d2af-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="1d2af-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1d2af-126">-標籤</span><span class="sxs-lookup"><span data-stu-id="1d2af-126">-Label</span></span>
<span data-ttu-id="1d2af-127">指定磁片的新標籤。</span><span class="sxs-lookup"><span data-stu-id="1d2af-127">Specifies the new label for the disk.</span></span>

```yaml
Type: String
Parameter Sets: Resize
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NoResize
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d2af-128">-設定檔</span><span class="sxs-lookup"><span data-stu-id="1d2af-128">-Profile</span></span>
<span data-ttu-id="1d2af-129">指定此 Cmdlet 讀取的 Azure 設定檔。</span><span class="sxs-lookup"><span data-stu-id="1d2af-129">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1d2af-130">如果您沒有指定設定檔，此 Cmdlet 會從本機預設設定檔讀取。</span><span class="sxs-lookup"><span data-stu-id="1d2af-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1d2af-131">-ResizedSizeInGB</span><span class="sxs-lookup"><span data-stu-id="1d2af-131">-ResizedSizeInGB</span></span>
<span data-ttu-id="1d2af-132">指定磁片的新大小（以 gb 為數）。</span><span class="sxs-lookup"><span data-stu-id="1d2af-132">Specifies the new size, in gigabytes, for the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: Resize
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d2af-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d2af-133">CommonParameters</span></span>
<span data-ttu-id="1d2af-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d2af-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d2af-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1d2af-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d2af-136">輸入</span><span class="sxs-lookup"><span data-stu-id="1d2af-136">INPUTS</span></span>

## <span data-ttu-id="1d2af-137">輸出</span><span class="sxs-lookup"><span data-stu-id="1d2af-137">OUTPUTS</span></span>

### <span data-ttu-id="1d2af-138">DiskCoNtext</span><span class="sxs-lookup"><span data-stu-id="1d2af-138">DiskContext</span></span>

## <span data-ttu-id="1d2af-139">筆記</span><span class="sxs-lookup"><span data-stu-id="1d2af-139">NOTES</span></span>

## <span data-ttu-id="1d2af-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d2af-140">RELATED LINKS</span></span>

[<span data-ttu-id="1d2af-141">附加 AzureDisk</span><span class="sxs-lookup"><span data-stu-id="1d2af-141">Add-AzureDisk</span></span>](./Add-AzureDisk.md)

[<span data-ttu-id="1d2af-142">AzureDisk</span><span class="sxs-lookup"><span data-stu-id="1d2af-142">Get-AzureDisk</span></span>](./Get-AzureDisk.md)

[<span data-ttu-id="1d2af-143">移除-AzureDisk</span><span class="sxs-lookup"><span data-stu-id="1d2af-143">Remove-AzureDisk</span></span>](./Remove-AzureDisk.md)


