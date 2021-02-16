---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/invoke-azvmreimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Invoke-AzVMReimage.md
ms.openlocfilehash: 508b945bfc9661ea203d7e1e49ccf9d3e8d3bc25
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127870"
---
# <span data-ttu-id="41614-101">Invoke-AzVMReimage</span><span class="sxs-lookup"><span data-stu-id="41614-101">Invoke-AzVMReimage</span></span>

## <span data-ttu-id="41614-102">摘要</span><span class="sxs-lookup"><span data-stu-id="41614-102">SYNOPSIS</span></span>
<span data-ttu-id="41614-103">重新鏡像 Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="41614-103">Reimage an Azure virtual machine.</span></span>

## <span data-ttu-id="41614-104">句法</span><span class="sxs-lookup"><span data-stu-id="41614-104">SYNTAX</span></span>

```
Invoke-AzVMReimage [-ResourceGroupName] <String> [-VMName] <String> [-TempDisk] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41614-105">說明</span><span class="sxs-lookup"><span data-stu-id="41614-105">DESCRIPTION</span></span>
<span data-ttu-id="41614-106">**AzVMReimage** Cmdlet reimages Azure 虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="41614-106">The **Invoke-AzVMReimage** cmdlet reimages an Azure virtual machine.</span></span>

## <span data-ttu-id="41614-107">示例</span><span class="sxs-lookup"><span data-stu-id="41614-107">EXAMPLES</span></span>

### <span data-ttu-id="41614-108">範例1</span><span class="sxs-lookup"><span data-stu-id="41614-108">Example 1</span></span>
```powershell
PS C:\> Invoke-AzVMReimage -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="41614-109">此命令會在 ResourceGroup11 中 reimages 名為 VirtualMachine07 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="41614-109">This command reimages the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="41614-110">參數</span><span class="sxs-lookup"><span data-stu-id="41614-110">PARAMETERS</span></span>

### <span data-ttu-id="41614-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41614-111">-AsJob</span></span>
<span data-ttu-id="41614-112">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="41614-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41614-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41614-113">-DefaultProfile</span></span>
<span data-ttu-id="41614-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="41614-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41614-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41614-115">-ResourceGroupName</span></span>
<span data-ttu-id="41614-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="41614-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="41614-117">-TempDisk</span><span class="sxs-lookup"><span data-stu-id="41614-117">-TempDisk</span></span>
<span data-ttu-id="41614-118">指定是否要重新鏡像 temp 磁片。</span><span class="sxs-lookup"><span data-stu-id="41614-118">Specifies whether to reimage temp disk.</span></span>

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

### <span data-ttu-id="41614-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="41614-119">-VMName</span></span>
<span data-ttu-id="41614-120">虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="41614-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41614-121">-確認</span><span class="sxs-lookup"><span data-stu-id="41614-121">-Confirm</span></span>
<span data-ttu-id="41614-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="41614-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41614-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41614-123">-WhatIf</span></span>
<span data-ttu-id="41614-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="41614-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41614-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="41614-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41614-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41614-126">CommonParameters</span></span>
<span data-ttu-id="41614-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="41614-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41614-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="41614-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41614-129">輸入</span><span class="sxs-lookup"><span data-stu-id="41614-129">INPUTS</span></span>

### <span data-ttu-id="41614-130">System.object</span><span class="sxs-lookup"><span data-stu-id="41614-130">System.String</span></span>

## <span data-ttu-id="41614-131">輸出</span><span class="sxs-lookup"><span data-stu-id="41614-131">OUTPUTS</span></span>

### <span data-ttu-id="41614-132">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="41614-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="41614-133">筆記</span><span class="sxs-lookup"><span data-stu-id="41614-133">NOTES</span></span>

## <span data-ttu-id="41614-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="41614-134">RELATED LINKS</span></span>
