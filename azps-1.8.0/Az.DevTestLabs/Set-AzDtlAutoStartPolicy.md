---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevTestLabs.dll-Help.xml
Module Name: Az.DevTestLabs
ms.assetid: 3FADEC2E-4A2B-46EB-8A94-CF48D717C7FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.devtestlabs/set-azdtlautostartpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevTestLabs/DevTestLabs/help/Set-AzDtlAutoStartPolicy.md
ms.openlocfilehash: c751335f05f0e6ac9df5acb585dc5eb651d957a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622389"
---
# <span data-ttu-id="ae125-101">Set-AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="ae125-101">Set-AzDtlAutoStartPolicy</span></span>

## <span data-ttu-id="ae125-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ae125-102">SYNOPSIS</span></span>
<span data-ttu-id="ae125-103">在 DevTest Labs 中設定實驗的自動啟動原則。</span><span class="sxs-lookup"><span data-stu-id="ae125-103">Sets the auto start policy of a lab in DevTest Labs.</span></span>

## <span data-ttu-id="ae125-104">句法</span><span class="sxs-lookup"><span data-stu-id="ae125-104">SYNTAX</span></span>

### <span data-ttu-id="ae125-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="ae125-105">Enable (Default)</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae125-106">禁止</span><span class="sxs-lookup"><span data-stu-id="ae125-106">Disable</span></span>
```
Set-AzDtlAutoStartPolicy [[-Time] <DateTime>] [[-Days] <DayOfWeek[]>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ae125-107">說明</span><span class="sxs-lookup"><span data-stu-id="ae125-107">DESCRIPTION</span></span>
<span data-ttu-id="ae125-108">**AzDtlAutoStartPolicy** Cmdlet 會設定 lab 的自動啟動原則，這可讓實驗式虛擬機器排程自動啟動。</span><span class="sxs-lookup"><span data-stu-id="ae125-108">The **Set-AzDtlAutoStartPolicy** cmdlet sets the auto start policy of a lab, which allows lab virtual machines to be scheduled for automatic start.</span></span>
<span data-ttu-id="ae125-109">此 Cmdlet 會使用指定的資源群組和 lab 名稱來設定原則。</span><span class="sxs-lookup"><span data-stu-id="ae125-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="ae125-110">示例</span><span class="sxs-lookup"><span data-stu-id="ae125-110">EXAMPLES</span></span>

## <span data-ttu-id="ae125-111">參數</span><span class="sxs-lookup"><span data-stu-id="ae125-111">PARAMETERS</span></span>

### <span data-ttu-id="ae125-112">天</span><span class="sxs-lookup"><span data-stu-id="ae125-112">-Days</span></span>
<span data-ttu-id="ae125-113">指定為數組，即必須在每週的哪幾天啟動實驗室的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="ae125-113">Specifies, as an array, the days of the week for when the virtual machines of the lab must be started.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: (All)
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae125-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae125-114">-DefaultProfile</span></span>
<span data-ttu-id="ae125-115">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ae125-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ae125-116">-停用</span><span class="sxs-lookup"><span data-stu-id="ae125-116">-Disable</span></span>
<span data-ttu-id="ae125-117">表示此 Cmdlet 會針對實驗室中的虛擬機器停用原則。</span><span class="sxs-lookup"><span data-stu-id="ae125-117">Indicates that this cmdlet disables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="ae125-118">-啟用</span><span class="sxs-lookup"><span data-stu-id="ae125-118">-Enable</span></span>
<span data-ttu-id="ae125-119">表示此 Cmdlet 會針對實驗室中的虛擬機器啟用原則。</span><span class="sxs-lookup"><span data-stu-id="ae125-119">Indicates that this cmdlet enables the policy for the virtual machines in the lab.</span></span>

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

### <span data-ttu-id="ae125-120">-LabName</span><span class="sxs-lookup"><span data-stu-id="ae125-120">-LabName</span></span>
<span data-ttu-id="ae125-121">指定此 Cmdlet 設定自動啟動原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="ae125-121">Specifies the name of the lab for which this cmdlet sets the automatic start policy.</span></span>

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

### <span data-ttu-id="ae125-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae125-122">-ResourceGroupName</span></span>
<span data-ttu-id="ae125-123">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="ae125-123">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="ae125-124">時間</span><span class="sxs-lookup"><span data-stu-id="ae125-124">-Time</span></span>
<span data-ttu-id="ae125-125">指定實驗室的虛擬機器必須開始的時間。</span><span class="sxs-lookup"><span data-stu-id="ae125-125">Specifies the time when the virtual machines of the lab must be started.</span></span>

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

### <span data-ttu-id="ae125-126">-確認</span><span class="sxs-lookup"><span data-stu-id="ae125-126">-Confirm</span></span>
<span data-ttu-id="ae125-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ae125-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae125-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae125-128">-WhatIf</span></span>
<span data-ttu-id="ae125-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ae125-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae125-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ae125-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae125-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae125-131">CommonParameters</span></span>
<span data-ttu-id="ae125-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ae125-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae125-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ae125-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae125-134">輸入</span><span class="sxs-lookup"><span data-stu-id="ae125-134">INPUTS</span></span>

### <span data-ttu-id="ae125-135">System.object</span><span class="sxs-lookup"><span data-stu-id="ae125-135">System.String</span></span>

## <span data-ttu-id="ae125-136">輸出</span><span class="sxs-lookup"><span data-stu-id="ae125-136">OUTPUTS</span></span>

### <span data-ttu-id="ae125-137">PSSchedule 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="ae125-137">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>

## <span data-ttu-id="ae125-138">筆記</span><span class="sxs-lookup"><span data-stu-id="ae125-138">NOTES</span></span>

## <span data-ttu-id="ae125-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="ae125-139">RELATED LINKS</span></span>

[<span data-ttu-id="ae125-140">AzDtlAutoStartPolicy</span><span class="sxs-lookup"><span data-stu-id="ae125-140">Get-AzDtlAutoStartPolicy</span></span>](./Get-AzDtlAutoStartPolicy.md)


