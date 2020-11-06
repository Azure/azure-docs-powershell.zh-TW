---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1e2dc6fe56cfaf182fb0614121ad9511edcfc2fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448736"
---
# <span data-ttu-id="c566e-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="c566e-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="c566e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c566e-102">SYNOPSIS</span></span>
<span data-ttu-id="c566e-103">從虛擬機器中移除自訂腳本延伸。</span><span class="sxs-lookup"><span data-stu-id="c566e-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c566e-104">句法</span><span class="sxs-lookup"><span data-stu-id="c566e-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c566e-105">說明</span><span class="sxs-lookup"><span data-stu-id="c566e-105">DESCRIPTION</span></span>
<span data-ttu-id="c566e-106">**AzureRmVMCustomScriptExtension** Cmdlet 會從虛擬機器中移除自訂腳本虛擬電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="c566e-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="c566e-107">示例</span><span class="sxs-lookup"><span data-stu-id="c566e-107">EXAMPLES</span></span>

## <span data-ttu-id="c566e-108">參數</span><span class="sxs-lookup"><span data-stu-id="c566e-108">PARAMETERS</span></span>

### <span data-ttu-id="c566e-109">-Force</span><span class="sxs-lookup"><span data-stu-id="c566e-109">-Force</span></span>
<span data-ttu-id="c566e-110">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="c566e-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c566e-111">-名稱</span><span class="sxs-lookup"><span data-stu-id="c566e-111">-Name</span></span>
<span data-ttu-id="c566e-112">指定此 Cmdlet 移除的自訂腳本副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="c566e-112">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="c566e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c566e-113">-ResourceGroupName</span></span>
<span data-ttu-id="c566e-114">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c566e-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="c566e-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="c566e-115">-VMName</span></span>
<span data-ttu-id="c566e-116">指定此 Cmdlet 從中移除自訂腳本延伸的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="c566e-116">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="c566e-117">-確認</span><span class="sxs-lookup"><span data-stu-id="c566e-117">-Confirm</span></span>
<span data-ttu-id="c566e-118">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="c566e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c566e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c566e-119">-WhatIf</span></span>
<span data-ttu-id="c566e-120">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c566e-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="c566e-121">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c566e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c566e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c566e-122">CommonParameters</span></span>
<span data-ttu-id="c566e-123">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c566e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c566e-124">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c566e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c566e-125">輸入</span><span class="sxs-lookup"><span data-stu-id="c566e-125">INPUTS</span></span>

### <span data-ttu-id="c566e-126">所有</span><span class="sxs-lookup"><span data-stu-id="c566e-126">None</span></span>
<span data-ttu-id="c566e-127">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="c566e-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c566e-128">輸出</span><span class="sxs-lookup"><span data-stu-id="c566e-128">OUTPUTS</span></span>

## <span data-ttu-id="c566e-129">筆記</span><span class="sxs-lookup"><span data-stu-id="c566e-129">NOTES</span></span>

## <span data-ttu-id="c566e-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="c566e-130">RELATED LINKS</span></span>

[<span data-ttu-id="c566e-131">AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="c566e-131">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="c566e-132">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="c566e-132">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
