---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: ee0762dfa78a5bd863ede7b56cb746c2c8cab3be
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93626127"
---
# <span data-ttu-id="9e0d6-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9e0d6-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="9e0d6-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e0d6-102">SYNOPSIS</span></span>
<span data-ttu-id="9e0d6-103">從虛擬機器中移除自訂腳本延伸。</span><span class="sxs-lookup"><span data-stu-id="9e0d6-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e0d6-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e0d6-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e0d6-105">說明</span><span class="sxs-lookup"><span data-stu-id="9e0d6-105">DESCRIPTION</span></span>
<span data-ttu-id="9e0d6-106">**AzureRmVMCustomScriptExtension** Cmdlet 會從虛擬機器中移除自訂腳本虛擬電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="9e0d6-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="9e0d6-107">示例</span><span class="sxs-lookup"><span data-stu-id="9e0d6-107">EXAMPLES</span></span>

## <span data-ttu-id="9e0d6-108">參數</span><span class="sxs-lookup"><span data-stu-id="9e0d6-108">PARAMETERS</span></span>

### <span data-ttu-id="9e0d6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e0d6-109">-DefaultProfile</span></span>
<span data-ttu-id="9e0d6-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e0d6-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e0d6-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9e0d6-111">-Force</span></span>
<span data-ttu-id="9e0d6-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="9e0d6-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e0d6-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e0d6-113">-Name</span></span>
<span data-ttu-id="9e0d6-114">指定此 Cmdlet 移除的自訂腳本副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e0d6-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0d6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e0d6-115">-ResourceGroupName</span></span>
<span data-ttu-id="9e0d6-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e0d6-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9e0d6-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="9e0d6-117">-VMName</span></span>
<span data-ttu-id="9e0d6-118">指定此 Cmdlet 從中移除自訂腳本延伸的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e0d6-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e0d6-119">-確認</span><span class="sxs-lookup"><span data-stu-id="9e0d6-119">-Confirm</span></span>
<span data-ttu-id="9e0d6-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e0d6-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e0d6-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e0d6-121">-WhatIf</span></span>
<span data-ttu-id="9e0d6-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e0d6-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e0d6-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e0d6-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e0d6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e0d6-124">CommonParameters</span></span>
<span data-ttu-id="9e0d6-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e0d6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e0d6-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e0d6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e0d6-127">輸入</span><span class="sxs-lookup"><span data-stu-id="9e0d6-127">INPUTS</span></span>

### <span data-ttu-id="9e0d6-128">System.object</span><span class="sxs-lookup"><span data-stu-id="9e0d6-128">System.String</span></span>

## <span data-ttu-id="9e0d6-129">輸出</span><span class="sxs-lookup"><span data-stu-id="9e0d6-129">OUTPUTS</span></span>

### <span data-ttu-id="9e0d6-130">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="9e0d6-130">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9e0d6-131">筆記</span><span class="sxs-lookup"><span data-stu-id="9e0d6-131">NOTES</span></span>

## <span data-ttu-id="9e0d6-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e0d6-132">RELATED LINKS</span></span>

[<span data-ttu-id="9e0d6-133">AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9e0d6-133">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="9e0d6-134">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="9e0d6-134">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
