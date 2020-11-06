---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMDataDisk.md
ms.openlocfilehash: 67158561b9a0369d65d3a846b4156f914a97358a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622750"
---
# <span data-ttu-id="365e1-101">New-AzVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="365e1-101">New-AzVMDataDisk</span></span>

## <span data-ttu-id="365e1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="365e1-102">SYNOPSIS</span></span>
<span data-ttu-id="365e1-103">為虛擬機器或 Vmss VM 建立本機資料磁片物件。</span><span class="sxs-lookup"><span data-stu-id="365e1-103">Creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="365e1-104">句法</span><span class="sxs-lookup"><span data-stu-id="365e1-104">SYNTAX</span></span>

### <span data-ttu-id="365e1-105">NormalDiskParameterSetName (預設) </span><span class="sxs-lookup"><span data-stu-id="365e1-105">NormalDiskParameterSetName (Default)</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-VhdUri <String>] [-SourceImageUri <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="365e1-106">ManagedDiskParameterSetName</span><span class="sxs-lookup"><span data-stu-id="365e1-106">ManagedDiskParameterSetName</span></span>
```
New-AzVMDataDisk [-Lun] <Int32> [-CreateOption] <String> [-Name <String>] [-Caching <CachingTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <String>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="365e1-107">說明</span><span class="sxs-lookup"><span data-stu-id="365e1-107">DESCRIPTION</span></span>
<span data-ttu-id="365e1-108">**新的-AzVMDataDisk** Cmdlet 會為虛擬機器或 Vmss VM 建立本機資料磁片物件。</span><span class="sxs-lookup"><span data-stu-id="365e1-108">The **New-AzVMDataDisk** cmdlet creates a local data disk object for a virtual machine or a Vmss VM.</span></span>

## <span data-ttu-id="365e1-109">示例</span><span class="sxs-lookup"><span data-stu-id="365e1-109">EXAMPLES</span></span>

### <span data-ttu-id="365e1-110">範例1：將受管理的資料磁片新增至 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="365e1-110">Example 1: Add a managed data disk to a Vmss VM.</span></span>
```
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $datadisk = New-AzVMDataDisk -Caching 'ReadOnly' -Lun 2 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> Update-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 -DataDisk $datadisk
```

<span data-ttu-id="365e1-111">第一個命令會取得現有的受管理磁片。</span><span class="sxs-lookup"><span data-stu-id="365e1-111">The first command gets an existing managed disk.</span></span>
<span data-ttu-id="365e1-112">下一個命令會使用受管理的磁片建立資料磁片物件。</span><span class="sxs-lookup"><span data-stu-id="365e1-112">The next command creates a data disk object with the managed disk.</span></span>
<span data-ttu-id="365e1-113">Next 命令會取得資源群組名稱所提供的現有 Vmss VM、Vmss 名稱和實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="365e1-113">The next command gets an existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="365e1-114">最後一個命令會透過新增資料磁片來更新 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="365e1-114">The final command updates the Vmss VM by adding a new data disk.</span></span>

## <span data-ttu-id="365e1-115">參數</span><span class="sxs-lookup"><span data-stu-id="365e1-115">PARAMETERS</span></span>

### <span data-ttu-id="365e1-116">-快取</span><span class="sxs-lookup"><span data-stu-id="365e1-116">-Caching</span></span>
<span data-ttu-id="365e1-117">虛擬機器資料磁片的快取。</span><span class="sxs-lookup"><span data-stu-id="365e1-117">The virtual machine data disk's caching.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365e1-118">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="365e1-118">-CreateOption</span></span>
<span data-ttu-id="365e1-119">虛擬機器資料磁片的 [建立] 選項。</span><span class="sxs-lookup"><span data-stu-id="365e1-119">The virtual machine data disk's create option.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365e1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="365e1-120">-DefaultProfile</span></span>
<span data-ttu-id="365e1-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="365e1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="365e1-122">-DiskSizeInGB</span><span class="sxs-lookup"><span data-stu-id="365e1-122">-DiskSizeInGB</span></span>
<span data-ttu-id="365e1-123">虛擬機器資料磁片的大小（以 GB 為規格）。</span><span class="sxs-lookup"><span data-stu-id="365e1-123">The virtual machine data disk's size in GB.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365e1-124">-Lun</span><span class="sxs-lookup"><span data-stu-id="365e1-124">-Lun</span></span>
<span data-ttu-id="365e1-125">虛擬機器資料磁片的 Lun。</span><span class="sxs-lookup"><span data-stu-id="365e1-125">The virtual machine data disk's Lun.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365e1-126">-ManagedDiskId</span><span class="sxs-lookup"><span data-stu-id="365e1-126">-ManagedDiskId</span></span>
<span data-ttu-id="365e1-127">虛擬機器受管理磁片的 Id。</span><span class="sxs-lookup"><span data-stu-id="365e1-127">The virtual machine managed disk's Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365e1-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="365e1-128">-Name</span></span>
<span data-ttu-id="365e1-129">虛擬機器資料磁片的名稱。</span><span class="sxs-lookup"><span data-stu-id="365e1-129">The virtual machine data disk's name.</span></span>

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

### <span data-ttu-id="365e1-130">-SourceImageUri</span><span class="sxs-lookup"><span data-stu-id="365e1-130">-SourceImageUri</span></span>
<span data-ttu-id="365e1-131">虛擬機器 OS 磁片的來源影像 Uri。</span><span class="sxs-lookup"><span data-stu-id="365e1-131">The virtual machine OS disk's source image Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases: SourceImage

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365e1-132">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="365e1-132">-StorageAccountType</span></span>
<span data-ttu-id="365e1-133">虛擬機器受管理磁片的帳戶類型。</span><span class="sxs-lookup"><span data-stu-id="365e1-133">The virtual machine managed disk's account type.</span></span>

```yaml
Type: System.String
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365e1-134">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="365e1-134">-VhdUri</span></span>
<span data-ttu-id="365e1-135">虛擬機器資料磁片的 Vhd Uri。</span><span class="sxs-lookup"><span data-stu-id="365e1-135">The virtual machine data disk's Vhd Uri.</span></span>

