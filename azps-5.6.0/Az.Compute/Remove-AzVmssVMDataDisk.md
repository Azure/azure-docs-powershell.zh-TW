---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssVMDataDisk.md
ms.openlocfilehash: c44369915c38219491bd8dfdc1ca288487da27f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906782"
---
# <span data-ttu-id="b3d51-101">Remove-AzVmssVMDataDisk</span><span class="sxs-lookup"><span data-stu-id="b3d51-101">Remove-AzVmssVMDataDisk</span></span>

## <span data-ttu-id="b3d51-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b3d51-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d51-103">從虛擬機器縮放集 VM 移除資料磁片</span><span class="sxs-lookup"><span data-stu-id="b3d51-103">Removes a data disk from a virtual machine scale set VM</span></span>

## <span data-ttu-id="b3d51-104">語法</span><span class="sxs-lookup"><span data-stu-id="b3d51-104">SYNTAX</span></span>

```
Remove-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3d51-105">描述</span><span class="sxs-lookup"><span data-stu-id="b3d51-105">DESCRIPTION</span></span>
<span data-ttu-id="b3d51-106">**Remove-Az VmsMS VMDataData Cmdlet** 會從 VM 縮放集 VM 移除資料磁片</span><span class="sxs-lookup"><span data-stu-id="b3d51-106">The **Remove-AzVmssVMDataDisk** cmdlet removes a data disk from a VM scale set VM</span></span>

## <span data-ttu-id="b3d51-107">例子</span><span class="sxs-lookup"><span data-stu-id="b3d51-107">EXAMPLES</span></span>

### <span data-ttu-id="b3d51-108">範例 1：從 VM 縮放集 VM 移除資料磁片</span><span class="sxs-lookup"><span data-stu-id="b3d51-108">Example 1: Remove a data disk from a VM scale set VM</span></span>
```powershell
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0 
PS C:\> Remove-AzVmssVMDataDisk -VM $VirtualMachine -Lun 0
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

<span data-ttu-id="b3d51-109">第一個命令會獲得資源組名、vms 名稱和實例識別碼提供的現有 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="b3d51-109">The first command getsan existing Vmss VM given by the resource group name, the vmss name and the instance ID.</span></span>
<span data-ttu-id="b3d51-110">第二個命令會從儲存在 $VmssVM 的 VM 縮放集 VM 中移除資料磁片 0。最後一個命令會以已移除的資料磁片更新 Vmss VM。</span><span class="sxs-lookup"><span data-stu-id="b3d51-110">The second command removes the data disk lun 0 from the VM scale set VM stored in $VmssVM The final command updates the Vmss VM with removed data disk.</span></span>

## <span data-ttu-id="b3d51-111">參數</span><span class="sxs-lookup"><span data-stu-id="b3d51-111">PARAMETERS</span></span>

### <span data-ttu-id="b3d51-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d51-112">-DefaultProfile</span></span>
<span data-ttu-id="b3d51-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b3d51-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3d51-114">-四分位</span><span class="sxs-lookup"><span data-stu-id="b3d51-114">-Lun</span></span>
<span data-ttu-id="b3d51-115">指定磁片的邏輯單位編號。</span><span class="sxs-lookup"><span data-stu-id="b3d51-115">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3d51-116">-VirtualMachineScaleSetMS</span><span class="sxs-lookup"><span data-stu-id="b3d51-116">-VirtualMachineScaleSetVM</span></span>
<span data-ttu-id="b3d51-117">虛擬機器縮放比例會設定 VM 設定檔。</span><span class="sxs-lookup"><span data-stu-id="b3d51-117">The virtual machine scale set VM profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d51-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d51-118">CommonParameters</span></span>
<span data-ttu-id="b3d51-119">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b3d51-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d51-120">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3d51-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d51-121">輸入</span><span class="sxs-lookup"><span data-stu-id="b3d51-121">INPUTS</span></span>

### <span data-ttu-id="b3d51-122">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSetVT</span><span class="sxs-lookup"><span data-stu-id="b3d51-122">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="b3d51-123">輸出</span><span class="sxs-lookup"><span data-stu-id="b3d51-123">OUTPUTS</span></span>

### <span data-ttu-id="b3d51-124">Microsoft.Azure.Commands.Compute.Automation.models.PSVirtualMachineScaleSetVT</span><span class="sxs-lookup"><span data-stu-id="b3d51-124">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM</span></span>

## <span data-ttu-id="b3d51-125">筆記</span><span class="sxs-lookup"><span data-stu-id="b3d51-125">NOTES</span></span>

## <span data-ttu-id="b3d51-126">相關連結</span><span class="sxs-lookup"><span data-stu-id="b3d51-126">RELATED LINKS</span></span>
