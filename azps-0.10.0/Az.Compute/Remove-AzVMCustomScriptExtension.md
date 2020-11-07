---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 8bead12111148d193e0e5dfe880ed3b28c6dcd01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796038"
---
# <span data-ttu-id="66595-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="66595-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="66595-102">摘要</span><span class="sxs-lookup"><span data-stu-id="66595-102">SYNOPSIS</span></span>
<span data-ttu-id="66595-103">從虛擬機器中移除自訂腳本延伸。</span><span class="sxs-lookup"><span data-stu-id="66595-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="66595-104">句法</span><span class="sxs-lookup"><span data-stu-id="66595-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66595-105">說明</span><span class="sxs-lookup"><span data-stu-id="66595-105">DESCRIPTION</span></span>
<span data-ttu-id="66595-106">**AzVMCustomScriptExtension** Cmdlet 會從虛擬機器中移除自訂腳本虛擬電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="66595-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="66595-107">示例</span><span class="sxs-lookup"><span data-stu-id="66595-107">EXAMPLES</span></span>

## <span data-ttu-id="66595-108">參數</span><span class="sxs-lookup"><span data-stu-id="66595-108">PARAMETERS</span></span>

### <span data-ttu-id="66595-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66595-109">-DefaultProfile</span></span>
<span data-ttu-id="66595-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="66595-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66595-111">-Force</span><span class="sxs-lookup"><span data-stu-id="66595-111">-Force</span></span>
<span data-ttu-id="66595-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="66595-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="66595-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="66595-113">-Name</span></span>
<span data-ttu-id="66595-114">指定此 Cmdlet 移除的自訂腳本副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="66595-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="66595-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66595-115">-ResourceGroupName</span></span>
<span data-ttu-id="66595-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="66595-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="66595-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="66595-117">-VMName</span></span>
<span data-ttu-id="66595-118">指定此 Cmdlet 從中移除自訂腳本延伸的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="66595-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="66595-119">-確認</span><span class="sxs-lookup"><span data-stu-id="66595-119">-Confirm</span></span>
<span data-ttu-id="66595-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="66595-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66595-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66595-121">-WhatIf</span></span>
<span data-ttu-id="66595-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="66595-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="66595-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="66595-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66595-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66595-124">CommonParameters</span></span>
<span data-ttu-id="66595-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="66595-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66595-126">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="66595-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66595-127">輸入</span><span class="sxs-lookup"><span data-stu-id="66595-127">INPUTS</span></span>

### <span data-ttu-id="66595-128">所有</span><span class="sxs-lookup"><span data-stu-id="66595-128">None</span></span>
<span data-ttu-id="66595-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="66595-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66595-130">輸出</span><span class="sxs-lookup"><span data-stu-id="66595-130">OUTPUTS</span></span>

### <span data-ttu-id="66595-131">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="66595-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="66595-132">筆記</span><span class="sxs-lookup"><span data-stu-id="66595-132">NOTES</span></span>

## <span data-ttu-id="66595-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="66595-133">RELATED LINKS</span></span>

[<span data-ttu-id="66595-134">AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="66595-134">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="66595-135">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="66595-135">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
