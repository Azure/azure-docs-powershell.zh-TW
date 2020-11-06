---
external help file: Microsoft.Azure.Commands.DevTestLabs.dll-Help.xml
Module Name: AzureRM.DevTestLabs
ms.assetid: 8AAD9309-5763-4903-AF6A-1E50310146C0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devtestlabs/set-azurermdtlautoshutdownpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevTestLabs/Commands.DevTestLabs/help/Set-AzureRmDtlAutoShutdownPolicy.md
ms.openlocfilehash: edded91551b87e180b17ff8f97d84d16bef0b0ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455420"
---
# <span data-ttu-id="506e7-101">Set-AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="506e7-101">Set-AzureRmDtlAutoShutdownPolicy</span></span>

## <span data-ttu-id="506e7-102">摘要</span><span class="sxs-lookup"><span data-stu-id="506e7-102">SYNOPSIS</span></span>
<span data-ttu-id="506e7-103">設定實驗 DevTest 實驗的自動關閉原則。</span><span class="sxs-lookup"><span data-stu-id="506e7-103">Sets the auto shutdown policy of a lab DevTest Labs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="506e7-104">句法</span><span class="sxs-lookup"><span data-stu-id="506e7-104">SYNTAX</span></span>

### <span data-ttu-id="506e7-105">啟用 (預設) </span><span class="sxs-lookup"><span data-stu-id="506e7-105">Enable (Default)</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Enable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="506e7-106">禁止</span><span class="sxs-lookup"><span data-stu-id="506e7-106">Disable</span></span>
```
Set-AzureRmDtlAutoShutdownPolicy [[-Time] <DateTime>] [-Disable] [-LabName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="506e7-107">說明</span><span class="sxs-lookup"><span data-stu-id="506e7-107">DESCRIPTION</span></span>
<span data-ttu-id="506e7-108">**AzureRmDtlAutoShutdownPolicy** Cmdlet 會設定實驗的自動關閉原則，這會在一天指定的時間自動關閉實驗室中的所有虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="506e7-108">The **Set-AzureRmDtlAutoShutdownPolicy** cmdlet sets the auto shutdown policy of a lab, which automatically shuts down all the virtual machines in the lab at a specified time of the day.</span></span>
<span data-ttu-id="506e7-109">此 Cmdlet 會使用指定的資源群組和 lab 名稱來設定原則。</span><span class="sxs-lookup"><span data-stu-id="506e7-109">The cmdlet uses the specified resource group and name of the lab to set the policy.</span></span>

## <span data-ttu-id="506e7-110">示例</span><span class="sxs-lookup"><span data-stu-id="506e7-110">EXAMPLES</span></span>

## <span data-ttu-id="506e7-111">參數</span><span class="sxs-lookup"><span data-stu-id="506e7-111">PARAMETERS</span></span>

### <span data-ttu-id="506e7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="506e7-112">-DefaultProfile</span></span>
<span data-ttu-id="506e7-113">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="506e7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="506e7-114">-停用</span><span class="sxs-lookup"><span data-stu-id="506e7-114">-Disable</span></span>
<span data-ttu-id="506e7-115">表示該 Cmdlet 停用實驗室中的原則。</span><span class="sxs-lookup"><span data-stu-id="506e7-115">Indicates that the cmdlet disables the policy in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506e7-116">-啟用</span><span class="sxs-lookup"><span data-stu-id="506e7-116">-Enable</span></span>
<span data-ttu-id="506e7-117">表示此 Cmdlet 在 lab 中啟用原則。</span><span class="sxs-lookup"><span data-stu-id="506e7-117">Indicates that the cmdlet enables the policy in the lab.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Enable
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506e7-118">-LabName</span><span class="sxs-lookup"><span data-stu-id="506e7-118">-LabName</span></span>
<span data-ttu-id="506e7-119">指定此 Cmdlet 設定自動關閉原則的實驗名稱。</span><span class="sxs-lookup"><span data-stu-id="506e7-119">Specifies the name of the lab for which this cmdlet sets the auto shutdown policy.</span></span>

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

### <span data-ttu-id="506e7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="506e7-120">-ResourceGroupName</span></span>
<span data-ttu-id="506e7-121">指定實驗室所屬之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="506e7-121">Specifies the name of the resource group that the lab belongs to.</span></span>

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

### <span data-ttu-id="506e7-122">時間</span><span class="sxs-lookup"><span data-stu-id="506e7-122">-Time</span></span>
<span data-ttu-id="506e7-123">指定實驗室中的虛擬機器必須關閉時的時間（以 **DateTime** 物件表示）。</span><span class="sxs-lookup"><span data-stu-id="506e7-123">Specifies the time, as a **DateTime** object, for when the virtual machines in the lab must shut down.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="506e7-124">-確認</span><span class="sxs-lookup"><span data-stu-id="506e7-124">-Confirm</span></span>
<span data-ttu-id="506e7-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="506e7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="506e7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="506e7-126">-WhatIf</span></span>
<span data-ttu-id="506e7-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="506e7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="506e7-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="506e7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="506e7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="506e7-129">CommonParameters</span></span>
<span data-ttu-id="506e7-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="506e7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="506e7-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="506e7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="506e7-132">輸入</span><span class="sxs-lookup"><span data-stu-id="506e7-132">INPUTS</span></span>

### <span data-ttu-id="506e7-133">所有</span><span class="sxs-lookup"><span data-stu-id="506e7-133">None</span></span>
<span data-ttu-id="506e7-134">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="506e7-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="506e7-135">輸出</span><span class="sxs-lookup"><span data-stu-id="506e7-135">OUTPUTS</span></span>

### <span data-ttu-id="506e7-136">PSSchedule 中的 DevTestLabs。</span><span class="sxs-lookup"><span data-stu-id="506e7-136">Microsoft.Azure.Commands.DevTestLabs.Models.PSSchedule</span></span>
<span data-ttu-id="506e7-137">這個 Cmdlet 會傳回指定實驗室中的虛擬機器必須關閉的時間。</span><span class="sxs-lookup"><span data-stu-id="506e7-137">This cmdlet returns the schedule which specifies when the virtual machines in the lab must shut down.</span></span>

## <span data-ttu-id="506e7-138">筆記</span><span class="sxs-lookup"><span data-stu-id="506e7-138">NOTES</span></span>

## <span data-ttu-id="506e7-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="506e7-139">RELATED LINKS</span></span>

[<span data-ttu-id="506e7-140">AzureRmDtlAutoShutdownPolicy</span><span class="sxs-lookup"><span data-stu-id="506e7-140">Get-AzureRmDtlAutoShutdownPolicy</span></span>](./Get-AzureRmDtlAutoShutdownPolicy.md)


