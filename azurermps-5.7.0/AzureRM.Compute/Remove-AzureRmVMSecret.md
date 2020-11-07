---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMSecret.md
ms.openlocfilehash: 84f8abc6c298d7c82bef2494086deef3e4130842
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624197"
---
# <span data-ttu-id="6fc45-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="6fc45-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="6fc45-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6fc45-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc45-103">從虛擬電腦物件移除 () 密碼 (s) </span><span class="sxs-lookup"><span data-stu-id="6fc45-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fc45-104">句法</span><span class="sxs-lookup"><span data-stu-id="6fc45-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fc45-105">說明</span><span class="sxs-lookup"><span data-stu-id="6fc45-105">DESCRIPTION</span></span>
<span data-ttu-id="6fc45-106">Remove-AzureRmVMSecret Cmdlet 會從虛擬電腦物件中移除 () 密碼 () s。</span><span class="sxs-lookup"><span data-stu-id="6fc45-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="6fc45-107">示例</span><span class="sxs-lookup"><span data-stu-id="6fc45-107">EXAMPLES</span></span>

### <span data-ttu-id="6fc45-108">範例1</span><span class="sxs-lookup"><span data-stu-id="6fc45-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="6fc45-109">從資源群組 "rg1" 中的虛擬機器 "vm1" 移除所有機密並更新 VM</span><span class="sxs-lookup"><span data-stu-id="6fc45-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="6fc45-110">參數</span><span class="sxs-lookup"><span data-stu-id="6fc45-110">PARAMETERS</span></span>

### <span data-ttu-id="6fc45-111">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6fc45-111">-SourceVaultId</span></span>
<span data-ttu-id="6fc45-112">指定此 Cmdlet 移除之來源電子倉庫 Id 的陣列。</span><span class="sxs-lookup"><span data-stu-id="6fc45-112">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fc45-113">-VM</span><span class="sxs-lookup"><span data-stu-id="6fc45-113">-VM</span></span>
<span data-ttu-id="6fc45-114">指定此 Cmdlet 從中移除 () 機密 (s) 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="6fc45-114">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="6fc45-115">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fc45-115">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6fc45-116">-確認</span><span class="sxs-lookup"><span data-stu-id="6fc45-116">-Confirm</span></span>
<span data-ttu-id="6fc45-117">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6fc45-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fc45-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fc45-118">-WhatIf</span></span>
<span data-ttu-id="6fc45-119">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6fc45-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fc45-120">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6fc45-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fc45-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc45-121">CommonParameters</span></span>
<span data-ttu-id="6fc45-122">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6fc45-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc45-123">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6fc45-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc45-124">輸入</span><span class="sxs-lookup"><span data-stu-id="6fc45-124">INPUTS</span></span>

### <span data-ttu-id="6fc45-125">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6fc45-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6fc45-126">輸出</span><span class="sxs-lookup"><span data-stu-id="6fc45-126">OUTPUTS</span></span>

### <span data-ttu-id="6fc45-127">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6fc45-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6fc45-128">筆記</span><span class="sxs-lookup"><span data-stu-id="6fc45-128">NOTES</span></span>

## <span data-ttu-id="6fc45-129">相關連結</span><span class="sxs-lookup"><span data-stu-id="6fc45-129">RELATED LINKS</span></span>

