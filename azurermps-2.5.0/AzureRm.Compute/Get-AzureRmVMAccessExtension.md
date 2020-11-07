---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmaccessextension
schema: 2.0.0
ms.openlocfilehash: 5d07d90e7a9902713be3ef4d2acf3a2650e4f1b4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93800550"
---
# <span data-ttu-id="9425f-101">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9425f-101">Get-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="9425f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9425f-102">SYNOPSIS</span></span>
<span data-ttu-id="9425f-103">取得 VMAccess 延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9425f-103">Gets information about the VMAccess extension.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9425f-104">句法</span><span class="sxs-lookup"><span data-stu-id="9425f-104">SYNTAX</span></span>

```
Get-AzureRmVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9425f-105">說明</span><span class="sxs-lookup"><span data-stu-id="9425f-105">DESCRIPTION</span></span>
<span data-ttu-id="9425f-106">**AzureRmVMAccessExtension** Cmdlet 會取得虛擬機器存取 (VMAccess) 虛擬電腦延伸的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9425f-106">The **Get-AzureRmVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="9425f-107">示例</span><span class="sxs-lookup"><span data-stu-id="9425f-107">EXAMPLES</span></span>

### <span data-ttu-id="9425f-108">範例1：取得 VMAccess 延伸</span><span class="sxs-lookup"><span data-stu-id="9425f-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="9425f-109">這個命令會取得名為 VirtualMachine07 的虛擬機器的名為 ContosoTest 的 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="9425f-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="9425f-110">範例2：取得 VMAccess 延伸的 [實例] 視圖</span><span class="sxs-lookup"><span data-stu-id="9425f-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzureRmVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="9425f-111">這個命令會取得名為 VirtualMachine07 的虛擬機器之 VMAccess 延伸 ContosoTest 的實例視圖。</span><span class="sxs-lookup"><span data-stu-id="9425f-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="9425f-112">參數</span><span class="sxs-lookup"><span data-stu-id="9425f-112">PARAMETERS</span></span>

### <span data-ttu-id="9425f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9425f-113">-DefaultProfile</span></span>
<span data-ttu-id="9425f-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9425f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9425f-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="9425f-115">-Name</span></span>
<span data-ttu-id="9425f-116">指定此 Cmdlet 所取得之延伸的名稱。</span><span class="sxs-lookup"><span data-stu-id="9425f-116">Specifies the name of the extension that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9425f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9425f-117">-ResourceGroupName</span></span>
<span data-ttu-id="9425f-118">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9425f-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9425f-119">-狀態</span><span class="sxs-lookup"><span data-stu-id="9425f-119">-Status</span></span>
<span data-ttu-id="9425f-120">表示此 Cmdlet 只會取得延伸的 [實例] 視圖。</span><span class="sxs-lookup"><span data-stu-id="9425f-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

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

### <span data-ttu-id="9425f-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="9425f-121">-VMName</span></span>
<span data-ttu-id="9425f-122">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9425f-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="9425f-123">這個 Cmdlet 會取得此參數指定之虛擬機器之 VMAccess 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9425f-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="9425f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9425f-124">CommonParameters</span></span>
<span data-ttu-id="9425f-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9425f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9425f-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9425f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9425f-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9425f-127">INPUTS</span></span>

### <span data-ttu-id="9425f-128">所有</span><span class="sxs-lookup"><span data-stu-id="9425f-128">None</span></span>
<span data-ttu-id="9425f-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9425f-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9425f-130">輸出</span><span class="sxs-lookup"><span data-stu-id="9425f-130">OUTPUTS</span></span>

### <span data-ttu-id="9425f-131">VirtualMachineAccessExtensionCoNtext 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="9425f-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="9425f-132">筆記</span><span class="sxs-lookup"><span data-stu-id="9425f-132">NOTES</span></span>

## <span data-ttu-id="9425f-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="9425f-133">RELATED LINKS</span></span>

[<span data-ttu-id="9425f-134">移除-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9425f-134">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="9425f-135">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="9425f-135">Set-AzureRmVMAccessExtension</span></span>](./Set-AzureRmVMAccessExtension.md)

[<span data-ttu-id="9425f-136">AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="9425f-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)


