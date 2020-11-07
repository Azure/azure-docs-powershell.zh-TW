---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoShutdownPolicy.md
ms.openlocfilehash: 3b8c6965034b741ddd281bb81c9748a25d7038be
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93958328"
---
# <span data-ttu-id="d3d02-101">Set-AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="d3d02-101">Set-AzDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="d3d02-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d3d02-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d02-103">設定實驗 DevTest 實驗的自動關閉原則。</span><span class="sxs-lookup"><span data-stu-id="d3d02-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

## <span data-ttu-id="d3d02-104">句法</span><span class="sxs-lookup"><span data-stu-id="d3d02-104">SYNTAX</span></span>

### <span data-ttu-id="d3d02-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="d3d02-105">Enable (Default)</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3d02-106">禁止</span><span class="sxs-lookup"><span data-stu-id="d3d02-106">Disable</span></span>
```
Set-AzDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3d02-107">說明</span><span class="sxs-lookup"><span data-stu-id="d3d02-107">DESCRIPTION</span></span>
<span data-ttu-id="d3d02-108">**AzDtlAutoShutdownPolicy** Cmdlet 會設定實驗的自動關閉原則，這會在一天指定的時間自動關閉實驗室中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="d3d02-108">The **Set-AzDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="d3d02-109">此 Cmdlet 會使用指定的資源群組和 lab 名稱來設定原則。</span><span class="sxs-lookup"><span data-stu-id="d3d02-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="d3d02-110">示例</span><span class="sxs-lookup"><span data-stu-id="d3d02-110">EXAMPLES</span></span>

## <span data-ttu-id="d3d02-111">參數</span><span class="sxs-lookup"><span data-stu-id="d3d02-111">PARAMETERS</span></span>

### <span data-ttu-id="d3d02-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d02-112">-DefaultProfile</span></span>
<span data-ttu-id="d3d02-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d3d02-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3d02-114">-停用</span><span class="sxs-lookup"><span data-stu-id="d3d02-114">-Disable</span></span>
<span data-ttu-id="d3d02-115">表示該 Cmdlet 停用實驗室中的原則。</span><span class="sxs-lookup"><span data-stu-id="d3d02-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

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

### <span data-ttu-id="d3d02-116">-啟用</span><span class="sxs-lookup"><span data-stu-id="d3d02-116">-Enable</span></span>
<span data-ttu-id="d3d02-117">表示此 Cmdlet 在 lab 中啟用原則。</span><span class="sxs-lookup"><span data-stu-id="d3d02-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

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

### <span data-ttu-id="d3d02-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="d3d02-118">-LabName</span></span>
<span data-ttu-id="d3d02-119">指定此 Cmdlet 設定自動關閉原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="d3d02-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="d3d02-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3d02-120">-ResourceGroupName</span></span>
<span data-ttu-id="d3d02-121">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3d02-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="d3d02-122">時間</span><span class="sxs-lookup"><span data-stu-id="d3d02-122">-Time</span></span>
<span data-ttu-id="d3d02-123">指定實驗室中的虛擬機器必須關閉時的時間（以 **DateTime** 物件表示）。</span><span class="sxs-lookup"><span data-stu-id="d3d02-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

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

### <span data-ttu-id="d3d02-124">-確認</span><span class="sxs-lookup"><span data-stu-id="d3d02-124">-Confirm</span></span>
<span data-ttu-id="d3d02-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d3d02-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3d02-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3d02-126">-WhatIf</span></span>
<span data-ttu-id="d3d02-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d3d02-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3d02-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d3d02-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3d02-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d02-129">CommonParameters</span></span>
<span data-ttu-id="d3d02-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d3d02-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d02-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d3d02-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d02-132">輸入</span><span class="sxs-lookup"><span data-stu-id="d3d02-132">INPUTS</span></span>

### <span data-ttu-id="d3d02-133">System.object</span><span class="sxs-lookup"><span data-stu-id="d3d02-133">System.String</span></span>

## <span data-ttu-id="d3d02-134">輸出</span><span class="sxs-lookup"><span data-stu-id="d3d02-134">OUTPUTS</span></span>

### <span data-ttu-id="d3d02-135">PSSchedule 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="d3d02-135">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="d3d02-136">筆記</span><span class="sxs-lookup"><span data-stu-id="d3d02-136">NOTES</span></span>

## <span data-ttu-id="d3d02-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="d3d02-137">RELATED LINKS</span></span>

[<span data-ttu-id="d3d02-138">AzDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="d3d02-138">Get-AzDtlAutoShutdownPolicy</span></span>](./Get-AzDtlAutoShutdownPolicy.md)


