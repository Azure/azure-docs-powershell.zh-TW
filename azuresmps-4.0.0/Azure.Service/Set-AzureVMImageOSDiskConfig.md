---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9CD39F1C-D858-4275-A6DE-10901DC962FE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cb2557b411d46ce718f97ba7939efb4571ce025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966890"
---
# <span data-ttu-id="ceac6-101">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ceac6-101">Set-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="ceac6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ceac6-102">SYNOPSIS</span></span>
<span data-ttu-id="ceac6-103">在虛擬機器影像上設定作業系統磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="ceac6-103">Sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="ceac6-104">句法</span><span class="sxs-lookup"><span data-stu-id="ceac6-104">SYNTAX</span></span>

### <span data-ttu-id="ceac6-105">UpdateAzureVMImageParamSet (預設) </span><span class="sxs-lookup"><span data-stu-id="ceac6-105">UpdateAzureVMImageParamSet (Default)</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ceac6-106">AddAzureVMImageParamSet</span><span class="sxs-lookup"><span data-stu-id="ceac6-106">AddAzureVMImageParamSet</span></span>
```
Set-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [[-HostCaching] <String>]
 [-MediaLink] <Uri> [-OSState] <String> [-OS] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ceac6-107">說明</span><span class="sxs-lookup"><span data-stu-id="ceac6-107">DESCRIPTION</span></span>
<span data-ttu-id="ceac6-108">**AzureVMImageOSDiskConfig** Cmdlet 會在虛擬機器影像上設定作業系統磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="ceac6-108">The **Set-AzureVMImageOSDiskConfig** cmdlet sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="ceac6-109">示例</span><span class="sxs-lookup"><span data-stu-id="ceac6-109">EXAMPLES</span></span>

### <span data-ttu-id="ceac6-110">範例1：在虛擬機器影像上設定作業系統磁片屬性</span><span class="sxs-lookup"><span data-stu-id="ceac6-110">Example 1: Set the operating system disk properties on a virtual machine image</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -Name "Test" -HostCaching "ReadWrite" -LUN 0
PS C:\> Update-AzureVMImage -ImageName "Image2" -Label "Test1" -Description "Test1" -DiskConfigSet $Disk;
```

<span data-ttu-id="ceac6-111">這個範例會設定虛擬機器影像的作業系統磁片屬性。</span><span class="sxs-lookup"><span data-stu-id="ceac6-111">This example sets the operating system disk properties on a virtual machine image.</span></span>

## <span data-ttu-id="ceac6-112">參數</span><span class="sxs-lookup"><span data-stu-id="ceac6-112">PARAMETERS</span></span>

### <span data-ttu-id="ceac6-113">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="ceac6-113">-DiskConfig</span></span>
<span data-ttu-id="ceac6-114">指定封裝作業系統磁片和資料磁片物件的磁片設定物件。</span><span class="sxs-lookup"><span data-stu-id="ceac6-114">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="ceac6-115">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="ceac6-115">-HostCaching</span></span>
<span data-ttu-id="ceac6-116">指定作業系統磁片的 host cache 屬性。</span><span class="sxs-lookup"><span data-stu-id="ceac6-116">Specifies the host cache attribute for the operating system disk.</span></span>

<span data-ttu-id="ceac6-117">有效值為：</span><span class="sxs-lookup"><span data-stu-id="ceac6-117">Valid values are:</span></span>

<span data-ttu-id="ceac6-118">--ReadOnly--ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ceac6-118">--ReadOnly --ReadWrite</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceac6-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ceac6-119">-InformationAction</span></span>
<span data-ttu-id="ceac6-120">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="ceac6-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ceac6-121">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="ceac6-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ceac6-122">持續</span><span class="sxs-lookup"><span data-stu-id="ceac6-122">Continue</span></span>
- <span data-ttu-id="ceac6-123">理會</span><span class="sxs-lookup"><span data-stu-id="ceac6-123">Ignore</span></span>
- <span data-ttu-id="ceac6-124">看</span><span class="sxs-lookup"><span data-stu-id="ceac6-124">Inquire</span></span>
- <span data-ttu-id="ceac6-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ceac6-125">SilentlyContinue</span></span>
- <span data-ttu-id="ceac6-126">停止</span><span class="sxs-lookup"><span data-stu-id="ceac6-126">Stop</span></span>
- <span data-ttu-id="ceac6-127">封存</span><span class="sxs-lookup"><span data-stu-id="ceac6-127">Suspend</span></span>

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

