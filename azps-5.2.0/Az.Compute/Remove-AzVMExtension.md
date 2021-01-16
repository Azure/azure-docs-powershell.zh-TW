---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 70495ee657e511aace4babf47959c4bd6841197c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98281096"
---
# <span data-ttu-id="556b0-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="556b0-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="556b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="556b0-102">SYNOPSIS</span></span>
<span data-ttu-id="556b0-103">從虛擬機器移除延伸。</span><span class="sxs-lookup"><span data-stu-id="556b0-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="556b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="556b0-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="556b0-105">說明</span><span class="sxs-lookup"><span data-stu-id="556b0-105">DESCRIPTION</span></span>
<span data-ttu-id="556b0-106">**AzVMExtension** Cmdlet 會從虛擬機器的虛擬機器延伸中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="556b0-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="556b0-107">示例</span><span class="sxs-lookup"><span data-stu-id="556b0-107">EXAMPLES</span></span>

### <span data-ttu-id="556b0-108">範例1：從虛擬機器移除擴充功能</span><span class="sxs-lookup"><span data-stu-id="556b0-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="556b0-109">這個命令會從 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器中移除名為 ContosoTest 的延伸。</span><span class="sxs-lookup"><span data-stu-id="556b0-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="556b0-110">參數</span><span class="sxs-lookup"><span data-stu-id="556b0-110">PARAMETERS</span></span>

### <span data-ttu-id="556b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="556b0-111">-DefaultProfile</span></span>
<span data-ttu-id="556b0-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="556b0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="556b0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="556b0-113">-Force</span></span>
<span data-ttu-id="556b0-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="556b0-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="556b0-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="556b0-115">-Name</span></span>
<span data-ttu-id="556b0-116">指定此 Cmdlet 移除的延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="556b0-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="556b0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="556b0-117">-ResourceGroupName</span></span>
<span data-ttu-id="556b0-118">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="556b0-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="556b0-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="556b0-119">-VMName</span></span>
<span data-ttu-id="556b0-120">指定此 Cmdlet 從中移除延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="556b0-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="556b0-121">-確認</span><span class="sxs-lookup"><span data-stu-id="556b0-121">-Confirm</span></span>
<span data-ttu-id="556b0-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="556b0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="556b0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="556b0-123">-WhatIf</span></span>
<span data-ttu-id="556b0-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="556b0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="556b0-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="556b0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="556b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="556b0-126">CommonParameters</span></span>
<span data-ttu-id="556b0-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="556b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="556b0-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="556b0-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="556b0-129">輸入</span><span class="sxs-lookup"><span data-stu-id="556b0-129">INPUTS</span></span>

### <span data-ttu-id="556b0-130">System.object</span><span class="sxs-lookup"><span data-stu-id="556b0-130">System.String</span></span>

## <span data-ttu-id="556b0-131">輸出</span><span class="sxs-lookup"><span data-stu-id="556b0-131">OUTPUTS</span></span>

### <span data-ttu-id="556b0-132">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="556b0-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="556b0-133">筆記</span><span class="sxs-lookup"><span data-stu-id="556b0-133">NOTES</span></span>

## <span data-ttu-id="556b0-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="556b0-134">RELATED LINKS</span></span>

[<span data-ttu-id="556b0-135">AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="556b0-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="556b0-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="556b0-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


