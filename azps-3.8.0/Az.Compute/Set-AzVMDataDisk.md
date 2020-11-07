---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: 2361fc663efc3ec4a967c718abd778599ca5340b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966085"
---
# <span data-ttu-id="624ac-101">Set-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="624ac-101">Set-AzVMDataDisk</span></span>

## <span data-ttu-id="624ac-102">摘要</span><span class="sxs-lookup"><span data-stu-id="624ac-102">SYNOPSIS</span></span>
<span data-ttu-id="624ac-103">修改虛擬機器資料磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="624ac-103">Modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="624ac-104">句法</span><span class="sxs-lookup"><span data-stu-id="624ac-104">SYNTAX</span></span>

### <span data-ttu-id="624ac-105">ChangeWithName</span><span class="sxs-lookup"><span data-stu-id="624ac-105">ChangeWithName</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="624ac-106">ChangeWithLun</span><span class="sxs-lookup"><span data-stu-id="624ac-106">ChangeWithLun</span></span>
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>]
 [-StorageAccountType <String>] [-DiskEncryptionSetId <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="624ac-107">說明</span><span class="sxs-lookup"><span data-stu-id="624ac-107">DESCRIPTION</span></span>
<span data-ttu-id="624ac-108">**AzVMDataDisk** Cmdlet 會修改虛擬機器資料磁片的屬性。</span><span class="sxs-lookup"><span data-stu-id="624ac-108">The **Set-AzVMDataDisk** cmdlet modifies properties of a virtual machine data disk.</span></span>

## <span data-ttu-id="624ac-109">示例</span><span class="sxs-lookup"><span data-stu-id="624ac-109">EXAMPLES</span></span>

### <span data-ttu-id="624ac-110">範例1：修改資料磁片的快取模式</span><span class="sxs-lookup"><span data-stu-id="624ac-110">Example 1: Modify the caching mode of a data disk</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

<span data-ttu-id="624ac-111">第一個命令會使用 **AzVM** 來取得名為 ContosoVM07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="624ac-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="624ac-112">該命令會將它儲存在 $VM 變數中。</span><span class="sxs-lookup"><span data-stu-id="624ac-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="624ac-113">第二個命令會修改 $VM 虛擬機器上名為 DataDisk01 之資料磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="624ac-113">The second command modifies the caching mode for the data disk named DataDisk01 on the virtual machine in $VM.</span></span>
<span data-ttu-id="624ac-114">命令會將結果傳遞給 Update-AzVM Cmdlet，以執行您的變更。</span><span class="sxs-lookup"><span data-stu-id="624ac-114">The command passes the result to the Update-AzVM cmdlet, which implements your changes.</span></span>
<span data-ttu-id="624ac-115">對 cashing 模式所做的變更會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="624ac-115">A change to the cashing mode causes the virtual machine to restart.</span></span>

## <span data-ttu-id="624ac-116">參數</span><span class="sxs-lookup"><span data-stu-id="624ac-116">PARAMETERS</span></span>

### <span data-ttu-id="624ac-117">-快取</span><span class="sxs-lookup"><span data-stu-id="624ac-117">-Caching</span></span>
<span data-ttu-id="624ac-118">指定磁片的快取模式。</span><span class="sxs-lookup"><span data-stu-id="624ac-118">Specifies the caching mode of the disk.</span></span>
<span data-ttu-id="624ac-119">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="624ac-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="624ac-120">唯讀</span><span class="sxs-lookup"><span data-stu-id="624ac-120">ReadOnly</span></span>
- <span data-ttu-id="624ac-121">ReadWrite 的預設值是 ReadWrite。</span><span class="sxs-lookup"><span data-stu-id="624ac-121">ReadWrite The default value is ReadWrite.</span></span>
<span data-ttu-id="624ac-122">變更此值會導致虛擬機器重新開機。</span><span class="sxs-lookup"><span data-stu-id="624ac-122">Changing this value causes the virtual machine to restart.</span></span>
<span data-ttu-id="624ac-123">此設定會影響磁片的一致性和效能。</span><span class="sxs-lookup"><span data-stu-id="624ac-123">This setting affects the consistency and performance of the disk.</span></span>

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

### <span data-ttu-id="624ac-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="624ac-124">-DefaultProfile</span></span>
<span data-ttu-id="624ac-125">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="624ac-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="624ac-126">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="624ac-126">-DiskEncryptionSetId</span></span>
<span data-ttu-id="624ac-127">指定客戶管理磁片加密集的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="624ac-127">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="624ac-128">只能為受管理的磁片指定這種情況。</span><span class="sxs-lookup"><span data-stu-id="624ac-128">This can only be specified for managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="624ac-129">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="624ac-129">-DiskSizeInGB</span></span>
<span data-ttu-id="624ac-130">指定資料磁片的大小（以 gb 為數）。</span><span class="sxs-lookup"><span data-stu-id="624ac-130">Specifies the size, in gigabytes, for the data disk.</span></span>

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

### <span data-ttu-id="624ac-131">-Lun</span><span class="sxs-lookup"><span data-stu-id="624ac-131">-Lun</span></span>
<span data-ttu-id="624ac-132">指定此 Cmdlet 所修改之資料磁片的邏輯單元號碼 (LUN) 。</span><span class="sxs-lookup"><span data-stu-id="624ac-132">Specifies the logical unit number (LUN) of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="624ac-133">-名稱</span><span class="sxs-lookup"><span data-stu-id="624ac-133">-Name</span></span>
<span data-ttu-id="624ac-134">指定此 Cmdlet 所修改之資料磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="624ac-134">Specifies the name of the data disk that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="624ac-135">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="624ac-135">-StorageAccountType</span></span>
<span data-ttu-id="624ac-136">虛擬機器受管理磁片的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="624ac-136">The virtual machine managed disk's account type.</span></span>

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

### <span data-ttu-id="624ac-137">-VM</span><span class="sxs-lookup"><span data-stu-id="624ac-137">-VM</span></span>
<span data-ttu-id="624ac-138">指定此 Cmdlet 修改資料磁片的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="624ac-138">Specifies the virtual machine for which this cmdlet modifies a data disk.</span></span>
<span data-ttu-id="624ac-139">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="624ac-139">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="624ac-140">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="624ac-140">-WriteAccelerator</span></span>
<span data-ttu-id="624ac-141">指定是否應該在資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="624ac-141">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="624ac-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="624ac-142">CommonParameters</span></span>
<span data-ttu-id="624ac-143">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="624ac-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="624ac-144">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="624ac-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="624ac-145">輸入</span><span class="sxs-lookup"><span data-stu-id="624ac-145">INPUTS</span></span>

### <span data-ttu-id="624ac-146">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="624ac-146">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="624ac-147">System.object</span><span class="sxs-lookup"><span data-stu-id="624ac-147">System.String</span></span>

### <span data-ttu-id="624ac-148">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="624ac-148">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="624ac-149">"CachingTypes" 1 [[23.0.0.0]。計算，版本 =，Culture = 中性，PublicKeyToken = 31bf3856ad364e35 "]]）。）</span><span class="sxs-lookup"><span data-stu-id="624ac-149">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="624ac-150">輸出</span><span class="sxs-lookup"><span data-stu-id="624ac-150">OUTPUTS</span></span>

### <span data-ttu-id="624ac-151">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="624ac-151">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="624ac-152">筆記</span><span class="sxs-lookup"><span data-stu-id="624ac-152">NOTES</span></span>

## <span data-ttu-id="624ac-153">相關連結</span><span class="sxs-lookup"><span data-stu-id="624ac-153">RELATED LINKS</span></span>

[<span data-ttu-id="624ac-154">AzVM</span><span class="sxs-lookup"><span data-stu-id="624ac-154">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="624ac-155">更新-AzVM</span><span class="sxs-lookup"><span data-stu-id="624ac-155">Update-AzVM</span></span>](./Update-AzVM.md)


