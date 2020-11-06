---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: 9f9b8f28fd3b2597dede1b9fe50780b2c5e43abb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622721"
---
# <span data-ttu-id="f1335-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="f1335-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="f1335-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f1335-102">SYNOPSIS</span></span>
<span data-ttu-id="f1335-103">從虛擬電腦物件移除 () 密碼 (s) </span><span class="sxs-lookup"><span data-stu-id="f1335-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="f1335-104">句法</span><span class="sxs-lookup"><span data-stu-id="f1335-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1335-105">說明</span><span class="sxs-lookup"><span data-stu-id="f1335-105">DESCRIPTION</span></span>
<span data-ttu-id="f1335-106">Remove-AzVMSecret Cmdlet 會從虛擬電腦物件中移除 () 密碼 () s。</span><span class="sxs-lookup"><span data-stu-id="f1335-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="f1335-107">示例</span><span class="sxs-lookup"><span data-stu-id="f1335-107">EXAMPLES</span></span>

### <span data-ttu-id="f1335-108">範例1</span><span class="sxs-lookup"><span data-stu-id="f1335-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="f1335-109">從資源群組 "rg1" 中的虛擬機器 "vm1" 移除所有機密並更新 VM</span><span class="sxs-lookup"><span data-stu-id="f1335-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="f1335-110">參數</span><span class="sxs-lookup"><span data-stu-id="f1335-110">PARAMETERS</span></span>

### <span data-ttu-id="f1335-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1335-111">-DefaultProfile</span></span>
<span data-ttu-id="f1335-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f1335-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1335-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="f1335-113">-SourceVaultId</span></span>
<span data-ttu-id="f1335-114">指定此 Cmdlet 移除之來源電子倉庫 Id 的陣列。</span><span class="sxs-lookup"><span data-stu-id="f1335-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1335-115">-VM</span><span class="sxs-lookup"><span data-stu-id="f1335-115">-VM</span></span>
<span data-ttu-id="f1335-116">指定此 Cmdlet 從中移除 () 機密 (s) 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="f1335-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="f1335-117">若要取得虛擬機器物件，請使用 Get-AzVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1335-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f1335-118">-確認</span><span class="sxs-lookup"><span data-stu-id="f1335-118">-Confirm</span></span>
<span data-ttu-id="f1335-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f1335-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1335-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1335-120">-WhatIf</span></span>
<span data-ttu-id="f1335-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f1335-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1335-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f1335-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1335-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1335-123">CommonParameters</span></span>
<span data-ttu-id="f1335-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f1335-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1335-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f1335-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1335-126">輸入</span><span class="sxs-lookup"><span data-stu-id="f1335-126">INPUTS</span></span>

### <span data-ttu-id="f1335-127">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="f1335-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f1335-128">輸出</span><span class="sxs-lookup"><span data-stu-id="f1335-128">OUTPUTS</span></span>

### <span data-ttu-id="f1335-129">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="f1335-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="f1335-130">筆記</span><span class="sxs-lookup"><span data-stu-id="f1335-130">NOTES</span></span>

## <span data-ttu-id="f1335-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="f1335-131">RELATED LINKS</span></span>
