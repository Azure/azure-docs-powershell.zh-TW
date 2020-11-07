---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 69eff38068c379dadc4f3a061cfba4f9cb6539e3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93796021"
---
# <span data-ttu-id="9e43b-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9e43b-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="9e43b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e43b-102">SYNOPSIS</span></span>
<span data-ttu-id="9e43b-103">從資源群組中的虛擬機器移除 DSC 延伸處理常式。</span><span class="sxs-lookup"><span data-stu-id="9e43b-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="9e43b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e43b-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e43b-105">說明</span><span class="sxs-lookup"><span data-stu-id="9e43b-105">DESCRIPTION</span></span>
<span data-ttu-id="9e43b-106">**AzVMDscExtension** Cmdlet 會從資源群組中的虛擬機器 (DSC) 延伸處理常式，移除所需的狀態設定。</span><span class="sxs-lookup"><span data-stu-id="9e43b-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="9e43b-107">示例</span><span class="sxs-lookup"><span data-stu-id="9e43b-107">EXAMPLES</span></span>

### <span data-ttu-id="9e43b-108">範例1：移除 DSC 副檔名</span><span class="sxs-lookup"><span data-stu-id="9e43b-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="9e43b-109">這個命令會移除名為 VM07 的虛擬機器上名為 DSC 的延伸。</span><span class="sxs-lookup"><span data-stu-id="9e43b-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="9e43b-110">參數</span><span class="sxs-lookup"><span data-stu-id="9e43b-110">PARAMETERS</span></span>

### <span data-ttu-id="9e43b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e43b-111">-DefaultProfile</span></span>
<span data-ttu-id="9e43b-112">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e43b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e43b-113">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e43b-113">-Name</span></span>
<span data-ttu-id="9e43b-114">指定此 Cmdlet 移除的 DSC 副檔名名稱。</span><span class="sxs-lookup"><span data-stu-id="9e43b-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="9e43b-115">Set-AzVMDscExtension Cmdlet 會將此名稱設定為 AzVMDscExtension，這是 **Remove-** 所使用的預設值。</span><span class="sxs-lookup"><span data-stu-id="9e43b-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e43b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e43b-116">-ResourceGroupName</span></span>
<span data-ttu-id="9e43b-117">指定虛擬機器之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9e43b-117">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9e43b-118">-VMName</span><span class="sxs-lookup"><span data-stu-id="9e43b-118">-VMName</span></span>
<span data-ttu-id="9e43b-119">指定此 Cmdlet 從中移除 DSC 副檔名的虛擬機器名稱。</span><span class="sxs-lookup"><span data-stu-id="9e43b-119">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e43b-120">-確認</span><span class="sxs-lookup"><span data-stu-id="9e43b-120">-Confirm</span></span>
<span data-ttu-id="9e43b-121">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e43b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e43b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e43b-122">-WhatIf</span></span>
<span data-ttu-id="9e43b-123">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e43b-123">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="9e43b-124">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e43b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e43b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e43b-125">CommonParameters</span></span>
<span data-ttu-id="9e43b-126">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e43b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e43b-127">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="9e43b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e43b-128">輸入</span><span class="sxs-lookup"><span data-stu-id="9e43b-128">INPUTS</span></span>

### <span data-ttu-id="9e43b-129">所有</span><span class="sxs-lookup"><span data-stu-id="9e43b-129">None</span></span>
<span data-ttu-id="9e43b-130">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="9e43b-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9e43b-131">輸出</span><span class="sxs-lookup"><span data-stu-id="9e43b-131">OUTPUTS</span></span>

### <span data-ttu-id="9e43b-132">PSAzureOperationResponse 中的 [計算] 命令</span><span class="sxs-lookup"><span data-stu-id="9e43b-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="9e43b-133">筆記</span><span class="sxs-lookup"><span data-stu-id="9e43b-133">NOTES</span></span>

## <span data-ttu-id="9e43b-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e43b-134">RELATED LINKS</span></span>

[<span data-ttu-id="9e43b-135">AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9e43b-135">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="9e43b-136">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="9e43b-136">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


