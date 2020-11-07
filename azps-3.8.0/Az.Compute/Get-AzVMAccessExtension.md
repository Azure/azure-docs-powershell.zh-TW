---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: c139e1bac6f910a1759e4482abdd7c67d2e7fa55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93966505"
---
# <span data-ttu-id="2c0f2-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="2c0f2-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="2c0f2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c0f2-102">SYNOPSIS</span></span>
<span data-ttu-id="2c0f2-103">取得 VMAccess 延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="2c0f2-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c0f2-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2c0f2-105">說明</span><span class="sxs-lookup"><span data-stu-id="2c0f2-105">DESCRIPTION</span></span>
<span data-ttu-id="2c0f2-106">**AzVMAccessExtension** Cmdlet 會取得虛擬機器存取 (VMAccess) 虛擬電腦延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="2c0f2-107">示例</span><span class="sxs-lookup"><span data-stu-id="2c0f2-107">EXAMPLES</span></span>

### <span data-ttu-id="2c0f2-108">範例1：取得 VMAccess 延伸</span><span class="sxs-lookup"><span data-stu-id="2c0f2-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="2c0f2-109">這個命令會取得名為 VirtualMachine07 的虛擬機器的名為 ContosoTest 的 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="2c0f2-110">範例2：取得 VMAccess 延伸的 [實例] 視圖</span><span class="sxs-lookup"><span data-stu-id="2c0f2-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="2c0f2-111">這個命令會取得名為 VirtualMachine07 的虛擬機器之 VMAccess 延伸 ContosoTest 的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="2c0f2-112">參數</span><span class="sxs-lookup"><span data-stu-id="2c0f2-112">PARAMETERS</span></span>

### <span data-ttu-id="2c0f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c0f2-113">-DefaultProfile</span></span>
<span data-ttu-id="2c0f2-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c0f2-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c0f2-115">-Name</span></span>
<span data-ttu-id="2c0f2-116">指定此 Cmdlet 所取得之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="2c0f2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c0f2-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c0f2-118">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2c0f2-119">-狀態</span><span class="sxs-lookup"><span data-stu-id="2c0f2-119">-Status</span></span>
<span data-ttu-id="2c0f2-120">表示此 Cmdlet 只會取得延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="2c0f2-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="2c0f2-121">-VMName</span></span>
<span data-ttu-id="2c0f2-122">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2c0f2-123">這個 Cmdlet 會取得此參數指定之虛擬機器之 VMAccess 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="2c0f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c0f2-124">CommonParameters</span></span>
<span data-ttu-id="2c0f2-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c0f2-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="2c0f2-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c0f2-127">輸入</span><span class="sxs-lookup"><span data-stu-id="2c0f2-127">INPUTS</span></span>

### <span data-ttu-id="2c0f2-128">System.object</span><span class="sxs-lookup"><span data-stu-id="2c0f2-128">System.String</span></span>

### <span data-ttu-id="2c0f2-129">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="2c0f2-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2c0f2-130">輸出</span><span class="sxs-lookup"><span data-stu-id="2c0f2-130">OUTPUTS</span></span>

### <span data-ttu-id="2c0f2-131">VirtualMachineAccessExtensionCoNtext 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="2c0f2-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="2c0f2-132">筆記</span><span class="sxs-lookup"><span data-stu-id="2c0f2-132">NOTES</span></span>

## <span data-ttu-id="2c0f2-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c0f2-133">RELATED LINKS</span></span>

[<span data-ttu-id="2c0f2-134">移除-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="2c0f2-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="2c0f2-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="2c0f2-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="2c0f2-136">AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="2c0f2-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


