---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: cc813b4d6b3c5efbd1c54c25b5e198c5b0ce94e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910273"
---
# <span data-ttu-id="aecbc-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="aecbc-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="aecbc-102">簡介</span><span class="sxs-lookup"><span data-stu-id="aecbc-102">SYNOPSIS</span></span>
<span data-ttu-id="aecbc-103">移除虛擬機器的擴充功能。</span><span class="sxs-lookup"><span data-stu-id="aecbc-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="aecbc-104">語法</span><span class="sxs-lookup"><span data-stu-id="aecbc-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aecbc-105">描述</span><span class="sxs-lookup"><span data-stu-id="aecbc-105">DESCRIPTION</span></span>
<span data-ttu-id="aecbc-106">**Remove-Az VIRTUALExtension** Cmdlet 會從虛擬機器的虛擬機器擴充功能移除擴充功能。</span><span class="sxs-lookup"><span data-stu-id="aecbc-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="aecbc-107">例子</span><span class="sxs-lookup"><span data-stu-id="aecbc-107">EXAMPLES</span></span>

### <span data-ttu-id="aecbc-108">範例 1：從虛擬機器移除擴充功能</span><span class="sxs-lookup"><span data-stu-id="aecbc-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="aecbc-109">此命令會從 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器移除名為 ContosoTest 的副檔名。</span><span class="sxs-lookup"><span data-stu-id="aecbc-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="aecbc-110">參數</span><span class="sxs-lookup"><span data-stu-id="aecbc-110">PARAMETERS</span></span>

### <span data-ttu-id="aecbc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aecbc-111">-DefaultProfile</span></span>
<span data-ttu-id="aecbc-112">用於與 azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="aecbc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aecbc-113">-強制</span><span class="sxs-lookup"><span data-stu-id="aecbc-113">-Force</span></span>
<span data-ttu-id="aecbc-114">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="aecbc-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aecbc-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="aecbc-115">-Name</span></span>
<span data-ttu-id="aecbc-116">指定此 Cmdlet 移除的副檔名。</span><span class="sxs-lookup"><span data-stu-id="aecbc-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="aecbc-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aecbc-117">-ResourceGroupName</span></span>
<span data-ttu-id="aecbc-118">指定虛擬機器的資源組名。</span><span class="sxs-lookup"><span data-stu-id="aecbc-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="aecbc-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="aecbc-119">-VMName</span></span>
<span data-ttu-id="aecbc-120">指定此 Cmdlet 移除副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="aecbc-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="aecbc-121">-確認</span><span class="sxs-lookup"><span data-stu-id="aecbc-121">-Confirm</span></span>
<span data-ttu-id="aecbc-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="aecbc-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aecbc-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aecbc-123">-WhatIf</span></span>
<span data-ttu-id="aecbc-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aecbc-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aecbc-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aecbc-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aecbc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aecbc-126">CommonParameters</span></span>
<span data-ttu-id="aecbc-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="aecbc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aecbc-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aecbc-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aecbc-129">輸入</span><span class="sxs-lookup"><span data-stu-id="aecbc-129">INPUTS</span></span>

### <span data-ttu-id="aecbc-130">System.String</span><span class="sxs-lookup"><span data-stu-id="aecbc-130">System.String</span></span>

## <span data-ttu-id="aecbc-131">輸出</span><span class="sxs-lookup"><span data-stu-id="aecbc-131">OUTPUTS</span></span>

### <span data-ttu-id="aecbc-132">Microsoft.Azure.Commands.Compute.models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="aecbc-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="aecbc-133">筆記</span><span class="sxs-lookup"><span data-stu-id="aecbc-133">NOTES</span></span>

## <span data-ttu-id="aecbc-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="aecbc-134">RELATED LINKS</span></span>

[<span data-ttu-id="aecbc-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="aecbc-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="aecbc-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="aecbc-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


