---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMExtension.md
ms.openlocfilehash: da05148a0e27ba553f80fa18b44cb45decf9f1df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93444724"
---
# <span data-ttu-id="e5f88-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="e5f88-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="e5f88-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e5f88-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f88-103">從虛擬機器移除延伸。</span><span class="sxs-lookup"><span data-stu-id="e5f88-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5f88-104">句法</span><span class="sxs-lookup"><span data-stu-id="e5f88-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5f88-105">說明</span><span class="sxs-lookup"><span data-stu-id="e5f88-105">DESCRIPTION</span></span>
<span data-ttu-id="e5f88-106">**AzureRmVMExtension** Cmdlet 會從虛擬機器的虛擬機器延伸中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="e5f88-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="e5f88-107">示例</span><span class="sxs-lookup"><span data-stu-id="e5f88-107">EXAMPLES</span></span>

### <span data-ttu-id="e5f88-108">範例1：從虛擬機器移除擴充功能</span><span class="sxs-lookup"><span data-stu-id="e5f88-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="e5f88-109">這個命令會從 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器中移除名為 ContosoTest 的延伸。</span><span class="sxs-lookup"><span data-stu-id="e5f88-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="e5f88-110">參數</span><span class="sxs-lookup"><span data-stu-id="e5f88-110">PARAMETERS</span></span>

### <span data-ttu-id="e5f88-111">-Force</span><span class="sxs-lookup"><span data-stu-id="e5f88-111">-Force</span></span>
<span data-ttu-id="e5f88-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="e5f88-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f88-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="e5f88-113">-Name</span></span>
<span data-ttu-id="e5f88-114">指定此 Cmdlet 移除的延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="e5f88-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e5f88-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5f88-115">-ResourceGroupName</span></span>
<span data-ttu-id="e5f88-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="e5f88-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e5f88-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="e5f88-117">-VMName</span></span>
<span data-ttu-id="e5f88-118">指定此 Cmdlet 從中移除延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="e5f88-118">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="e5f88-119">-確認</span><span class="sxs-lookup"><span data-stu-id="e5f88-119">-Confirm</span></span>
<span data-ttu-id="e5f88-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="e5f88-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f88-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f88-121">-WhatIf</span></span>
<span data-ttu-id="e5f88-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="e5f88-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="e5f88-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="e5f88-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f88-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f88-124">CommonParameters</span></span>
<span data-ttu-id="e5f88-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e5f88-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f88-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e5f88-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f88-127">輸入</span><span class="sxs-lookup"><span data-stu-id="e5f88-127">INPUTS</span></span>

### <span data-ttu-id="e5f88-128">所有</span><span class="sxs-lookup"><span data-stu-id="e5f88-128">None</span></span>
<span data-ttu-id="e5f88-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e5f88-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e5f88-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e5f88-130">OUTPUTS</span></span>

## <span data-ttu-id="e5f88-131">筆記</span><span class="sxs-lookup"><span data-stu-id="e5f88-131">NOTES</span></span>

## <span data-ttu-id="e5f88-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="e5f88-132">RELATED LINKS</span></span>

[<span data-ttu-id="e5f88-133">AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="e5f88-133">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="e5f88-134">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="e5f88-134">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


