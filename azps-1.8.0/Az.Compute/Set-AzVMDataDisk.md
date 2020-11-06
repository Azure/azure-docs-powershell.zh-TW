---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: 032efea1c892905a41dc141e253cd480c3f3bba7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622679"
---
# <span data-ttu-id="1d24c-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="1d24c-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="1d24c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1d24c-102">SYNOPSIS</span></span>
<span data-ttu-id="1d24c-103">修改虛擬機器資料磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="1d24c-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="1d24c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1d24c-104">SYNTAX</span></span>

### <span data-ttu-id="1d24c-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="1d24c-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d24c-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="1d24c-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>]
 [-StorageAccountType <String>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d24c-107">說明</span><span class="sxs-lookup"><span data-stu-id="1d24c-107">DESCRIPTION</span></span>
<span data-ttu-id="1d24c-108">**AzVMDataDisk** Cmdlet 會修改虛擬機器資料磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="1d24c-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="1d24c-109">示例</span><span class="sxs-lookup"><span data-stu-id="1d24c-109">EXAMPLES</span></span>

### <span data-ttu-id="1d24c-110">範例1：修改資料磁片的快取模式</span><span class="sxs-lookup"><span data-stu-id="1d24c-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="1d24c-111">第一個命令會使用 **AzVM** 來取得名為 ContosoVM07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1d24c-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="1d24c-112">該命令會將它儲存在 $VM 變數中。</span><span class="sxs-lookup"><span data-stu-id="1d24c-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="1d24c-113">第二個命令會修改 $VM 虛擬機器上名為 DataDisk01 之資料磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="1d24c-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="1d24c-114">命令會將結果傳遞給 Update-AzVM Cmdlet，以執行您的變更。</span><span class="sxs-lookup"><span data-stu-id="1d24c-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="1d24c-115">對 cashing 模式所做的變更會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="1d24c-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="1d24c-116">參數</span><span class="sxs-lookup"><span data-stu-id="1d24c-116">PARAMETERS</span></span>

### <span data-ttu-id="1d24c-117">-快取</span><span class="sxs-lookup"><span data-stu-id="1d24c-117">-Caching</span></span>
<span data-ttu-id="1d24c-118">指定磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="1d24c-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="1d24c-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="1d24c-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1d24c-120">唯讀</span><span class="sxs-lookup"><span data-stu-id="1d24c-120">ReadOnly</span></span>
- <span data-ttu-id="1d24c-121">ReadWrite 的預設值是 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="1d24c-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="1d24c-122">變更此值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="1d24c-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="1d24c-123">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="1d24c-123">This setting affects the consistency and performance of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d24c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d24c-124">-DefaultProfile</span></span>
<span data-ttu-id="1d24c-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1d24c-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d24c-126">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="1d24c-126">-DiskSizeInGB</span></span>
<span data-ttu-id="1d24c-127">指定資料磁片的大小（以 gb 為數）。</span><span class="sxs-lookup"><span data-stu-id="1d24c-127">Specifies the size, in gigabytes, for the data disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d24c-128">-Lun</span><span class="sxs-lookup"><span data-stu-id="1d24c-128">-Lun</span></span>
<span data-ttu-id="1d24c-129">指定此 Cmdlet 所修改之資料磁片的邏輯單元號碼 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="1d24c-129">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ChangeWithLun
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d24c-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="1d24c-130">-Name</span></span>
<span data-ttu-id="1d24c-131">指定此 Cmdlet 所修改之資料磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="1d24c-131">Specifies the name of the data disk that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ChangeWithName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d24c-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="1d24c-132">-StorageAccountType</span></span>
<span data-ttu-id="1d24c-133">虛擬機器受管理磁片的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="1d24c-133">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d24c-134">-VM</span><span class="sxs-lookup"><span data-stu-id="1d24c-134">-VM</span></span>
<span data-ttu-id="1d24c-135">指定此 Cmdlet 修改資料磁片的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="1d24c-135">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="1d24c-136">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1d24c-136">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="1d24c-137">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="1d24c-137">-WriteAccelerator</span></span>
<span data-ttu-id="1d24c-138">指定是否應該在資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="1d24c-138">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d24c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d24c-139">CommonParameters</span></span>
<span data-ttu-id="1d24c-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1d24c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d24c-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1d24c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d24c-142">輸入</span><span class="sxs-lookup"><span data-stu-id="1d24c-142">INPUTS</span></span>

### <span data-ttu-id="1d24c-143">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="1d24c-143">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="1d24c-144">System.object</span><span class="sxs-lookup"><span data-stu-id="1d24c-144">System.String</span></span>

### <span data-ttu-id="1d24c-145">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1d24c-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1d24c-146">"CachingTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="1d24c-146">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="1d24c-147">輸出</span><span class="sxs-lookup"><span data-stu-id="1d24c-147">OUTPUTS</span></span>

### <span data-ttu-id="1d24c-148">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="1d24c-148">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1d24c-149">筆記</span><span class="sxs-lookup"><span data-stu-id="1d24c-149">NOTES</span></span>

## <span data-ttu-id="1d24c-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="1d24c-150">RELATED LINKS</span></span>

[<span data-ttu-id="1d24c-151">AzVM</span><span class="sxs-lookup"><span data-stu-id="1d24c-151">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="1d24c-152">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="1d24c-152">Update-AzVM</span></span>](./Update-AzVM.md)


