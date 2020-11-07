---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1E1F98E9-FC45-4BEF-90F6-A21D7DB7C82F
online version: ''
schema: 2.0.0
ms.openlocfilehash: eac6db4400e5c51f295e0bbf549117ffdbc97644
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/18/2020
ms.locfileid: "93967891"
---
# <span data-ttu-id="04d42-101">Remove-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="04d42-101">Remove-AzureVMImageOSDiskConfig</span></span>

## <span data-ttu-id="04d42-102">摘要</span><span class="sxs-lookup"><span data-stu-id="04d42-102">SYNOPSIS</span></span>
<span data-ttu-id="04d42-103">從 DiskConfigSet 物件中移除作業系統磁片設定。</span><span class="sxs-lookup"><span data-stu-id="04d42-103">Removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="04d42-104">句法</span><span class="sxs-lookup"><span data-stu-id="04d42-104">SYNTAX</span></span>

```
Remove-AzureVMImageOSDiskConfig [-DiskConfig] <VirtualMachineImageDiskConfigSet>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="04d42-105">說明</span><span class="sxs-lookup"><span data-stu-id="04d42-105">DESCRIPTION</span></span>
<span data-ttu-id="04d42-106">**AzureVMImageOSDiskConfig** Cmdlet 會從 DiskConfigSet 物件中移除作業系統磁片設定。</span><span class="sxs-lookup"><span data-stu-id="04d42-106">The **Remove-AzureVMImageOSDiskConfig** cmdlet removes the operating system disk configuration from the DiskConfigSet object.</span></span>

## <span data-ttu-id="04d42-107">示例</span><span class="sxs-lookup"><span data-stu-id="04d42-107">EXAMPLES</span></span>

### <span data-ttu-id="04d42-108">範例1：從 DiskConfigSet 移除作業系統磁片設定</span><span class="sxs-lookup"><span data-stu-id="04d42-108">Example 1: Remove the operating system disk configuration from a DiskConfigSet</span></span>
```
PS C:\> $Disk = New-AzureDiskConfigSet
PS C:\> $Disk = Set-AzureOSDiskConfig -DiskConfig $Disk -HostCaching ReadWrite
PS C:\> Remove-AzureVMImageOSDiskConfig -DiskConfig $Disk
```

<span data-ttu-id="04d42-109">這個命令會從 DiskConfigSet 物件中移除作業系統磁片設定</span><span class="sxs-lookup"><span data-stu-id="04d42-109">This command removes the operating system disk configuration from the DiskConfigSet object</span></span>

## <span data-ttu-id="04d42-110">參數</span><span class="sxs-lookup"><span data-stu-id="04d42-110">PARAMETERS</span></span>

### <span data-ttu-id="04d42-111">-DiskConfig</span><span class="sxs-lookup"><span data-stu-id="04d42-111">-DiskConfig</span></span>
<span data-ttu-id="04d42-112">指定封裝作業系統磁片和資料磁片物件的磁片設定物件。</span><span class="sxs-lookup"><span data-stu-id="04d42-112">Specifies the disk configuration object that encapsulates the operating system disk and Data Disk objects.</span></span>

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

### <span data-ttu-id="04d42-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="04d42-113">-InformationAction</span></span>
<span data-ttu-id="04d42-114">指定這個 Cmdlet 回應資訊事件的方式。</span><span class="sxs-lookup"><span data-stu-id="04d42-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="04d42-115">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="04d42-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04d42-116">持續</span><span class="sxs-lookup"><span data-stu-id="04d42-116">Continue</span></span>
- <span data-ttu-id="04d42-117">理會</span><span class="sxs-lookup"><span data-stu-id="04d42-117">Ignore</span></span>
- <span data-ttu-id="04d42-118">看</span><span class="sxs-lookup"><span data-stu-id="04d42-118">Inquire</span></span>
- <span data-ttu-id="04d42-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="04d42-119">SilentlyContinue</span></span>
- <span data-ttu-id="04d42-120">停止</span><span class="sxs-lookup"><span data-stu-id="04d42-120">Stop</span></span>
- <span data-ttu-id="04d42-121">封存</span><span class="sxs-lookup"><span data-stu-id="04d42-121">Suspend</span></span>

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

### <span data-ttu-id="04d42-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="04d42-122">-InformationVariable</span></span>
<span data-ttu-id="04d42-123">指定資訊變數。</span><span class="sxs-lookup"><span data-stu-id="04d42-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="04d42-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d42-124">CommonParameters</span></span>
<span data-ttu-id="04d42-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="04d42-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d42-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="04d42-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d42-127">輸入</span><span class="sxs-lookup"><span data-stu-id="04d42-127">INPUTS</span></span>

## <span data-ttu-id="04d42-128">輸出</span><span class="sxs-lookup"><span data-stu-id="04d42-128">OUTPUTS</span></span>

### <span data-ttu-id="04d42-129">WindowsAzure. ServiceManagement. VirtualMachineImageDiskConfigSet</span><span class="sxs-lookup"><span data-stu-id="04d42-129">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.VirtualMachineImageDiskConfigSet</span></span>

## <span data-ttu-id="04d42-130">筆記</span><span class="sxs-lookup"><span data-stu-id="04d42-130">NOTES</span></span>

## <span data-ttu-id="04d42-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="04d42-131">RELATED LINKS</span></span>

[<span data-ttu-id="04d42-132">Set-AzureVMImageOSDiskConfig</span><span class="sxs-lookup"><span data-stu-id="04d42-132">Set-AzureVMImageOSDiskConfig</span></span>](./Set-AzureVMImageOSDiskConfig.md)


