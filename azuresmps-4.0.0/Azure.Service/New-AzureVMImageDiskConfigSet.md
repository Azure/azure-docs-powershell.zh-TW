---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F420A47F-D036-4B31-AA59-97CFC9C79E75
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a53d0821832b29f0f1f6a0b2ab5f1353e3331a3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967644"
---
# <span data-ttu-id="dce1d-101">New-AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="dce1d-101">New-AzureVMImageDiskConfigSet</span></span>

## <span data-ttu-id="dce1d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="dce1d-102">SYNOPSIS</span></span>
<span data-ttu-id="dce1d-103">建立磁片設定集物件。</span><span class="sxs-lookup"><span data-stu-id="dce1d-103">Creates a disk configuration set object.</span></span>

## <span data-ttu-id="dce1d-104">句法</span><span class="sxs-lookup"><span data-stu-id="dce1d-104">SYNTAX</span></span>

```
New-AzureVMImageDiskConfigSet [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="dce1d-105">說明</span><span class="sxs-lookup"><span data-stu-id="dce1d-105">DESCRIPTION</span></span>
<span data-ttu-id="dce1d-106">**新的-AzureVMImageDiskConfigSet** Cmdlet 會建立一個傳送至影像更新 Cmdlet 的磁片設定集物件。</span><span class="sxs-lookup"><span data-stu-id="dce1d-106">The **New-AzureVMImageDiskConfigSet** cmdlet creates a disk configuration set object that is passed to the image update cmdlet.</span></span>
<span data-ttu-id="dce1d-107">它會封裝 OSDiskConfig 和 DataDiskConfig 物件。</span><span class="sxs-lookup"><span data-stu-id="dce1d-107">It encapsulates the OSDiskConfig and the DataDiskConfig object.</span></span>
<span data-ttu-id="dce1d-108">使用 **AzureVMImageOSDiskConfig** 和 **set AzureVMImageDataDiskConfig** Cmdlet 來設定虛擬機器影像的 OS 磁片和資料磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="dce1d-108">Use the **Set-AzureVMImageOSDiskConfig** and **Set-AzureVMImageDataDiskConfig** cmdlets to set the OS Disk and Data Disk properties for the virtual machine image.</span></span>

## <span data-ttu-id="dce1d-109">示例</span><span class="sxs-lookup"><span data-stu-id="dce1d-109">EXAMPLES</span></span>

### <span data-ttu-id="dce1d-110">範例1：建立磁片設定集物件</span><span class="sxs-lookup"><span data-stu-id="dce1d-110">Example 1: Create a disk configuration set object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="dce1d-111">這個命令會建立磁片設定集物件，並將結果儲存在名為 $Disk 的變數中。</span><span class="sxs-lookup"><span data-stu-id="dce1d-111">This command creates a disk configuration set object and stores the results in the variable named $Disk.</span></span>
<span data-ttu-id="dce1d-112">在建立磁片配置之後，就會使用它來設定 OSDiskConfig 和 DataDiskConfig。</span><span class="sxs-lookup"><span data-stu-id="dce1d-112">After the disk configuration is created, it is used to set the OSDiskConfig and DataDiskConfig.</span></span>
<span data-ttu-id="dce1d-113">然後，就會使用設定來更新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="dce1d-113">Then the virtual machine is updated with the configuration.</span></span>

## <span data-ttu-id="dce1d-114">參數</span><span class="sxs-lookup"><span data-stu-id="dce1d-114">PARAMETERS</span></span>

### <span data-ttu-id="dce1d-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="dce1d-115">-InformationAction</span></span>
<span data-ttu-id="dce1d-116">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="dce1d-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dce1d-117">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="dce1d-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dce1d-118">持續</span><span class="sxs-lookup"><span data-stu-id="dce1d-118">Continue</span></span>
- <span data-ttu-id="dce1d-119">理會</span><span class="sxs-lookup"><span data-stu-id="dce1d-119">Ignore</span></span>
- <span data-ttu-id="dce1d-120">看</span><span class="sxs-lookup"><span data-stu-id="dce1d-120">Inquire</span></span>
- <span data-ttu-id="dce1d-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dce1d-121">SilentlyContinue</span></span>
- <span data-ttu-id="dce1d-122">停止</span><span class="sxs-lookup"><span data-stu-id="dce1d-122">Stop</span></span>
- <span data-ttu-id="dce1d-123">封存</span><span class="sxs-lookup"><span data-stu-id="dce1d-123">Suspend</span></span>

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

### <span data-ttu-id="dce1d-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dce1d-124">-InformationVariable</span></span>
<span data-ttu-id="dce1d-125">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="dce1d-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dce1d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce1d-126">CommonParameters</span></span>
<span data-ttu-id="dce1d-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="dce1d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce1d-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="dce1d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce1d-129">輸入</span><span class="sxs-lookup"><span data-stu-id="dce1d-129">INPUTS</span></span>

## <span data-ttu-id="dce1d-130">輸出</span><span class="sxs-lookup"><span data-stu-id="dce1d-130">OUTPUTS</span></span>

### <span data-ttu-id="dce1d-131">WindowsAzure. ServiceManagement. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="dce1d-131">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="dce1d-132">筆記</span><span class="sxs-lookup"><span data-stu-id="dce1d-132">NOTES</span></span>

## <span data-ttu-id="dce1d-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="dce1d-133">RELATED LINKS</span></span>

[<span data-ttu-id="dce1d-134">AzureVMImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="dce1d-134">Get-AzureVMImageDiskConfigSet</span></span>](./Get-AzureVMImageDiskConfigSet.md)

[<span data-ttu-id="dce1d-135">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="dce1d-135">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)

[<span data-ttu-id="dce1d-136">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="dce1d-136">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


