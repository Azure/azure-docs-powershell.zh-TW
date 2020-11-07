---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 888ba66f1949a687228f5b9f2563c3d810c7cd5f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796053"
---
# <span data-ttu-id="76729-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="76729-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="76729-102">摘要</span><span class="sxs-lookup"><span data-stu-id="76729-102">SYNOPSIS</span></span>
<span data-ttu-id="76729-103">從虛擬機器移除 VMAccess 延伸。</span><span class="sxs-lookup"><span data-stu-id="76729-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="76729-104">句法</span><span class="sxs-lookup"><span data-stu-id="76729-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76729-105">說明</span><span class="sxs-lookup"><span data-stu-id="76729-105">DESCRIPTION</span></span>
<span data-ttu-id="76729-106">**AzVMAccessExtension** Cmdlet 會從虛擬機器中移除虛擬機器存取 (VMAccess) 虛擬電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="76729-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="76729-107">示例</span><span class="sxs-lookup"><span data-stu-id="76729-107">EXAMPLES</span></span>

## <span data-ttu-id="76729-108">參數</span><span class="sxs-lookup"><span data-stu-id="76729-108">PARAMETERS</span></span>

### <span data-ttu-id="76729-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76729-109">-DefaultProfile</span></span>
<span data-ttu-id="76729-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="76729-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76729-111">-Force</span><span class="sxs-lookup"><span data-stu-id="76729-111">-Force</span></span>
<span data-ttu-id="76729-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="76729-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="76729-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="76729-113">-Name</span></span>
<span data-ttu-id="76729-114">指定此 Cmdlet 移除的延伸名稱。</span><span class="sxs-lookup"><span data-stu-id="76729-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="76729-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76729-115">-ResourceGroupName</span></span>
<span data-ttu-id="76729-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="76729-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="76729-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="76729-117">-VMName</span></span>
<span data-ttu-id="76729-118">指定虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="76729-118">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="76729-119">這個 Cmdlet 會移除此參數指定之虛擬機器的 VMAccess。</span><span class="sxs-lookup"><span data-stu-id="76729-119">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="76729-120">-確認</span><span class="sxs-lookup"><span data-stu-id="76729-120">-Confirm</span></span>
<span data-ttu-id="76729-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="76729-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76729-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76729-122">-WhatIf</span></span>
<span data-ttu-id="76729-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="76729-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="76729-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="76729-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76729-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76729-125">CommonParameters</span></span>
<span data-ttu-id="76729-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="76729-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76729-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="76729-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76729-128">輸入</span><span class="sxs-lookup"><span data-stu-id="76729-128">INPUTS</span></span>

### <span data-ttu-id="76729-129">所有</span><span class="sxs-lookup"><span data-stu-id="76729-129">None</span></span>
<span data-ttu-id="76729-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="76729-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76729-131">輸出</span><span class="sxs-lookup"><span data-stu-id="76729-131">OUTPUTS</span></span>

### <span data-ttu-id="76729-132">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="76729-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="76729-133">筆記</span><span class="sxs-lookup"><span data-stu-id="76729-133">NOTES</span></span>

## <span data-ttu-id="76729-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="76729-134">RELATED LINKS</span></span>

[<span data-ttu-id="76729-135">AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="76729-135">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="76729-136">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="76729-136">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="76729-137">移除-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="76729-137">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
