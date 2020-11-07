---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmsecret
schema: 2.0.0
ms.openlocfilehash: 8d3c10be9d4a3f165932271838f6af8fdbf18e4d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801389"
---
# <span data-ttu-id="49582-101">Remove-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="49582-101">Remove-AzureRmVMSecret</span></span>

## <span data-ttu-id="49582-102">摘要</span><span class="sxs-lookup"><span data-stu-id="49582-102">SYNOPSIS</span></span>
<span data-ttu-id="49582-103">從虛擬電腦物件移除 () 密碼 (s) </span><span class="sxs-lookup"><span data-stu-id="49582-103">Removes (a) secret(s) from a virtual machine object</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49582-104">句法</span><span class="sxs-lookup"><span data-stu-id="49582-104">SYNTAX</span></span>

```
Remove-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49582-105">說明</span><span class="sxs-lookup"><span data-stu-id="49582-105">DESCRIPTION</span></span>
<span data-ttu-id="49582-106">Remove-AzureRmVMSecret Cmdlet 會從虛擬電腦物件中移除 () 密碼 () s。</span><span class="sxs-lookup"><span data-stu-id="49582-106">The Remove-AzureRmVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="49582-107">示例</span><span class="sxs-lookup"><span data-stu-id="49582-107">EXAMPLES</span></span>

### <span data-ttu-id="49582-108">範例1</span><span class="sxs-lookup"><span data-stu-id="49582-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzureRmVMSecret | Update-AzureRmVM
```

<span data-ttu-id="49582-109">從資源群組 "rg1" 中的虛擬機器 "vm1" 移除所有機密並更新 VM</span><span class="sxs-lookup"><span data-stu-id="49582-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="49582-110">參數</span><span class="sxs-lookup"><span data-stu-id="49582-110">PARAMETERS</span></span>

### <span data-ttu-id="49582-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49582-111">-DefaultProfile</span></span>
<span data-ttu-id="49582-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="49582-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49582-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="49582-113">-SourceVaultId</span></span>
<span data-ttu-id="49582-114">指定此 Cmdlet 移除之來源電子倉庫 Id 的陣列。</span><span class="sxs-lookup"><span data-stu-id="49582-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="49582-115">-VM</span><span class="sxs-lookup"><span data-stu-id="49582-115">-VM</span></span>
<span data-ttu-id="49582-116">指定此 Cmdlet 從中移除 () 機密 (s) 的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="49582-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="49582-117">若要取得虛擬機器物件，請使用 Get-AzureRmVM Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49582-117">To obtain a virtual machine object, use the Get-AzureRmVM cmdlet.</span></span>

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

### <span data-ttu-id="49582-118">-確認</span><span class="sxs-lookup"><span data-stu-id="49582-118">-Confirm</span></span>
<span data-ttu-id="49582-119">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="49582-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49582-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49582-120">-WhatIf</span></span>
<span data-ttu-id="49582-121">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="49582-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49582-122">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="49582-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49582-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49582-123">CommonParameters</span></span>
<span data-ttu-id="49582-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="49582-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49582-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="49582-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49582-126">輸入</span><span class="sxs-lookup"><span data-stu-id="49582-126">INPUTS</span></span>

### <span data-ttu-id="49582-127">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="49582-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="49582-128">輸出</span><span class="sxs-lookup"><span data-stu-id="49582-128">OUTPUTS</span></span>

### <span data-ttu-id="49582-129">PSVirtualMachine 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="49582-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="49582-130">筆記</span><span class="sxs-lookup"><span data-stu-id="49582-130">NOTES</span></span>

## <span data-ttu-id="49582-131">相關連結</span><span class="sxs-lookup"><span data-stu-id="49582-131">RELATED LINKS</span></span>

