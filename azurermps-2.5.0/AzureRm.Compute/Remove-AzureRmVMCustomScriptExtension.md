---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: 70715c4bb4c3e5f805f297c8b68def0f5b3a0d6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93801702"
---
# <span data-ttu-id="6801b-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="6801b-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="6801b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6801b-102">SYNOPSIS</span></span>
<span data-ttu-id="6801b-103">從虛擬機器中移除自訂腳本延伸。</span><span class="sxs-lookup"><span data-stu-id="6801b-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6801b-104">句法</span><span class="sxs-lookup"><span data-stu-id="6801b-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6801b-105">說明</span><span class="sxs-lookup"><span data-stu-id="6801b-105">DESCRIPTION</span></span>
<span data-ttu-id="6801b-106">**AzureRmVMCustomScriptExtension** Cmdlet 會從虛擬機器中移除自訂腳本虛擬電腦延伸。</span><span class="sxs-lookup"><span data-stu-id="6801b-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="6801b-107">示例</span><span class="sxs-lookup"><span data-stu-id="6801b-107">EXAMPLES</span></span>

## <span data-ttu-id="6801b-108">參數</span><span class="sxs-lookup"><span data-stu-id="6801b-108">PARAMETERS</span></span>

### <span data-ttu-id="6801b-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6801b-109">-DefaultProfile</span></span>
<span data-ttu-id="6801b-110">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6801b-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6801b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="6801b-111">-Force</span></span>
<span data-ttu-id="6801b-112">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="6801b-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6801b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="6801b-113">-Name</span></span>
<span data-ttu-id="6801b-114">指定此 Cmdlet 移除的自訂腳本副檔名的名稱。</span><span class="sxs-lookup"><span data-stu-id="6801b-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6801b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6801b-115">-ResourceGroupName</span></span>
<span data-ttu-id="6801b-116">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6801b-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6801b-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="6801b-117">-VMName</span></span>
<span data-ttu-id="6801b-118">指定此 Cmdlet 從中移除自訂腳本延伸的虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="6801b-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="6801b-119">-確認</span><span class="sxs-lookup"><span data-stu-id="6801b-119">-Confirm</span></span>
<span data-ttu-id="6801b-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6801b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6801b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6801b-121">-WhatIf</span></span>
<span data-ttu-id="6801b-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6801b-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="6801b-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6801b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6801b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6801b-124">CommonParameters</span></span>
<span data-ttu-id="6801b-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6801b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6801b-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6801b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6801b-127">輸入</span><span class="sxs-lookup"><span data-stu-id="6801b-127">INPUTS</span></span>

### <span data-ttu-id="6801b-128">所有</span><span class="sxs-lookup"><span data-stu-id="6801b-128">None</span></span>
<span data-ttu-id="6801b-129">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6801b-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6801b-130">輸出</span><span class="sxs-lookup"><span data-stu-id="6801b-130">OUTPUTS</span></span>

### <span data-ttu-id="6801b-131">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="6801b-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6801b-132">筆記</span><span class="sxs-lookup"><span data-stu-id="6801b-132">NOTES</span></span>

## <span data-ttu-id="6801b-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="6801b-133">RELATED LINKS</span></span>

[<span data-ttu-id="6801b-134">AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="6801b-134">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="6801b-135">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="6801b-135">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
