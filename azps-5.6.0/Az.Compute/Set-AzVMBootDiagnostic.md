---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBootDiagnostic.md
ms.openlocfilehash: a163854838dcb8e41b7a8b65d1be9e1aca088d55
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101911749"
---
# <span data-ttu-id="77ee0-101">Set-AzVMBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="77ee0-101">Set-AzVMBootDiagnostic</span></span>

## <span data-ttu-id="77ee0-102">簡介</span><span class="sxs-lookup"><span data-stu-id="77ee0-102">SYNOPSIS</span></span>
<span data-ttu-id="77ee0-103">修改虛擬機器的開機診斷屬性。</span><span class="sxs-lookup"><span data-stu-id="77ee0-103">Modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="77ee0-104">語法</span><span class="sxs-lookup"><span data-stu-id="77ee0-104">SYNTAX</span></span>

### <span data-ttu-id="77ee0-105">EnableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="77ee0-105">EnableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="77ee0-106">DisableBootDiagnostics</span><span class="sxs-lookup"><span data-stu-id="77ee0-106">DisableBootDiagnostics</span></span>
```
Set-AzVMBootDiagnostic [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="77ee0-107">描述</span><span class="sxs-lookup"><span data-stu-id="77ee0-107">DESCRIPTION</span></span>
<span data-ttu-id="77ee0-108">**Set-Az VIRTUALBootDiagnostic** Cmdlet 會修改虛擬機器的開機診斷屬性。</span><span class="sxs-lookup"><span data-stu-id="77ee0-108">The **Set-AzVMBootDiagnostic** cmdlet modifies boot diagnostics properties of a virtual machine.</span></span>

## <span data-ttu-id="77ee0-109">例子</span><span class="sxs-lookup"><span data-stu-id="77ee0-109">EXAMPLES</span></span>

### <span data-ttu-id="77ee0-110">範例 1：啟用開機診斷</span><span class="sxs-lookup"><span data-stu-id="77ee0-110">Example 1: Enable boot diagnostics</span></span>
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzVMBootDiagnostic -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzVM -VM $VM
```

<span data-ttu-id="77ee0-111">第一個命令會使用 **Get-Az%。這個命令會取得名為 ContosoEV07** 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="77ee0-111">The first command gets the virtual machine named ContosoVM07 by using **Get-AzVM**.</span></span>
<span data-ttu-id="77ee0-112">命令會儲存在$VM變數中。</span><span class="sxs-lookup"><span data-stu-id="77ee0-112">The command stores it in the $VM variable.</span></span>
<span data-ttu-id="77ee0-113">第二個命令會針對 $VM 中的虛擬機器啟用開機$VM。</span><span class="sxs-lookup"><span data-stu-id="77ee0-113">The second command enables boot diagnostics for the virtual machine in $VM.</span></span>
<span data-ttu-id="77ee0-114">診斷資料會儲存在指定的帳號中。</span><span class="sxs-lookup"><span data-stu-id="77ee0-114">Diagnostics data is stored in the specified account.</span></span>

## <span data-ttu-id="77ee0-115">參數</span><span class="sxs-lookup"><span data-stu-id="77ee0-115">PARAMETERS</span></span>

### <span data-ttu-id="77ee0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77ee0-116">-DefaultProfile</span></span>
<span data-ttu-id="77ee0-117">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="77ee0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77ee0-118">-停用</span><span class="sxs-lookup"><span data-stu-id="77ee0-118">-Disable</span></span>
<span data-ttu-id="77ee0-119">表示此 Cmdlet 會停用虛擬機器的開機診斷。</span><span class="sxs-lookup"><span data-stu-id="77ee0-119">Indicates that this cmdlet disables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77ee0-120">-啟用</span><span class="sxs-lookup"><span data-stu-id="77ee0-120">-Enable</span></span>
<span data-ttu-id="77ee0-121">表示此 Cmdlet 啟用虛擬機器的開機診斷。</span><span class="sxs-lookup"><span data-stu-id="77ee0-121">Indicates that this cmdlet enables the boot diagnostics for the virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77ee0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77ee0-122">-ResourceGroupName</span></span>
<span data-ttu-id="77ee0-123">指定儲存帳戶的資源組名。</span><span class="sxs-lookup"><span data-stu-id="77ee0-123">Specifies the name of the resource group of storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77ee0-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="77ee0-124">-StorageAccountName</span></span>
<span data-ttu-id="77ee0-125">指定儲存開機診斷資料的儲存空間帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="77ee0-125">Specifies the name of the storage account in which to save boot diagnostics data.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableBootDiagnostics
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77ee0-126">-VM</span><span class="sxs-lookup"><span data-stu-id="77ee0-126">-VM</span></span>
<span data-ttu-id="77ee0-127">指定此 Cmdlet 變更開機診斷的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="77ee0-127">Specifies the virtual machine for which this cmdlet changes boot diagnostics.</span></span>
<span data-ttu-id="77ee0-128">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="77ee0-128">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="77ee0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77ee0-129">CommonParameters</span></span>
<span data-ttu-id="77ee0-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="77ee0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77ee0-131">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="77ee0-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77ee0-132">輸入</span><span class="sxs-lookup"><span data-stu-id="77ee0-132">INPUTS</span></span>

### <span data-ttu-id="77ee0-133">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="77ee0-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="77ee0-134">System.String</span><span class="sxs-lookup"><span data-stu-id="77ee0-134">System.String</span></span>

## <span data-ttu-id="77ee0-135">輸出</span><span class="sxs-lookup"><span data-stu-id="77ee0-135">OUTPUTS</span></span>

### <span data-ttu-id="77ee0-136">Microsoft.Azure.Commands.Compute.models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="77ee0-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="77ee0-137">筆記</span><span class="sxs-lookup"><span data-stu-id="77ee0-137">NOTES</span></span>

## <span data-ttu-id="77ee0-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="77ee0-138">RELATED LINKS</span></span>

[<span data-ttu-id="77ee0-139">Get-AzMS</span><span class="sxs-lookup"><span data-stu-id="77ee0-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="77ee0-140">Get-AzDATABootDiagnosticsData</span><span class="sxs-lookup"><span data-stu-id="77ee0-140">Get-AzVMBootDiagnosticsData</span></span>](./Get-AzVMBootDiagnosticsData.md)


