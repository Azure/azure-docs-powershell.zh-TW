---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: D00E04D9-C91F-4F89-8867-0A026C274F27
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlvmsperuserpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlVMsPerUserPolicy.md
ms.openlocfilehash: 33f60d8246f7235e4be816ad55b69c2ebafe9b0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622386"
---
# <span data-ttu-id="5395a-101">Set-AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="5395a-101">Set-AzDtlVMsPerUserPolicy</span></span>

## <span data-ttu-id="5395a-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5395a-102">SYNOPSIS</span></span>
<span data-ttu-id="5395a-103">在 DevTest Labs 中設定每位使用者的虛擬機器原則。</span><span class="sxs-lookup"><span data-stu-id="5395a-103">Sets the virtual machines per user policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="5395a-104">句法</span><span class="sxs-lookup"><span data-stu-id="5395a-104">SYNTAX</span></span>

### <span data-ttu-id="5395a-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="5395a-105">Enable (Default)</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5395a-106">禁止</span><span class="sxs-lookup"><span data-stu-id="5395a-106">Disable</span></span>
```
Set-AzDtlVMsPerUserPolicy [[-MaxVMs] <Int32>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5395a-107">說明</span><span class="sxs-lookup"><span data-stu-id="5395a-107">DESCRIPTION</span></span>
<span data-ttu-id="5395a-108">**AzDtlVMsPerUserPolicy** Cmdlet 會設定實驗室的每個使用者原則的虛擬機器原則，這會設定每位使用者允許的虛擬機器數量上限。</span><span class="sxs-lookup"><span data-stu-id="5395a-108">The **Set-AzDtlVMsPerUserPolicy** cmdlet sets the virtual machines per user policy of a lab, which sets the maximum number of virtual machines allowed per user.</span></span>
<span data-ttu-id="5395a-109">此 Cmdlet 會使用指定的資源群組和 lab 名稱來設定原則。</span><span class="sxs-lookup"><span data-stu-id="5395a-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="5395a-110">示例</span><span class="sxs-lookup"><span data-stu-id="5395a-110">EXAMPLES</span></span>

## <span data-ttu-id="5395a-111">參數</span><span class="sxs-lookup"><span data-stu-id="5395a-111">PARAMETERS</span></span>

### <span data-ttu-id="5395a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5395a-112">-DefaultProfile</span></span>
<span data-ttu-id="5395a-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5395a-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5395a-114">-停用</span><span class="sxs-lookup"><span data-stu-id="5395a-114">-Disable</span></span>
<span data-ttu-id="5395a-115">表示此 Cmdlet 會停用實驗室的原則。</span><span class="sxs-lookup"><span data-stu-id="5395a-115">Indicates that this cmdlet disables the policy for the lab.</span></span>

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

### <span data-ttu-id="5395a-116">-啟用</span><span class="sxs-lookup"><span data-stu-id="5395a-116">-Enable</span></span>
<span data-ttu-id="5395a-117">表示此 Cmdlet 可為 lab 啟用原則。</span><span class="sxs-lookup"><span data-stu-id="5395a-117">Indicates that this cmdlet enables the policy for the lab.</span></span>

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

### <span data-ttu-id="5395a-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="5395a-118">-LabName</span></span>
<span data-ttu-id="5395a-119">指定此 Cmdlet 針對每個使用者策略設定虛擬機器原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="5395a-119">Specifies the name of the lab for which this cmdlet sets the virtual machines per user policy.</span></span>

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

### <span data-ttu-id="5395a-120">-MaxVMs</span><span class="sxs-lookup"><span data-stu-id="5395a-120">-MaxVMs</span></span>
<span data-ttu-id="5395a-121">指定可在 lab 中建立的虛擬機器數目上限。</span><span class="sxs-lookup"><span data-stu-id="5395a-121">Specifies the maximum number of virtual machines that can be created in the lab.</span></span>

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

### <span data-ttu-id="5395a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5395a-122">-ResourceGroupName</span></span>
<span data-ttu-id="5395a-123">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5395a-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="5395a-124">-確認</span><span class="sxs-lookup"><span data-stu-id="5395a-124">-Confirm</span></span>
<span data-ttu-id="5395a-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5395a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5395a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5395a-126">-WhatIf</span></span>
<span data-ttu-id="5395a-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5395a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5395a-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5395a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5395a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5395a-129">CommonParameters</span></span>
<span data-ttu-id="5395a-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5395a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5395a-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5395a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5395a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="5395a-132">INPUTS</span></span>

### <span data-ttu-id="5395a-133">System.object</span><span class="sxs-lookup"><span data-stu-id="5395a-133">System.String</span></span>

## <span data-ttu-id="5395a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="5395a-134">OUTPUTS</span></span>

### <span data-ttu-id="5395a-135">PSPolicy 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="5395a-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSPolicy</span></span>

## <span data-ttu-id="5395a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="5395a-136">NOTES</span></span>

## <span data-ttu-id="5395a-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="5395a-137">RELATED LINKS</span></span>

[<span data-ttu-id="5395a-138">AzDtlVMsPerUserPolicy</span><span class="sxs-lookup"><span data-stu-id="5395a-138">Get-AzDtlVMsPerUserPolicy</span></span>](./Get-AzDtlVMsPerUserPolicy.md)


