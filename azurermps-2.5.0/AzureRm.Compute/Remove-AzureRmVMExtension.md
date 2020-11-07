---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmextension
schema: 2.0.0
ms.openlocfilehash: 835413728b22dd8bbb80d472eed71e0f4185db89
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801393"
---
# <span data-ttu-id="db386-101">Remove-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="db386-101">Remove-AzureRmVMExtension</span></span>

## <span data-ttu-id="db386-102">摘要</span><span class="sxs-lookup"><span data-stu-id="db386-102">SYNOPSIS</span></span>
<span data-ttu-id="db386-103">從虛擬機器移除延伸。</span><span class="sxs-lookup"><span data-stu-id="db386-103">Removes an extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db386-104">句法</span><span class="sxs-lookup"><span data-stu-id="db386-104">SYNTAX</span></span>

```
Remove-AzureRmVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db386-105">說明</span><span class="sxs-lookup"><span data-stu-id="db386-105">DESCRIPTION</span></span>
<span data-ttu-id="db386-106">**AzureRmVMExtension** Cmdlet 會從虛擬機器的虛擬機器延伸中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="db386-106">The **Remove-AzureRmVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="db386-107">示例</span><span class="sxs-lookup"><span data-stu-id="db386-107">EXAMPLES</span></span>

### <span data-ttu-id="db386-108">範例1：從虛擬機器移除擴充功能</span><span class="sxs-lookup"><span data-stu-id="db386-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="db386-109">這個命令會從 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器中移除名為 ContosoTest 的延伸。</span><span class="sxs-lookup"><span data-stu-id="db386-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="db386-110">參數</span><span class="sxs-lookup"><span data-stu-id="db386-110">PARAMETERS</span></span>

### <span data-ttu-id="db386-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db386-111">-DefaultProfile</span></span>
<span data-ttu-id="db386-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="db386-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db386-113">-Force</span><span class="sxs-lookup"><span data-stu-id="db386-113">-Force</span></span>
<span data-ttu-id="db386-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="db386-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="db386-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="db386-115">-Name</span></span>
<span data-ttu-id="db386-116">指定此 Cmdlet 移除的延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="db386-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="db386-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db386-117">-ResourceGroupName</span></span>
<span data-ttu-id="db386-118">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="db386-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="db386-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="db386-119">-VMName</span></span>
<span data-ttu-id="db386-120">指定此 Cmdlet 從中移除延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="db386-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="db386-121">-確認</span><span class="sxs-lookup"><span data-stu-id="db386-121">-Confirm</span></span>
<span data-ttu-id="db386-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="db386-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db386-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db386-123">-WhatIf</span></span>
<span data-ttu-id="db386-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="db386-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="db386-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="db386-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db386-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db386-126">CommonParameters</span></span>
<span data-ttu-id="db386-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="db386-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db386-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="db386-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db386-129">輸入</span><span class="sxs-lookup"><span data-stu-id="db386-129">INPUTS</span></span>

### <span data-ttu-id="db386-130">所有</span><span class="sxs-lookup"><span data-stu-id="db386-130">None</span></span>
<span data-ttu-id="db386-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="db386-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db386-132">輸出</span><span class="sxs-lookup"><span data-stu-id="db386-132">OUTPUTS</span></span>

### <span data-ttu-id="db386-133">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="db386-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="db386-134">筆記</span><span class="sxs-lookup"><span data-stu-id="db386-134">NOTES</span></span>

## <span data-ttu-id="db386-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="db386-135">RELATED LINKS</span></span>

[<span data-ttu-id="db386-136">AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="db386-136">Get-AzureRmVMExtension</span></span>](./Get-AzureRmVMExtension.md)

[<span data-ttu-id="db386-137">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="db386-137">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)


