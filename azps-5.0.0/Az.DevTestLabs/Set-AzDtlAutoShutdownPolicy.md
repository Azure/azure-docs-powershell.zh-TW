---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: e8980d7e323cc6958ff64fa2d763b414eff97b34
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94136987"
---
# <span data-ttu-id="2b105-101">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="2b105-101">Set-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="2b105-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b105-102">SYNOPSIS</span></span>
<span data-ttu-id="2b105-103">設定實驗 DevTest 實驗的自動關閉原則。</span><span class="sxs-lookup"><span data-stu-id="2b105-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

## <span data-ttu-id="2b105-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b105-104">SYNTAX</span></span>

### <span data-ttu-id="2b105-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="2b105-105">Enable (Default)</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b105-106">禁止</span><span class="sxs-lookup"><span data-stu-id="2b105-106">Disable</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b105-107">說明</span><span class="sxs-lookup"><span data-stu-id="2b105-107">DESCRIPTION</span></span>
<span data-ttu-id="2b105-108">**AzDtlAutoShutdownPolicy** Cmdlet 會設定實驗的自動關閉原則，這會在一天指定的時間自動關閉實驗室中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="2b105-108">The **Set-AzDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="2b105-109">此 Cmdlet 會使用指定的資源群組和 lab 名稱來設定原則。</span><span class="sxs-lookup"><span data-stu-id="2b105-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="2b105-110">示例</span><span class="sxs-lookup"><span data-stu-id="2b105-110">EXAMPLES</span></span>

### <span data-ttu-id="2b105-111">範例1</span><span class="sxs-lookup"><span data-stu-id="2b105-111">Example 1</span></span>

<span data-ttu-id="2b105-112">設定實驗 DevTest 實驗的自動關閉原則。</span><span class="sxs-lookup"><span data-stu-id="2b105-112">Sets the auto shutdown policy of a lab DevTest Labs.</span></span> <span data-ttu-id="2b105-113"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="2b105-113">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzDtlAutoShutdownPolicy -Enable -LabName <String> -ResourceGroupName MyResourceGroup -Time <DateTime>
```

## <span data-ttu-id="2b105-114">參數</span><span class="sxs-lookup"><span data-stu-id="2b105-114">PARAMETERS</span></span>

### <span data-ttu-id="2b105-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b105-115">-DefaultProfile</span></span>
<span data-ttu-id="2b105-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2b105-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b105-117">-停用</span><span class="sxs-lookup"><span data-stu-id="2b105-117">-Disable</span></span>
<span data-ttu-id="2b105-118">表示該 Cmdlet 停用實驗室中的原則。</span><span class="sxs-lookup"><span data-stu-id="2b105-118">Indicates that the cmdlet disables the policy in the lab.</span></span>

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

### <span data-ttu-id="2b105-119">-啟用</span><span class="sxs-lookup"><span data-stu-id="2b105-119">-Enable</span></span>
<span data-ttu-id="2b105-120">表示此 Cmdlet 在 lab 中啟用原則。</span><span class="sxs-lookup"><span data-stu-id="2b105-120">Indicates that the cmdlet enables the policy in the lab.</span></span>

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

### <span data-ttu-id="2b105-121">-LabName</span><span class="sxs-lookup"><span data-stu-id="2b105-121">-LabName</span></span>
<span data-ttu-id="2b105-122">指定此 Cmdlet 設定自動關閉原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="2b105-122">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="2b105-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b105-123">-ResourceGroupName</span></span>
<span data-ttu-id="2b105-124">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b105-124">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="2b105-125">時間</span><span class="sxs-lookup"><span data-stu-id="2b105-125">-Time</span></span>
<span data-ttu-id="2b105-126">指定實驗室中的虛擬機器必須關閉時的時間（以 **DateTime** 物件表示）。</span><span class="sxs-lookup"><span data-stu-id="2b105-126">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b105-127">-確認</span><span class="sxs-lookup"><span data-stu-id="2b105-127">-Confirm</span></span>
<span data-ttu-id="2b105-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2b105-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b105-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b105-129">-WhatIf</span></span>
<span data-ttu-id="2b105-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b105-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b105-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b105-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b105-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b105-132">CommonParameters</span></span>
<span data-ttu-id="2b105-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b105-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b105-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b105-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b105-135">輸入</span><span class="sxs-lookup"><span data-stu-id="2b105-135">INPUTS</span></span>

### <span data-ttu-id="2b105-136">System.object</span><span class="sxs-lookup"><span data-stu-id="2b105-136">System.String</span></span>

## <span data-ttu-id="2b105-137">輸出</span><span class="sxs-lookup"><span data-stu-id="2b105-137">OUTPUTS</span></span>

### <span data-ttu-id="2b105-138">PSSchedule 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="2b105-138">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="2b105-139">筆記</span><span class="sxs-lookup"><span data-stu-id="2b105-139">NOTES</span></span>

## <span data-ttu-id="2b105-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b105-140">RELATED LINKS</span></span>

[<span data-ttu-id="2b105-141">AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="2b105-141">Get-AzDtlAutoShutdownPolicy</span></span>](./Get-AzDtlAutoShutdownPolicy.md)

