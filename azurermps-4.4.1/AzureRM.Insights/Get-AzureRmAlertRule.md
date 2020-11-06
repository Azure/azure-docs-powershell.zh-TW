---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 65c5bc7a2767fd00497b487783c4e6f0ce6d6723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456584"
---
# <span data-ttu-id="c5b19-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="c5b19-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="c5b19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="c5b19-102">SYNOPSIS</span></span>
<span data-ttu-id="c5b19-103">取得警示規則。</span><span class="sxs-lookup"><span data-stu-id="c5b19-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5b19-104">句法</span><span class="sxs-lookup"><span data-stu-id="c5b19-104">SYNTAX</span></span>

### <span data-ttu-id="c5b19-105">Get-AzureRmAlertRule Cmdlet 的參數</span><span class="sxs-lookup"><span data-stu-id="c5b19-105">Parameters for Get-AzureRmAlertRule cmdlet</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c5b19-106">使用 name Get-AzureRmAlertRule Cmdlet 的參數</span><span class="sxs-lookup"><span data-stu-id="c5b19-106">Parameters for Get-AzureRmAlertRule cmdlet using name</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5b19-107">使用目標資源 uri Get-AzureRmAlertRule Cmdlet 的參數</span><span class="sxs-lookup"><span data-stu-id="c5b19-107">Parameters for Get-AzureRmAlertRule cmdlet using target resource uri</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5b19-108">說明</span><span class="sxs-lookup"><span data-stu-id="c5b19-108">DESCRIPTION</span></span>
<span data-ttu-id="c5b19-109">AzureRmAlertRule Cmdlet 會根據其名稱或 URI，或從指定的資源群組取得所有警示規則，來 **取得** 警示規則。</span><span class="sxs-lookup"><span data-stu-id="c5b19-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="c5b19-110">示例</span><span class="sxs-lookup"><span data-stu-id="c5b19-110">EXAMPLES</span></span>

### <span data-ttu-id="c5b19-111">範例1：取得資源群組的警示規則</span><span class="sxs-lookup"><span data-stu-id="c5b19-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="c5b19-112">這個命令會取得名為 [預設-Web CentralUS] 的資源群組的所有通知規則。</span><span class="sxs-lookup"><span data-stu-id="c5b19-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="c5b19-113">輸出不會包含有關規則的詳細資料，因為未指定 *DetailedOutput* 參數。</span><span class="sxs-lookup"><span data-stu-id="c5b19-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="c5b19-114">範例2：依名稱取得警示規則</span><span class="sxs-lookup"><span data-stu-id="c5b19-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="c5b19-115">這個命令會取得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。</span><span class="sxs-lookup"><span data-stu-id="c5b19-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="c5b19-116">因為未指定 *DetailedOutput* 參數，所以輸出只包含有關警示規則的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="c5b19-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="c5b19-117">範例3：透過名稱取得警示規則及詳細的輸出</span><span class="sxs-lookup"><span data-stu-id="c5b19-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="c5b19-118">這個命令會取得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。</span><span class="sxs-lookup"><span data-stu-id="c5b19-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="c5b19-119">已指定 *DetailedOutput* 參數，因此會詳細說明輸出。</span><span class="sxs-lookup"><span data-stu-id="c5b19-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="c5b19-120">參數</span><span class="sxs-lookup"><span data-stu-id="c5b19-120">PARAMETERS</span></span>

### <span data-ttu-id="c5b19-121">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="c5b19-121">-DetailedOutput</span></span>
<span data-ttu-id="c5b19-122">顯示輸出中的完整詳細資料。</span><span class="sxs-lookup"><span data-stu-id="c5b19-122">Displays full details in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b19-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="c5b19-123">-Name</span></span>
<span data-ttu-id="c5b19-124">指定要取得之警示規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5b19-124">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b19-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c5b19-125">-ResourceGroup</span></span>
<span data-ttu-id="c5b19-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="c5b19-126">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b19-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c5b19-127">-TargetResourceId</span></span>
<span data-ttu-id="c5b19-128">指定目標資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="c5b19-128">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using target resource uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b19-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5b19-129">-DefaultProfile</span></span>
<span data-ttu-id="c5b19-130">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="c5b19-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c5b19-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5b19-131">CommonParameters</span></span>
<span data-ttu-id="c5b19-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="c5b19-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5b19-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="c5b19-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5b19-134">輸入</span><span class="sxs-lookup"><span data-stu-id="c5b19-134">INPUTS</span></span>

## <span data-ttu-id="c5b19-135">輸出</span><span class="sxs-lookup"><span data-stu-id="c5b19-135">OUTPUTS</span></span>

### <span data-ttu-id="c5b19-136">[System.object]。清單 ' 1 [PSManagementItemDescriptor] OutputClasses.]</span><span class="sxs-lookup"><span data-stu-id="c5b19-136">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSManagementItemDescriptor]</span></span>

## <span data-ttu-id="c5b19-137">筆記</span><span class="sxs-lookup"><span data-stu-id="c5b19-137">NOTES</span></span>

## <span data-ttu-id="c5b19-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="c5b19-138">RELATED LINKS</span></span>

[<span data-ttu-id="c5b19-139">附加 AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="c5b19-139">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="c5b19-140">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="c5b19-140">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="c5b19-141">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="c5b19-141">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="c5b19-142">AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="c5b19-142">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="c5b19-143">移除-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="c5b19-143">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


