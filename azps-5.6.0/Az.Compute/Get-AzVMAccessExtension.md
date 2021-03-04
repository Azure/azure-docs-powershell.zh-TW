---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: f89260b083d07ca717e1e302c2fb0bb747005d43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909182"
---
# <span data-ttu-id="b601b-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b601b-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="b601b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b601b-102">SYNOPSIS</span></span>
<span data-ttu-id="b601b-103">獲得有關 VMAccess 擴充功能的資訊。</span><span class="sxs-lookup"><span data-stu-id="b601b-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="b601b-104">語法</span><span class="sxs-lookup"><span data-stu-id="b601b-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b601b-105">描述</span><span class="sxs-lookup"><span data-stu-id="b601b-105">DESCRIPTION</span></span>
<span data-ttu-id="b601b-106">**Get-Az VMAccessExtension** Cmdlet 會取得虛擬機器擴充功能 (VMAccess) 相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b601b-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="b601b-107">例子</span><span class="sxs-lookup"><span data-stu-id="b601b-107">EXAMPLES</span></span>

### <span data-ttu-id="b601b-108">範例 1：取得 VMAccess 擴充功能</span><span class="sxs-lookup"><span data-stu-id="b601b-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="b601b-109">此命令會針對名為 VirtualMachine07 的虛擬機器，獲得名為 ContosoTest 的 VMAccess 副檔名。</span><span class="sxs-lookup"><span data-stu-id="b601b-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="b601b-110">範例 2：取得 VMAccess 副檔名的實例視圖</span><span class="sxs-lookup"><span data-stu-id="b601b-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="b601b-111">此命令會針對名為 VirtualMachine07 的虛擬機器，獲得名為 ContosoTest 的 VMAccess 副檔名的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="b601b-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="b601b-112">參數</span><span class="sxs-lookup"><span data-stu-id="b601b-112">PARAMETERS</span></span>

### <span data-ttu-id="b601b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b601b-113">-DefaultProfile</span></span>
<span data-ttu-id="b601b-114">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="b601b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b601b-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="b601b-115">-Name</span></span>
<span data-ttu-id="b601b-116">指定此 Cmdlet 所獲取的副檔名。</span><span class="sxs-lookup"><span data-stu-id="b601b-116">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b601b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b601b-117">-ResourceGroupName</span></span>
<span data-ttu-id="b601b-118">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="b601b-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b601b-119">-狀態</span><span class="sxs-lookup"><span data-stu-id="b601b-119">-Status</span></span>
<span data-ttu-id="b601b-120">表示此 Cmdlet 僅會獲得擴充功能的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="b601b-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b601b-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="b601b-121">-VMName</span></span>
<span data-ttu-id="b601b-122">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b601b-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="b601b-123">此 Cmdlet 會針對此參數指定的虛擬機器，獲得有關 VMAccess 的資訊。</span><span class="sxs-lookup"><span data-stu-id="b601b-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b601b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b601b-124">CommonParameters</span></span>
<span data-ttu-id="b601b-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b601b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b601b-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b601b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b601b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="b601b-127">INPUTS</span></span>

### <span data-ttu-id="b601b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b601b-128">System.String</span></span>

### <span data-ttu-id="b601b-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b601b-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="b601b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="b601b-130">OUTPUTS</span></span>

### <span data-ttu-id="b601b-131">Microsoft.Azure.Commands.Compute.models.VirtualMachineAccesssExtensionCoNtext</span><span class="sxs-lookup"><span data-stu-id="b601b-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="b601b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="b601b-132">NOTES</span></span>

## <span data-ttu-id="b601b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="b601b-133">RELATED LINKS</span></span>

[<span data-ttu-id="b601b-134">Remove-AzEVAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b601b-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="b601b-135">Set-AzEVAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b601b-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="b601b-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="b601b-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


