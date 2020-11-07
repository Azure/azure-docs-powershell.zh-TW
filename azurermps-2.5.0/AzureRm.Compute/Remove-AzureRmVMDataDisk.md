---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdatadisk
schema: 2.0.0
ms.openlocfilehash: ea8b069be4b153e6e4ca295a917e1c3e81629094
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801406"
---
# <span data-ttu-id="ce668-101">Remove-AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ce668-101">Remove-AzureRmVMDataDisk</span></span>

## <span data-ttu-id="ce668-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ce668-102">SYNOPSIS</span></span>
<span data-ttu-id="ce668-103">從虛擬機器移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="ce668-103">Removes a data disk from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce668-104">句法</span><span class="sxs-lookup"><span data-stu-id="ce668-104">SYNTAX</span></span>

```
Remove-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce668-105">說明</span><span class="sxs-lookup"><span data-stu-id="ce668-105">DESCRIPTION</span></span>
<span data-ttu-id="ce668-106">**AzureRmVMDataDisk** Cmdlet 會從虛擬機器中移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="ce668-106">The **Remove-AzureRmVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="ce668-107">示例</span><span class="sxs-lookup"><span data-stu-id="ce668-107">EXAMPLES</span></span>

### <span data-ttu-id="ce668-108">範例1：從虛擬機器移除資料磁片</span><span class="sxs-lookup"><span data-stu-id="ce668-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzureRmVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="ce668-109">第一個命令會使用 **AzureRmVM** Cmdlet 取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ce668-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="ce668-110">該命令會將虛擬機器儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="ce668-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="ce668-111">第二個命令會從儲存在 $VirtualMachine 的虛擬機器中移除名為 Disk3 的資料磁片。</span><span class="sxs-lookup"><span data-stu-id="ce668-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="ce668-112">Final 命令會更新儲存在 ResourceGroup11 中 $VirtualMachine 的虛擬機器狀態。</span><span class="sxs-lookup"><span data-stu-id="ce668-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="ce668-113">參數</span><span class="sxs-lookup"><span data-stu-id="ce668-113">PARAMETERS</span></span>

### <span data-ttu-id="ce668-114">-DataDiskNames</span><span class="sxs-lookup"><span data-stu-id="ce668-114">-DataDiskNames</span></span>
<span data-ttu-id="ce668-115">指定此 Cmdlet 移除的一或多個資料磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="ce668-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ce668-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce668-116">-DefaultProfile</span></span>
<span data-ttu-id="ce668-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ce668-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce668-118">-VM</span><span class="sxs-lookup"><span data-stu-id="ce668-118">-VM</span></span>
<span data-ttu-id="ce668-119">指定要從中移除資料磁片的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="ce668-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="ce668-120">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce668-120">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="ce668-121">-確認</span><span class="sxs-lookup"><span data-stu-id="ce668-121">-Confirm</span></span>
<span data-ttu-id="ce668-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ce668-122">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="ce668-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce668-123">-WhatIf</span></span>
<span data-ttu-id="ce668-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ce668-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce668-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ce668-125">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="ce668-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce668-126">CommonParameters</span></span>
<span data-ttu-id="ce668-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ce668-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce668-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ce668-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce668-129">輸入</span><span class="sxs-lookup"><span data-stu-id="ce668-129">INPUTS</span></span>

### <span data-ttu-id="ce668-130">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ce668-130">PSVirtualMachine</span></span>
<span data-ttu-id="ce668-131">[VM "參數從管線接受類型 ' PSVirtualMachine」的值</span><span class="sxs-lookup"><span data-stu-id="ce668-131">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="ce668-132">輸出</span><span class="sxs-lookup"><span data-stu-id="ce668-132">OUTPUTS</span></span>

### <span data-ttu-id="ce668-133">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="ce668-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ce668-134">筆記</span><span class="sxs-lookup"><span data-stu-id="ce668-134">NOTES</span></span>

## <span data-ttu-id="ce668-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="ce668-135">RELATED LINKS</span></span>

[<span data-ttu-id="ce668-136">附加 AzureRmVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="ce668-136">Add-AzureRmVMDataDisk</span></span>](./Add-AzureRmVMDataDisk.md)

[<span data-ttu-id="ce668-137">AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ce668-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


