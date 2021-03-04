---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 629ed4d9bc8eeb01f41bb857868f4206afcc9b0a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916742"
---
# <span data-ttu-id="52bdd-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="52bdd-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="52bdd-102">簡介</span><span class="sxs-lookup"><span data-stu-id="52bdd-102">SYNOPSIS</span></span>
<span data-ttu-id="52bdd-103">在 DevTest 實驗室中設定實驗室的每個使用者策略的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="52bdd-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="52bdd-104">語法</span><span class="sxs-lookup"><span data-stu-id="52bdd-104">SYNTAX</span></span>

### <span data-ttu-id="52bdd-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="52bdd-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52bdd-106">禁用</span><span class="sxs-lookup"><span data-stu-id="52bdd-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52bdd-107">描述</span><span class="sxs-lookup"><span data-stu-id="52bdd-107">DESCRIPTION</span></span>
<span data-ttu-id="52bdd-108">**Set-AzDtlVMsPerUserPolicy** Cmdlet 會設定每個實驗室使用者策略的虛擬機器，設定每個使用者允許的虛擬機器數量上限。</span><span class="sxs-lookup"><span data-stu-id="52bdd-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="52bdd-109">Cmdlet 會使用指定的資源群組和實驗室名稱來設定策略。</span><span class="sxs-lookup"><span data-stu-id="52bdd-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="52bdd-110">例子</span><span class="sxs-lookup"><span data-stu-id="52bdd-110">EXAMPLES</span></span>

## <span data-ttu-id="52bdd-111">參數</span><span class="sxs-lookup"><span data-stu-id="52bdd-111">PARAMETERS</span></span>

### <span data-ttu-id="52bdd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52bdd-112">-DefaultProfile</span></span>
<span data-ttu-id="52bdd-113">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="52bdd-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="52bdd-114">-停用</span><span class="sxs-lookup"><span data-stu-id="52bdd-114">-Disable</span></span>
<span data-ttu-id="52bdd-115">表示此 Cmdlet 會停用實驗室的策略。</span><span class="sxs-lookup"><span data-stu-id="52bdd-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="52bdd-116">-啟用</span><span class="sxs-lookup"><span data-stu-id="52bdd-116">-Enable</span></span>
<span data-ttu-id="52bdd-117">表示此 Cmdlet 為實驗室啟用該策略。</span><span class="sxs-lookup"><span data-stu-id="52bdd-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="52bdd-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="52bdd-118">-LabName</span></span>
<span data-ttu-id="52bdd-119">指定此 Cmdlet 會針對每個使用者策略設定虛擬機器的實驗室名稱。</span><span class="sxs-lookup"><span data-stu-id="52bdd-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="52bdd-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="52bdd-120">-MaxVMs</span></span>
<span data-ttu-id="52bdd-121">指定可在實驗室中建立之虛擬機器的數量上限。</span><span class="sxs-lookup"><span data-stu-id="52bdd-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="52bdd-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52bdd-122">-ResourceGroupName</span></span>
<span data-ttu-id="52bdd-123">指定實驗室所屬的資源組名。</span><span class="sxs-lookup"><span data-stu-id="52bdd-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="52bdd-124">-確認</span><span class="sxs-lookup"><span data-stu-id="52bdd-124">-Confirm</span></span>
<span data-ttu-id="52bdd-125">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="52bdd-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52bdd-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52bdd-126">-WhatIf</span></span>
<span data-ttu-id="52bdd-127">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52bdd-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52bdd-128">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52bdd-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52bdd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52bdd-129">CommonParameters</span></span>
<span data-ttu-id="52bdd-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="52bdd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52bdd-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="52bdd-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52bdd-132">輸入</span><span class="sxs-lookup"><span data-stu-id="52bdd-132">INPUTS</span></span>

### <span data-ttu-id="52bdd-133">System.String</span><span class="sxs-lookup"><span data-stu-id="52bdd-133">System.String</span></span>

## <span data-ttu-id="52bdd-134">輸出</span><span class="sxs-lookup"><span data-stu-id="52bdd-134">OUTPUTS</span></span>

### <span data-ttu-id="52bdd-135">Microsoft.Azure.Commands.DevTestLabs.models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="52bdd-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="52bdd-136">筆記</span><span class="sxs-lookup"><span data-stu-id="52bdd-136">NOTES</span></span>

## <span data-ttu-id="52bdd-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="52bdd-137">RELATED LINKS</span></span>

[<span data-ttu-id="52bdd-138">Get-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="52bdd-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