### <span data-ttu-id="ceac6-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ceac6-128">-InformationVariable</span></span>
<span data-ttu-id="ceac6-129">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="ceac6-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ceac6-130">-MediaLink</span><span class="sxs-lookup"><span data-stu-id="ceac6-130">-MediaLink</span></span>
<span data-ttu-id="ceac6-131">指定新增資料磁片時建立新虛擬硬碟的位置 URI。</span><span class="sxs-lookup"><span data-stu-id="ceac6-131">Specifies the URI of the location where the new virtual hard drive is created when the new data disk is added.</span></span>

```yaml
Type: Uri
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceac6-132">-OS</span><span class="sxs-lookup"><span data-stu-id="ceac6-132">-OS</span></span>
<span data-ttu-id="ceac6-133">指定磁片配置的作業系統。</span><span class="sxs-lookup"><span data-stu-id="ceac6-133">Specifies the operating system of the disk configuration.</span></span>

<span data-ttu-id="ceac6-134">有效值為：</span><span class="sxs-lookup"><span data-stu-id="ceac6-134">Valid values are:</span></span>

- <span data-ttu-id="ceac6-135">時間</span><span class="sxs-lookup"><span data-stu-id="ceac6-135">Windows</span></span>
- <span data-ttu-id="ceac6-136">Linux</span><span class="sxs-lookup"><span data-stu-id="ceac6-136">Linux</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceac6-137">-OSState</span><span class="sxs-lookup"><span data-stu-id="ceac6-137">-OSState</span></span>
<span data-ttu-id="ceac6-138">指定虛擬機器影像的作業系統狀態</span><span class="sxs-lookup"><span data-stu-id="ceac6-138">Specifies the operating system state for virtual machine image</span></span>

<span data-ttu-id="ceac6-139">有效值為：</span><span class="sxs-lookup"><span data-stu-id="ceac6-139">Valid values are:</span></span>

- <span data-ttu-id="ceac6-140">普通</span><span class="sxs-lookup"><span data-stu-id="ceac6-140">Generalized</span></span>
- <span data-ttu-id="ceac6-141">特殊化</span><span class="sxs-lookup"><span data-stu-id="ceac6-141">Specialized</span></span>

<span data-ttu-id="ceac6-142">此參數的使用指示您要將虛擬機器影像捕獲至 Azure 的目的。</span><span class="sxs-lookup"><span data-stu-id="ceac6-142">The use of this parameter indicates your intent to capture the virtual machine image to Azure.</span></span>

```yaml
Type: String
Parameter Sets: AddAzureVMImageParamSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ceac6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceac6-143">CommonParameters</span></span>
<span data-ttu-id="ceac6-144">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ceac6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceac6-145">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ceac6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceac6-146">輸入</span><span class="sxs-lookup"><span data-stu-id="ceac6-146">INPUTS</span></span>

## <span data-ttu-id="ceac6-147">輸出</span><span class="sxs-lookup"><span data-stu-id="ceac6-147">OUTPUTS</span></span>

### <span data-ttu-id="ceac6-148">WindowsAzure. ServiceManagement. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="ceac6-148">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="ceac6-149">筆記</span><span class="sxs-lookup"><span data-stu-id="ceac6-149">NOTES</span></span>

## <span data-ttu-id="ceac6-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="ceac6-150">RELATED LINKS</span></span>

[<span data-ttu-id="ceac6-151">移除-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="ceac6-151">Remove-AzureVMImageOSDiskConfig</span></span>](./Remove-AzureVMImageOSDiskConfig.md)


