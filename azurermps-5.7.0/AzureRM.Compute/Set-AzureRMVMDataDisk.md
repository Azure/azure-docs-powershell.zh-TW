---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 2f961f144bc322cb1b1b12001ed006bc783ed67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450679"
---
# <span data-ttu-id="0867c-101">Set-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="0867c-101">Set-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="0867c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0867c-102">SYNOPSIS</span></span>
<span data-ttu-id="0867c-103">修改虛擬機器資料磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="0867c-103">Modifies properties of a virtual machine data disk.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0867c-104">句法</span><span class="sxs-lookup"><span data-stu-id="0867c-104">SYNTAX</span></span>

### <span data-ttu-id="0867c-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="0867c-105">ChangeWithName</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="0867c-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="0867c-106">ChangeWithLun</span></span>
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0867c-107">說明</span><span class="sxs-lookup"><span data-stu-id="0867c-107">DESCRIPTION</span></span>
<span data-ttu-id="0867c-108">**AzureRmVMDataDisk** Cmdlet 會修改虛擬機器資料磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="0867c-108">The **Set-AzureRmVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="0867c-109">示例</span><span class="sxs-lookup"><span data-stu-id="0867c-109">EXAMPLES</span></span>

### <span data-ttu-id="0867c-110">範例1：修改資料磁片的快取模式</span><span class="sxs-lookup"><span data-stu-id="0867c-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

<span data-ttu-id="0867c-111">第一個命令會使用 **AzureRmVM** 來取得名為 ContosoVM07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0867c-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzureRmVM**.</span></span>
<span data-ttu-id="0867c-112">該命令會將它儲存在 $VM 變數中。</span><span class="sxs-lookup"><span data-stu-id="0867c-112">The command stores it in the $VM variable.</span></span>

<span data-ttu-id="0867c-113">第二個命令會修改 $VM 虛擬機器上名為 DataDisk01 之資料磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="0867c-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="0867c-114">命令會將結果傳遞給 Update-AzureRmVM Cmdlet，以執行您的變更。</span><span class="sxs-lookup"><span data-stu-id="0867c-114">The command passes the result to the Update-AzureRmVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="0867c-115">對緩衝模式所做的變更會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="0867c-115">A change to the caching mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="0867c-116">參數</span><span class="sxs-lookup"><span data-stu-id="0867c-116">PARAMETERS</span></span>

### <span data-ttu-id="0867c-117">-快取</span><span class="sxs-lookup"><span data-stu-id="0867c-117">-Caching</span></span>
<span data-ttu-id="0867c-118">指定磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="0867c-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="0867c-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0867c-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0867c-120">唯讀</span><span class="sxs-lookup"><span data-stu-id="0867c-120">ReadOnly</span></span>
- <span data-ttu-id="0867c-121">讀</span><span class="sxs-lookup"><span data-stu-id="0867c-121">ReadWrite</span></span>

<span data-ttu-id="0867c-122">預設值為 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="0867c-122">The default value is ReadWrite.</span></span>
<span data-ttu-id="0867c-123">變更此值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="0867c-123">Changing this value causes the virtual machine to restart.</span></span>

<span data-ttu-id="0867c-124">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="0867c-124">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0867c-125">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="0867c-125">-DiskSizeInGB</span></span>
<span data-ttu-id="0867c-126">指定資料磁片的大小（以 gb 為數）。</span><span class="sxs-lookup"><span data-stu-id="0867c-126">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0867c-127">-Lun</span><span class="sxs-lookup"><span data-stu-id="0867c-127">-Lun</span></span>
<span data-ttu-id="0867c-128">指定此 Cmdlet 所修改之資料磁片的邏輯單元號碼 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="0867c-128">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: Int32
Parameter Sets: ChangeWithLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0867c-129">-名稱</span><span class="sxs-lookup"><span data-stu-id="0867c-129">-Name</span></span>
<span data-ttu-id="0867c-130">指定此 Cmdlet 所修改之資料磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="0867c-130">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0867c-131">-VM</span><span class="sxs-lookup"><span data-stu-id="0867c-131">-VM</span></span>
<span data-ttu-id="0867c-132">指定此 Cmdlet 修改資料磁片的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="0867c-132">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="0867c-133">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0867c-133">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="0867c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0867c-134">CommonParameters</span></span>
<span data-ttu-id="0867c-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0867c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0867c-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0867c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0867c-137">輸入</span><span class="sxs-lookup"><span data-stu-id="0867c-137">INPUTS</span></span>

### <span data-ttu-id="0867c-138">所有</span><span class="sxs-lookup"><span data-stu-id="0867c-138">None</span></span>
<span data-ttu-id="0867c-139">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="0867c-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0867c-140">輸出</span><span class="sxs-lookup"><span data-stu-id="0867c-140">OUTPUTS</span></span>

## <span data-ttu-id="0867c-141">筆記</span><span class="sxs-lookup"><span data-stu-id="0867c-141">NOTES</span></span>

## <span data-ttu-id="0867c-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="0867c-142">RELATED LINKS</span></span>

[<span data-ttu-id="0867c-143">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0867c-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0867c-144">更新-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0867c-144">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


