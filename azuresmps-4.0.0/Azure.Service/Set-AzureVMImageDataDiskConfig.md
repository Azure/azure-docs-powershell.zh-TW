---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6C7CB0AE-C788-4E6F-AD48-E30B547A2269
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7512ef446227742c2a3564c5f3e5f38f1e2ccce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966882"
---
# <span data-ttu-id="2fcf1-101">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="2fcf1-101">Set-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="2fcf1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2fcf1-102">SYNOPSIS</span></span>
<span data-ttu-id="2fcf1-103">在虛擬機器影像上設定資料磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="2fcf1-103">Sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="2fcf1-104">句法</span><span class="sxs-lookup"><span data-stu-id="2fcf1-104">SYNTAX</span></span>

### <span data-ttu-id="2fcf1-105">UpdateAzureVMImageParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="2fcf1-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-Lun] <Int32> [-HostCaching] <String> [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fcf1-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="2fcf1-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-HostCaching] <String> [-MediaLink] <Uri> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2fcf1-107">說明</span><span class="sxs-lookup"><span data-stu-id="2fcf1-107">DESCRIPTION</span></span>
<span data-ttu-id="2fcf1-108">**AzureVMImageDataDiskConfig** Cmdlet 會在虛擬機器影像上設定資料磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="2fcf1-108">The **Set-AzureVMImageDataDiskConfig** cmdlet sets the Data Disk properties on the virtual machine image.</span></span>

## <span data-ttu-id="2fcf1-109">示例</span><span class="sxs-lookup"><span data-stu-id="2fcf1-109">EXAMPLES</span></span>

### <span data-ttu-id="2fcf1-110">範例1：在虛擬機器影像上設定資料磁片屬性</span><span class="sxs-lookup"><span data-stu-id="2fcf1-110">Example 1: Set Data Disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="2fcf1-111">這個命令會在虛擬機器上設定資料磁片屬性，然後更新虛擬機器影像。</span><span class="sxs-lookup"><span data-stu-id="2fcf1-111">This command sets data disk properties on a virtual machine then updates the virtual machine image.</span></span>

## <span data-ttu-id="2fcf1-112">參數</span><span class="sxs-lookup"><span data-stu-id="2fcf1-112">PARAMETERS</span></span>

### <span data-ttu-id="2fcf1-113">-DataDiskName</span><span class="sxs-lookup"><span data-stu-id="2fcf1-113">-DataDiskName</span></span>
<span data-ttu-id="2fcf1-114">指定此 Cmdlet 所配置的資料磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="2fcf1-114">Specifies the name of the data disk that this cmdlet configures.</span></span>

```yaml
Type: String
Parameter Sets: UpdateAzureVMImageParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcf1-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="2fcf1-115">-DiskConfig</span></span>
<span data-ttu-id="2fcf1-116">指定封裝作業系統磁片和資料磁片物件的磁片設定物件。</span><span class="sxs-lookup"><span data-stu-id="2fcf1-116">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

```yaml
Type: VirtualMachineImageDiskConfigSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcf1-117">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="2fcf1-117">-HostCaching</span></span>
<span data-ttu-id="2fcf1-118">指定作業系統磁片的 host cache 屬性。</span><span class="sxs-lookup"><span data-stu-id="2fcf1-118">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="2fcf1-119">有效值為：</span><span class="sxs-lookup"><span data-stu-id="2fcf1-119">Valid values are:</span></span>

<span data-ttu-id="2fcf1-120">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="2fcf1-120">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcf1-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2fcf1-121">-InformationAction</span></span>
<span data-ttu-id="2fcf1-122">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="2fcf1-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2fcf1-123">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2fcf1-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fcf1-124">持續</span><span class="sxs-lookup"><span data-stu-id="2fcf1-124">Continue</span></span>
- <span data-ttu-id="2fcf1-125">理會</span><span class="sxs-lookup"><span data-stu-id="2fcf1-125">Ignore</span></span>
- <span data-ttu-id="2fcf1-126">看</span><span class="sxs-lookup"><span data-stu-id="2fcf1-126">Inquire</span></span>
- <span data-ttu-id="2fcf1-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2fcf1-127">SilentlyContinue</span></span>
- <span data-ttu-id="2fcf1-128">停止</span><span class="sxs-lookup"><span data-stu-id="2fcf1-128">Stop</span></span>
- <span data-ttu-id="2fcf1-129">封存</span><span class="sxs-lookup"><span data-stu-id="2fcf1-129">Suspend</span></span>

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

### <span data-ttu-id="2fcf1-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2fcf1-130">-InformationVariable</span></span>
<span data-ttu-id="2fcf1-131">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="2fcf1-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2fcf1-132">-Lun</span><span class="sxs-lookup"><span data-stu-id="2fcf1-132">-Lun</span></span>
<span data-ttu-id="2fcf1-133">指定在虛擬機器中掛載資料磁碟機的槽。</span><span class="sxs-lookup"><span data-stu-id="2fcf1-133">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcf1-134">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="2fcf1-134">-MediaLink</span></span>
<span data-ttu-id="2fcf1-135">指定新增資料磁片時建立新虛擬硬碟的位置 URI。</span><span class="sxs-lookup"><span data-stu-id="2fcf1-135">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fcf1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fcf1-136">CommonParameters</span></span>
<span data-ttu-id="2fcf1-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2fcf1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fcf1-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2fcf1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fcf1-139">輸入</span><span class="sxs-lookup"><span data-stu-id="2fcf1-139">INPUTS</span></span>

## <span data-ttu-id="2fcf1-140">輸出</span><span class="sxs-lookup"><span data-stu-id="2fcf1-140">OUTPUTS</span></span>

### <span data-ttu-id="2fcf1-141">WindowsAzure. ServiceManagement. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="2fcf1-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="2fcf1-142">筆記</span><span class="sxs-lookup"><span data-stu-id="2fcf1-142">NOTES</span></span>

## <span data-ttu-id="2fcf1-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="2fcf1-143">RELATED LINKS</span></span>

[<span data-ttu-id="2fcf1-144">移除-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="2fcf1-144">Remove-AzureVMImageDataDiskConfig</span></span>](./Remove-AzureVMImageDataDiskConfig.md)


