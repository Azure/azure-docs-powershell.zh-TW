---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMDataDisk.md
ms.openlocfilehash: 3c1edb8302ac0921a8f396230637b842d88eab77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623990"
---
# <span data-ttu-id="ca5cf-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ca5cf-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="ca5cf-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca5cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ca5cf-103">從虛擬機器移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca5cf-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca5cf-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca5cf-105">說明</span><span class="sxs-lookup"><span data-stu-id="ca5cf-105">DESCRIPTION</span></span>
<span data-ttu-id="ca5cf-106">**AzureRmVMDataDisk** Cmdlet 會從虛擬機器中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="ca5cf-107">示例</span><span class="sxs-lookup"><span data-stu-id="ca5cf-107">EXAMPLES</span></span>

### <span data-ttu-id="ca5cf-108">範例1：從虛擬機器移除資料磁片</span><span class="sxs-lookup"><span data-stu-id="ca5cf-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="ca5cf-109">第一個命令會使用 **AzureRmVM** Cmdlet 取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="ca5cf-110">該命令會將虛擬機器儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="ca5cf-111">第二個命令會從儲存在 $VirtualMachine 的虛擬機器中移除名為 Disk3 的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="ca5cf-112">Final 命令會更新儲存在 ResourceGroup11 中 $VirtualMachine 的虛擬機器狀態。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="ca5cf-113">參數</span><span class="sxs-lookup"><span data-stu-id="ca5cf-113">PARAMETERS</span></span>

### <span data-ttu-id="ca5cf-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="ca5cf-114">-DataDiskNames</span></span>
<span data-ttu-id="ca5cf-115">指定此 Cmdlet 移除的一或多個資料磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca5cf-116">-VM</span><span class="sxs-lookup"><span data-stu-id="ca5cf-116">-VM</span></span>
<span data-ttu-id="ca5cf-117">指定要從中移除資料磁片的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-117">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="ca5cf-118">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-118">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca5cf-119">-確認</span><span class="sxs-lookup"><span data-stu-id="ca5cf-119">-Confirm</span></span>
<span data-ttu-id="ca5cf-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-120">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca5cf-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca5cf-121">-WhatIf</span></span>
<span data-ttu-id="ca5cf-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca5cf-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-123">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca5cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca5cf-124">CommonParameters</span></span>
<span data-ttu-id="ca5cf-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca5cf-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca5cf-127">輸入</span><span class="sxs-lookup"><span data-stu-id="ca5cf-127">INPUTS</span></span>

### <span data-ttu-id="ca5cf-128">所有</span><span class="sxs-lookup"><span data-stu-id="ca5cf-128">None</span></span>
<span data-ttu-id="ca5cf-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="ca5cf-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ca5cf-130">輸出</span><span class="sxs-lookup"><span data-stu-id="ca5cf-130">OUTPUTS</span></span>

## <span data-ttu-id="ca5cf-131">筆記</span><span class="sxs-lookup"><span data-stu-id="ca5cf-131">NOTES</span></span>

## <span data-ttu-id="ca5cf-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca5cf-132">RELATED LINKS</span></span>

[<span data-ttu-id="ca5cf-133">附加 AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ca5cf-133">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="ca5cf-134">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ca5cf-134">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


