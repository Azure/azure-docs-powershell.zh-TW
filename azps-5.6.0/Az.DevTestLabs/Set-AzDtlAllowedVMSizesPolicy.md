---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: AAABDD1D-71BF-409C-B50B-9BE861D84229
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/set-azdtlallowedvmsizespolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAllowedVMSizesPolicy.md
ms.openlocfilehash: 04538710a078c72c7b91725823601a55c21ef846
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101912866"
---
# <span data-ttu-id="63632-101">Set-AzDtlAllowedVMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="63632-101">Set-AzDtlAllowedVMSizesPolicy</span></span>

## <span data-ttu-id="63632-102">簡介</span><span class="sxs-lookup"><span data-stu-id="63632-102">SYNOPSIS</span></span>
<span data-ttu-id="63632-103">在 DevTest 實驗室中設定實驗室的允許虛擬機器大小策略。</span><span class="sxs-lookup"><span data-stu-id="63632-103">Sets the allowed virtual machine sizes policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="63632-104">語法</span><span class="sxs-lookup"><span data-stu-id="63632-104">SYNTAX</span></span>

### <span data-ttu-id="63632-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="63632-105">Enable (Default)</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63632-106">禁用</span><span class="sxs-lookup"><span data-stu-id="63632-106">Disable</span></span>
```
Set-AzDtlAllowedVMSizesPolicy [[-VmSizes] <String[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="63632-107">描述</span><span class="sxs-lookup"><span data-stu-id="63632-107">DESCRIPTION</span></span>
<span data-ttu-id="63632-108">**Set-AzDtlAllowedMSizesPolicy** Cmdlet 會設定允許的虛擬機器大小政策，指定實驗室中允許的虛擬機器大小清單。</span><span class="sxs-lookup"><span data-stu-id="63632-108">The **Set-AzDtlAllowedVMSizesPolicy** cmdlet sets the allowed virtual machine sizes policy, which specifies a list of virtual machine sizes allowed in a lab.</span></span>
<span data-ttu-id="63632-109">Cmdlet 會使用指定的資源群組和實驗室名稱來設定策略。</span><span class="sxs-lookup"><span data-stu-id="63632-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="63632-110">例子</span><span class="sxs-lookup"><span data-stu-id="63632-110">EXAMPLES</span></span>

## <span data-ttu-id="63632-111">參數</span><span class="sxs-lookup"><span data-stu-id="63632-111">PARAMETERS</span></span>

### <span data-ttu-id="63632-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63632-112">-DefaultProfile</span></span>
<span data-ttu-id="63632-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="63632-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="63632-114">-停用</span><span class="sxs-lookup"><span data-stu-id="63632-114">-Disable</span></span>
<span data-ttu-id="63632-115">表示此 Cmdlet 會停用該政策。</span><span class="sxs-lookup"><span data-stu-id="63632-115">Indicates that this cmdlet disables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63632-116">-啟用</span><span class="sxs-lookup"><span data-stu-id="63632-116">-Enable</span></span>
<span data-ttu-id="63632-117">表示此 Cmdlet 會啟用該策略。</span><span class="sxs-lookup"><span data-stu-id="63632-117">Indicates that this cmdlet enables the policy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Enable
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63632-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="63632-118">-LabName</span></span>
<span data-ttu-id="63632-119">指定此 Cmdlet 設定虛擬機器大小策略的實驗室名稱。</span><span class="sxs-lookup"><span data-stu-id="63632-119">Specifies the name of the lab for which this cmdlet sets the virtual machine sizes policy.</span></span>

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

### <span data-ttu-id="63632-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63632-120">-ResourceGroupName</span></span>
<span data-ttu-id="63632-121">指定實驗室所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="63632-121">Specifies the name of the resource group that the lab belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63632-122">-VmSizes</span><span class="sxs-lookup"><span data-stu-id="63632-122">-VmSizes</span></span>
<span data-ttu-id="63632-123">指定在實驗室中允許的虛擬機器大小清單，做為字串陣列。</span><span class="sxs-lookup"><span data-stu-id="63632-123">Specifies, as a string array, the list of virtual machine sizes allowed in the lab.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63632-124">-確認</span><span class="sxs-lookup"><span data-stu-id="63632-124">-Confirm</span></span>
<span data-ttu-id="63632-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="63632-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63632-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63632-126">-WhatIf</span></span>
<span data-ttu-id="63632-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="63632-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63632-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="63632-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63632-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63632-129">CommonParameters</span></span>
<span data-ttu-id="63632-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="63632-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63632-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="63632-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63632-132">輸入</span><span class="sxs-lookup"><span data-stu-id="63632-132">INPUTS</span></span>

### <span data-ttu-id="63632-133">System.String</span><span class="sxs-lookup"><span data-stu-id="63632-133">System.String</span></span>

## <span data-ttu-id="63632-134">輸出</span><span class="sxs-lookup"><span data-stu-id="63632-134">OUTPUTS</span></span>

### <span data-ttu-id="63632-135">Microsoft.Azure.Commands.DevTestLabs.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="63632-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="63632-136">筆記</span><span class="sxs-lookup"><span data-stu-id="63632-136">NOTES</span></span>

## <span data-ttu-id="63632-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="63632-137">RELATED LINKS</span></span>

[<span data-ttu-id="63632-138">Get-AzDtlAllowedMSizesPolicy</span><span class="sxs-lookup"><span data-stu-id="63632-138">Get-AzDtlAllowedVMSizesPolicy</span></span>](./Get-AzDtlAllowedVMSizesPolicy.md)


