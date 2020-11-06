---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAccessExtension.md
ms.openlocfilehash: 9e7cb85bf29d6982271768af6948db1d3c5b8605
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447862"
---
# <span data-ttu-id="8434b-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8434b-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="8434b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8434b-102">SYNOPSIS</span></span>
<span data-ttu-id="8434b-103">取得 VMAccess 延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8434b-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8434b-104">句法</span><span class="sxs-lookup"><span data-stu-id="8434b-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [<CommonParameters>]
```

## <span data-ttu-id="8434b-105">說明</span><span class="sxs-lookup"><span data-stu-id="8434b-105">DESCRIPTION</span></span>
<span data-ttu-id="8434b-106">**AzureRmVMAccessExtension** Cmdlet 會取得虛擬機器存取 (VMAccess) 虛擬電腦延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8434b-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="8434b-107">示例</span><span class="sxs-lookup"><span data-stu-id="8434b-107">EXAMPLES</span></span>

### <span data-ttu-id="8434b-108">範例1：取得 VMAccess 延伸</span><span class="sxs-lookup"><span data-stu-id="8434b-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="8434b-109">這個命令會取得名為 VirtualMachine07 的虛擬機器的名為 ContosoTest 的 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="8434b-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="8434b-110">範例2：取得 VMAccess 延伸的 [實例] 視圖</span><span class="sxs-lookup"><span data-stu-id="8434b-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="8434b-111">這個命令會取得名為 VirtualMachine07 的虛擬機器之 VMAccess 延伸 ContosoTest 的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="8434b-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="8434b-112">參數</span><span class="sxs-lookup"><span data-stu-id="8434b-112">PARAMETERS</span></span>

### <span data-ttu-id="8434b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="8434b-113">-Name</span></span>
<span data-ttu-id="8434b-114">指定此 Cmdlet 所取得之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="8434b-114">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8434b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8434b-115">-ResourceGroupName</span></span>
<span data-ttu-id="8434b-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="8434b-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8434b-117">-狀態</span><span class="sxs-lookup"><span data-stu-id="8434b-117">-Status</span></span>
<span data-ttu-id="8434b-118">表示此 Cmdlet 只會取得延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="8434b-118">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8434b-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="8434b-119">-VMName</span></span>
<span data-ttu-id="8434b-120">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="8434b-120">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="8434b-121">這個 Cmdlet 會取得此參數指定之虛擬機器之 VMAccess 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="8434b-121">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8434b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8434b-122">CommonParameters</span></span>
<span data-ttu-id="8434b-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8434b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8434b-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8434b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8434b-125">輸入</span><span class="sxs-lookup"><span data-stu-id="8434b-125">INPUTS</span></span>

### <span data-ttu-id="8434b-126">所有</span><span class="sxs-lookup"><span data-stu-id="8434b-126">None</span></span>
<span data-ttu-id="8434b-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="8434b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8434b-128">輸出</span><span class="sxs-lookup"><span data-stu-id="8434b-128">OUTPUTS</span></span>

## <span data-ttu-id="8434b-129">筆記</span><span class="sxs-lookup"><span data-stu-id="8434b-129">NOTES</span></span>

## <span data-ttu-id="8434b-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="8434b-130">RELATED LINKS</span></span>

[<span data-ttu-id="8434b-131">移除-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8434b-131">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="8434b-132">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="8434b-132">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="8434b-133">AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="8434b-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


