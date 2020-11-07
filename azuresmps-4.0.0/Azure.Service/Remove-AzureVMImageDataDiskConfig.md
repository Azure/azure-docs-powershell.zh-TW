---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5CAF2D29-F4AE-4322-AA4F-61267723B955
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2e19ad4b56e5141458f1fe9305a0c33691d024d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93966943"
---
# <span data-ttu-id="b5f89-101">Remove-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b5f89-101">Remove-AzureVMImageDataDiskConfig</span></span>

## <span data-ttu-id="b5f89-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b5f89-102">SYNOPSIS</span></span>
<span data-ttu-id="b5f89-103">從 DiskConfigSet 物件中移除資料磁片設定。</span><span class="sxs-lookup"><span data-stu-id="b5f89-103">Removes the data disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="b5f89-104">句法</span><span class="sxs-lookup"><span data-stu-id="b5f89-104">SYNTAX</span></span>

### <span data-ttu-id="b5f89-105">RemoveByDiskName (預設) </span><span class="sxs-lookup"><span data-stu-id="b5f89-105">RemoveByDiskName (Default)</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-DataDiskName] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b5f89-106">RemoveByDiskLun</span><span class="sxs-lookup"><span data-stu-id="b5f89-106">RemoveByDiskLun</span></span>
```
Remove-AzureVMImageDataDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet> [-Lun] <Int32>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b5f89-107">說明</span><span class="sxs-lookup"><span data-stu-id="b5f89-107">DESCRIPTION</span></span>
<span data-ttu-id="b5f89-108">**AzureVMImageDataDiskConfig** Cmdlet 會從 **DiskConfigSet** 物件中移除資料磁片設定。</span><span class="sxs-lookup"><span data-stu-id="b5f89-108">The **Remove-AzureVMImageDataDiskConfig** cmdlet removes the data disk configuration from the **DiskConfigSet** object.</span></span>

## <span data-ttu-id="b5f89-109">示例</span><span class="sxs-lookup"><span data-stu-id="b5f89-109">EXAMPLES</span></span>

### <span data-ttu-id="b5f89-110">範例1：從 DiskConfigSet 物件中移除資料磁片設定</span><span class="sxs-lookup"><span data-stu-id="b5f89-110">Example 1: Remove the data disk configuration from the DiskConfigSet object</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureDataDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageDataDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="b5f89-111">這個範例會建立 **DiskConfigSet** ，加以設定，然後移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="b5f89-111">This example creates a **DiskConfigSet** , configures it, then removes the data disk.</span></span>

## <span data-ttu-id="b5f89-112">參數</span><span class="sxs-lookup"><span data-stu-id="b5f89-112">PARAMETERS</span></span>

### <span data-ttu-id="b5f89-113">-DataDiskName</span><span class="sxs-lookup"><span data-stu-id="b5f89-113">-DataDiskName</span></span>
<span data-ttu-id="b5f89-114">指定此 Cmdlet 移除的資料磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="b5f89-114">Specifies the name of the data disk that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDiskName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f89-115">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="b5f89-115">-DiskConfig</span></span>
<span data-ttu-id="b5f89-116">指定封裝作業系統磁片和資料磁片物件的磁片設定物件。</span><span class="sxs-lookup"><span data-stu-id="b5f89-116">Specifies the disk configuration object that encapsulates the operating system disk and data disk objects.</span></span>

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

### <span data-ttu-id="b5f89-117">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b5f89-117">-InformationAction</span></span>
<span data-ttu-id="b5f89-118">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="b5f89-118">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b5f89-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b5f89-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b5f89-120">持續</span><span class="sxs-lookup"><span data-stu-id="b5f89-120">Continue</span></span>
- <span data-ttu-id="b5f89-121">理會</span><span class="sxs-lookup"><span data-stu-id="b5f89-121">Ignore</span></span>
- <span data-ttu-id="b5f89-122">看</span><span class="sxs-lookup"><span data-stu-id="b5f89-122">Inquire</span></span>
- <span data-ttu-id="b5f89-123">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b5f89-123">SilentlyContinue</span></span>
- <span data-ttu-id="b5f89-124">停止</span><span class="sxs-lookup"><span data-stu-id="b5f89-124">Stop</span></span>
- <span data-ttu-id="b5f89-125">封存</span><span class="sxs-lookup"><span data-stu-id="b5f89-125">Suspend</span></span>

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

### <span data-ttu-id="b5f89-126">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b5f89-126">-InformationVariable</span></span>
<span data-ttu-id="b5f89-127">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="b5f89-127">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b5f89-128">-Lun</span><span class="sxs-lookup"><span data-stu-id="b5f89-128">-Lun</span></span>
<span data-ttu-id="b5f89-129">指定在虛擬機器中掛載資料磁碟機的槽。</span><span class="sxs-lookup"><span data-stu-id="b5f89-129">Specifies the slot where the data drive is mounted in the virtual machine.</span></span>

```yaml
Type: Int32
Parameter Sets: RemoveByDiskLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5f89-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5f89-130">CommonParameters</span></span>
<span data-ttu-id="b5f89-131">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b5f89-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5f89-132">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b5f89-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5f89-133">輸入</span><span class="sxs-lookup"><span data-stu-id="b5f89-133">INPUTS</span></span>

## <span data-ttu-id="b5f89-134">輸出</span><span class="sxs-lookup"><span data-stu-id="b5f89-134">OUTPUTS</span></span>

### <span data-ttu-id="b5f89-135">WindowsAzure. ServiceManagement. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="b5f89-135">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="b5f89-136">筆記</span><span class="sxs-lookup"><span data-stu-id="b5f89-136">NOTES</span></span>

## <span data-ttu-id="b5f89-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="b5f89-137">RELATED LINKS</span></span>

[<span data-ttu-id="b5f89-138">Set-AzureVMImageDataDiskConfig</span><span class="sxs-lookup"><span data-stu-id="b5f89-138">Set-AzureVMImageDataDiskConfig</span></span>](./Set-AzureVMImageDataDiskConfig.md)