```yaml
Type: System.String
Parameter Sets: NormalDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365e1-136">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="365e1-136">-WriteAccelerator</span></span>
<span data-ttu-id="365e1-137">指定是否應該在受管理的資料磁片上啟用或停用 WriteAccelerator。</span><span class="sxs-lookup"><span data-stu-id="365e1-137">Specifies whether WriteAccelerator should be enabled or disabled on a managed data disk.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedDiskParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365e1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365e1-138">CommonParameters</span></span>
<span data-ttu-id="365e1-139">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="365e1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365e1-140">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="365e1-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365e1-141">輸入</span><span class="sxs-lookup"><span data-stu-id="365e1-141">INPUTS</span></span>

### <span data-ttu-id="365e1-142">System.object</span><span class="sxs-lookup"><span data-stu-id="365e1-142">System.Int32</span></span>

### <span data-ttu-id="365e1-143">System.object</span><span class="sxs-lookup"><span data-stu-id="365e1-143">System.String</span></span>

### <span data-ttu-id="365e1-144">CachingTypes 中的 [Azure. 管理]</span><span class="sxs-lookup"><span data-stu-id="365e1-144">Microsoft.Azure.Management.Compute.Models.CachingTypes</span></span>

### <span data-ttu-id="365e1-145">"CoreLib" 1 ["System.object，System.object，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="365e1-145">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="365e1-146">輸出</span><span class="sxs-lookup"><span data-stu-id="365e1-146">OUTPUTS</span></span>

### <span data-ttu-id="365e1-147">PSVirtualMachineDataDisk 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="365e1-147">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineDataDisk</span></span>

## <span data-ttu-id="365e1-148">筆記</span><span class="sxs-lookup"><span data-stu-id="365e1-148">NOTES</span></span>

## <span data-ttu-id="365e1-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="365e1-149">RELATED LINKS</span></span>
