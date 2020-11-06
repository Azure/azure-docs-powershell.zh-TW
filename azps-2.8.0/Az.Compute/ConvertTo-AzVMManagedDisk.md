---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/convertto-azvmmanageddisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/ConvertTo-AzVMManagedDisk.md
ms.openlocfilehash: 71cbd99ccd34341eb996cd4015f9e8c39d9c7fa2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93613437"
---
# <span data-ttu-id="7c15b-101">ConvertTo-AzVMManagedDisk</span><span class="sxs-lookup"><span data-stu-id="7c15b-101">ConvertTo-AzVMManagedDisk</span></span>

## <span data-ttu-id="7c15b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7c15b-102">SYNOPSIS</span></span>
<span data-ttu-id="7c15b-103">使用受管理的磁片將包含 blob 磁片的虛擬機器轉換成虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7c15b-103">Converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>

## <span data-ttu-id="7c15b-104">句法</span><span class="sxs-lookup"><span data-stu-id="7c15b-104">SYNTAX</span></span>

```
ConvertTo-AzVMManagedDisk [-ResourceGroupName] <String> [-VMName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c15b-105">說明</span><span class="sxs-lookup"><span data-stu-id="7c15b-105">DESCRIPTION</span></span>
<span data-ttu-id="7c15b-106">**ConvertTo-AzVMManagedDisk** Cmdlet 會將包含 blob 磁片的虛擬機器轉換成具有受管理磁片的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7c15b-106">The **ConvertTo-AzVMManagedDisk** cmdlet converts a virtual machine with blob-based disks to a virtual machine with managed disks.</span></span>
<span data-ttu-id="7c15b-107">必須先停止解除配置虛擬機器，然後才能執行此作業。</span><span class="sxs-lookup"><span data-stu-id="7c15b-107">The virtual machine must be stop-deallocated before invoking this operation.</span></span>

## <span data-ttu-id="7c15b-108">示例</span><span class="sxs-lookup"><span data-stu-id="7c15b-108">EXAMPLES</span></span>

### <span data-ttu-id="7c15b-109">範例1</span><span class="sxs-lookup"><span data-stu-id="7c15b-109">Example 1</span></span>
```
PS C:\> ConvertTo-AzVMManagedDisk -ResourceGroupName 'ResourceGroup01' -VMName 'VM01'
```

<span data-ttu-id="7c15b-110">這個命令會將資源群組 "ResourceGroup01" 中名為 "VM01" 的虛擬機器 blob 磁片轉換成受管理的磁片。</span><span class="sxs-lookup"><span data-stu-id="7c15b-110">This command converts the blob-based disks of the virtual machine named 'VM01' in the resource group 'ResourceGroup01' to managed disks.</span></span>

## <span data-ttu-id="7c15b-111">參數</span><span class="sxs-lookup"><span data-stu-id="7c15b-111">PARAMETERS</span></span>

### <span data-ttu-id="7c15b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c15b-112">-AsJob</span></span>
<span data-ttu-id="7c15b-113">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="7c15b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c15b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c15b-114">-DefaultProfile</span></span>
<span data-ttu-id="7c15b-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7c15b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c15b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c15b-116">-ResourceGroupName</span></span>
<span data-ttu-id="7c15b-117">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c15b-117">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="7c15b-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="7c15b-118">-VMName</span></span>
<span data-ttu-id="7c15b-119">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7c15b-119">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="7c15b-120">-確認</span><span class="sxs-lookup"><span data-stu-id="7c15b-120">-Confirm</span></span>
<span data-ttu-id="7c15b-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7c15b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c15b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c15b-122">-WhatIf</span></span>
<span data-ttu-id="7c15b-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7c15b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c15b-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7c15b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c15b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c15b-125">CommonParameters</span></span>
<span data-ttu-id="7c15b-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7c15b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c15b-127">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7c15b-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c15b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="7c15b-128">INPUTS</span></span>

### <span data-ttu-id="7c15b-129">System.object</span><span class="sxs-lookup"><span data-stu-id="7c15b-129">System.String</span></span>

## <span data-ttu-id="7c15b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="7c15b-130">OUTPUTS</span></span>

### <span data-ttu-id="7c15b-131">PSOperationStatusResponse 中的 [計算] 命令。</span><span class="sxs-lookup"><span data-stu-id="7c15b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7c15b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="7c15b-132">NOTES</span></span>

## <span data-ttu-id="7c15b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="7c15b-133">RELATED LINKS</span></span>
