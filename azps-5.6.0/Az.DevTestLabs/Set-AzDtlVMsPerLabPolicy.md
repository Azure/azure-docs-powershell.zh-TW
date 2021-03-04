---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D2A7ECF6-E2B1-4BD5-BEA6-C9EC0C7377BA
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/set-azdtlvmsperlabpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerLabPolicy.md
ms.openlocfilehash: 30aad11674cbdef747e444d18bce55ed223e3698
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916748"
---
# <span data-ttu-id="a6fb1-101">Set-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="a6fb1-101">Set-AzDtlVMsPerLabPolicy</span></span>

## <span data-ttu-id="a6fb1-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a6fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="a6fb1-103">在 DevTest 實驗室中設定每個實驗室的虛擬機器策略。</span><span class="sxs-lookup"><span data-stu-id="a6fb1-103">Sets the virtual machines per lab policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="a6fb1-104">語法</span><span class="sxs-lookup"><span data-stu-id="a6fb1-104">SYNTAX</span></span>

### <span data-ttu-id="a6fb1-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="a6fb1-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6fb1-106">禁用</span><span class="sxs-lookup"><span data-stu-id="a6fb1-106">Disable</span></span>
```
Set-AzDtlVMsPerLabPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6fb1-107">描述</span><span class="sxs-lookup"><span data-stu-id="a6fb1-107">DESCRIPTION</span></span>
<span data-ttu-id="a6fb1-108">**Set-AzDtlVMsPerLabPolicy** Cmdlet 會根據實驗室的實驗室策略設定虛擬機器，以設定實驗室中允許的虛擬機器總數。</span><span class="sxs-lookup"><span data-stu-id="a6fb1-108">The **Set-AzDtlVMsPerLabPolicy** cmdlet sets the virtual machines per lab policy of a lab, which sets the total number of virtual machines allowed in a lab.</span></span>
<span data-ttu-id="a6fb1-109">Cmdlet 會使用指定的資源群組和實驗室名稱來設定策略。</span><span class="sxs-lookup"><span data-stu-id="a6fb1-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="a6fb1-110">例子</span><span class="sxs-lookup"><span data-stu-id="a6fb1-110">EXAMPLES</span></span>

## <span data-ttu-id="a6fb1-111">參數</span><span class="sxs-lookup"><span data-stu-id="a6fb1-111">PARAMETERS</span></span>

### <span data-ttu-id="a6fb1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6fb1-112">-DefaultProfile</span></span>
<span data-ttu-id="a6fb1-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a6fb1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6fb1-114">-停用</span><span class="sxs-lookup"><span data-stu-id="a6fb1-114">-Disable</span></span>
<span data-ttu-id="a6fb1-115">表示此 Cmdlet 會停用實驗室的政策。</span><span class="sxs-lookup"><span data-stu-id="a6fb1-115">Indicates that this cmdlet disables the policy of the lab.</span></span>

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

### <span data-ttu-id="a6fb1-116">-啟用</span><span class="sxs-lookup"><span data-stu-id="a6fb1-116">-Enable</span></span>
<span data-ttu-id="a6fb1-117">表示此 Cmdlet 會啟用實驗室的策略。</span><span class="sxs-lookup"><span data-stu-id="a6fb1-117">Indicates that this cmdlet enables the policy of the lab.</span></span>

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

### <span data-ttu-id="a6fb1-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="a6fb1-118">-LabName</span></span>
<span data-ttu-id="a6fb1-119">指定此 Cmdlet 根據實驗室策略設定虛擬機器的實驗室名稱。</span><span class="sxs-lookup"><span data-stu-id="a6fb1-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per lab policy.</span></span>

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

### <span data-ttu-id="a6fb1-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="a6fb1-120">-MaxVMs</span></span>
<span data-ttu-id="a6fb1-121">指定可在實驗室中建立之虛擬機器的數量上限。</span><span class="sxs-lookup"><span data-stu-id="a6fb1-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6fb1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6fb1-122">-ResourceGroupName</span></span>
<span data-ttu-id="a6fb1-123">指定實驗室所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="a6fb1-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="a6fb1-124">-確認</span><span class="sxs-lookup"><span data-stu-id="a6fb1-124">-Confirm</span></span>
<span data-ttu-id="a6fb1-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="a6fb1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6fb1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6fb1-126">-WhatIf</span></span>
<span data-ttu-id="a6fb1-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a6fb1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6fb1-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a6fb1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6fb1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6fb1-129">CommonParameters</span></span>
<span data-ttu-id="a6fb1-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a6fb1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6fb1-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a6fb1-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6fb1-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a6fb1-132">INPUTS</span></span>

### <span data-ttu-id="a6fb1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a6fb1-133">System.String</span></span>

## <span data-ttu-id="a6fb1-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a6fb1-134">OUTPUTS</span></span>

### <span data-ttu-id="a6fb1-135">Microsoft.Azure.Commands.DevTestLabs.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="a6fb1-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="a6fb1-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a6fb1-136">NOTES</span></span>

## <span data-ttu-id="a6fb1-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="a6fb1-137">RELATED LINKS</span></span>

[<span data-ttu-id="a6fb1-138">Get-AzDtlVMsPerLabPolicy</span><span class="sxs-lookup"><span data-stu-id="a6fb1-138">Get-AzDtlVMsPerLabPolicy</span></span>](./Get-AzDtlVMsPerLabPolicy.md)


