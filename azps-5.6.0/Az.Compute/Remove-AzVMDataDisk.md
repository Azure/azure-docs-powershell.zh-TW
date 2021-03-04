---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5943E9F-E4E6-4A1F-A144-44691CF32FC8
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDataDisk.md
ms.openlocfilehash: 72ccf9994b303e9e191594f32bb2aa23f0abd9ad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909745"
---
# <span data-ttu-id="49919-101">Remove-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="49919-101">Remove-AzVMDataDisk</span></span>

## <span data-ttu-id="49919-102">簡介</span><span class="sxs-lookup"><span data-stu-id="49919-102">SYNOPSIS</span></span>
<span data-ttu-id="49919-103">從虛擬機器移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="49919-103">Removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="49919-104">語法</span><span class="sxs-lookup"><span data-stu-id="49919-104">SYNTAX</span></span>

```
Remove-AzVMDataDisk [-VM] <PSVirtualMachine> [[-DataDiskNames] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49919-105">描述</span><span class="sxs-lookup"><span data-stu-id="49919-105">DESCRIPTION</span></span>
<span data-ttu-id="49919-106">**Remove-AzCMDataDataData Cmdlet** 會從虛擬機器移除資料磁片。</span><span class="sxs-lookup"><span data-stu-id="49919-106">The **Remove-AzVMDataDisk** cmdlet removes a data disk from a virtual machine.</span></span>

## <span data-ttu-id="49919-107">例子</span><span class="sxs-lookup"><span data-stu-id="49919-107">EXAMPLES</span></span>

### <span data-ttu-id="49919-108">範例 1：從虛擬機器移除資料磁片</span><span class="sxs-lookup"><span data-stu-id="49919-108">Example 1: Remove a data disk from a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" 
PS C:\> Remove-AzVMDataDisk -VM $VirtualMachine -Name "Disk3"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

<span data-ttu-id="49919-109">第一個命令會使用 **Get-Az VIRTUAL** Cmdlet 取得名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="49919-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="49919-110">該命令將虛擬機器儲存在 $VirtualMachine 變數中。</span><span class="sxs-lookup"><span data-stu-id="49919-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="49919-111">第二個命令會從儲存在本機的虛擬機器移除名為 Disk3 的資料$VirtualMachine。</span><span class="sxs-lookup"><span data-stu-id="49919-111">The second command removes the data disk named Disk3 from the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="49919-112">最後一個命令會更新儲存在 ResourceGroup11 $VirtualMachine的狀態。</span><span class="sxs-lookup"><span data-stu-id="49919-112">The final command updates the state of the virtual machine stored in $VirtualMachine in ResourceGroup11.</span></span>

## <span data-ttu-id="49919-113">參數</span><span class="sxs-lookup"><span data-stu-id="49919-113">PARAMETERS</span></span>

### <span data-ttu-id="49919-114">-DataNames</span><span class="sxs-lookup"><span data-stu-id="49919-114">-DataDiskNames</span></span>
<span data-ttu-id="49919-115">指定此 Cmdlet 移除的一或多個資料磁片名稱。</span><span class="sxs-lookup"><span data-stu-id="49919-115">Specifies the names of one or more data disks that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49919-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49919-116">-DefaultProfile</span></span>
<span data-ttu-id="49919-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="49919-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49919-118">-VM</span><span class="sxs-lookup"><span data-stu-id="49919-118">-VM</span></span>
<span data-ttu-id="49919-119">指定要從移除資料磁片的本機虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="49919-119">Specifies the local virtual machine object from which to remove a data disk.</span></span>
<span data-ttu-id="49919-120">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49919-120">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49919-121">-確認</span><span class="sxs-lookup"><span data-stu-id="49919-121">-Confirm</span></span>
<span data-ttu-id="49919-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="49919-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49919-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49919-123">-WhatIf</span></span>
<span data-ttu-id="49919-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49919-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49919-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49919-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49919-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49919-126">CommonParameters</span></span>
<span data-ttu-id="49919-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="49919-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49919-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49919-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49919-129">輸入</span><span class="sxs-lookup"><span data-stu-id="49919-129">INPUTS</span></span>

### <span data-ttu-id="49919-130">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="49919-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="49919-131">輸出</span><span class="sxs-lookup"><span data-stu-id="49919-131">OUTPUTS</span></span>

### <span data-ttu-id="49919-132">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="49919-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="49919-133">筆記</span><span class="sxs-lookup"><span data-stu-id="49919-133">NOTES</span></span>

## <span data-ttu-id="49919-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="49919-134">RELATED LINKS</span></span>

[<span data-ttu-id="49919-135">Add-AzDATAData至</span><span class="sxs-lookup"><span data-stu-id="49919-135">Add-AzVMDataDisk</span></span>](./Add-AzVMDataDisk.md)

[<span data-ttu-id="49919-136">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="49919-136">Get-AzVM</span></span>](./Get-AzVM.md)


