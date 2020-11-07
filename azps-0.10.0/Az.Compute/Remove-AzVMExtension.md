---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: e1b400f2fe3ff973c586fbde9f4003732ad8c6cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796017"
---
# <span data-ttu-id="2c655-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="2c655-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="2c655-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2c655-102">SYNOPSIS</span></span>
<span data-ttu-id="2c655-103">從虛擬機器移除延伸。</span><span class="sxs-lookup"><span data-stu-id="2c655-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="2c655-104">句法</span><span class="sxs-lookup"><span data-stu-id="2c655-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c655-105">說明</span><span class="sxs-lookup"><span data-stu-id="2c655-105">DESCRIPTION</span></span>
<span data-ttu-id="2c655-106">**AzVMExtension** Cmdlet 會從虛擬機器的虛擬機器延伸中移除延伸。</span><span class="sxs-lookup"><span data-stu-id="2c655-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="2c655-107">示例</span><span class="sxs-lookup"><span data-stu-id="2c655-107">EXAMPLES</span></span>

### <span data-ttu-id="2c655-108">範例1：從虛擬機器移除擴充功能</span><span class="sxs-lookup"><span data-stu-id="2c655-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="2c655-109">這個命令會從 ResourceGroup11 中名為 VirtualMachine22 的虛擬機器中移除名為 ContosoTest 的延伸。</span><span class="sxs-lookup"><span data-stu-id="2c655-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="2c655-110">參數</span><span class="sxs-lookup"><span data-stu-id="2c655-110">PARAMETERS</span></span>

### <span data-ttu-id="2c655-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c655-111">-DefaultProfile</span></span>
<span data-ttu-id="2c655-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="2c655-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c655-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2c655-113">-Force</span></span>
<span data-ttu-id="2c655-114">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="2c655-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c655-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="2c655-115">-Name</span></span>
<span data-ttu-id="2c655-116">指定此 Cmdlet 移除的延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="2c655-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2c655-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c655-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c655-118">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2c655-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2c655-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="2c655-119">-VMName</span></span>
<span data-ttu-id="2c655-120">指定此 Cmdlet 從中移除延伸的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="2c655-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="2c655-121">-確認</span><span class="sxs-lookup"><span data-stu-id="2c655-121">-Confirm</span></span>
<span data-ttu-id="2c655-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2c655-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c655-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c655-123">-WhatIf</span></span>
<span data-ttu-id="2c655-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2c655-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2c655-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2c655-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c655-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c655-126">CommonParameters</span></span>
<span data-ttu-id="2c655-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2c655-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c655-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2c655-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c655-129">輸入</span><span class="sxs-lookup"><span data-stu-id="2c655-129">INPUTS</span></span>

### <span data-ttu-id="2c655-130">所有</span><span class="sxs-lookup"><span data-stu-id="2c655-130">None</span></span>
<span data-ttu-id="2c655-131">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="2c655-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2c655-132">輸出</span><span class="sxs-lookup"><span data-stu-id="2c655-132">OUTPUTS</span></span>

### <span data-ttu-id="2c655-133">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="2c655-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2c655-134">筆記</span><span class="sxs-lookup"><span data-stu-id="2c655-134">NOTES</span></span>

## <span data-ttu-id="2c655-135">相關連結</span><span class="sxs-lookup"><span data-stu-id="2c655-135">RELATED LINKS</span></span>

[<span data-ttu-id="2c655-136">AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="2c655-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="2c655-137">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="2c655-137">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


