---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 672ab7a3c802ae8165b29c69ffb6c3f63310cc89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449808"
---
# <span data-ttu-id="f62df-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="f62df-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="f62df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f62df-102">SYNOPSIS</span></span>
<span data-ttu-id="f62df-103">取得警示規則。</span><span class="sxs-lookup"><span data-stu-id="f62df-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f62df-104">句法</span><span class="sxs-lookup"><span data-stu-id="f62df-104">SYNTAX</span></span>

### <span data-ttu-id="f62df-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f62df-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f62df-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="f62df-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f62df-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="f62df-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f62df-108">說明</span><span class="sxs-lookup"><span data-stu-id="f62df-108">DESCRIPTION</span></span>
<span data-ttu-id="f62df-109">AzureRmAlertRule Cmdlet 會根據其名稱或 URI，或從指定的資源群組取得所有警示規則，來 **取得** 警示規則。</span><span class="sxs-lookup"><span data-stu-id="f62df-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="f62df-110">示例</span><span class="sxs-lookup"><span data-stu-id="f62df-110">EXAMPLES</span></span>

### <span data-ttu-id="f62df-111">範例1：取得資源群組的警示規則</span><span class="sxs-lookup"><span data-stu-id="f62df-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="f62df-112">這個命令會取得名為 [預設-Web CentralUS] 的資源群組的所有通知規則。</span><span class="sxs-lookup"><span data-stu-id="f62df-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="f62df-113">輸出不會包含有關規則的詳細資料，因為未指定 *DetailedOutput* 參數。</span><span class="sxs-lookup"><span data-stu-id="f62df-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="f62df-114">範例2：依名稱取得警示規則</span><span class="sxs-lookup"><span data-stu-id="f62df-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="f62df-115">這個命令會取得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。</span><span class="sxs-lookup"><span data-stu-id="f62df-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="f62df-116">因為未指定 *DetailedOutput* 參數，所以輸出只包含有關警示規則的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="f62df-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="f62df-117">範例3：透過名稱取得警示規則及詳細的輸出</span><span class="sxs-lookup"><span data-stu-id="f62df-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="f62df-118">這個命令會取得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。</span><span class="sxs-lookup"><span data-stu-id="f62df-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="f62df-119">已指定 *DetailedOutput* 參數，因此會詳細說明輸出。</span><span class="sxs-lookup"><span data-stu-id="f62df-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="f62df-120">參數</span><span class="sxs-lookup"><span data-stu-id="f62df-120">PARAMETERS</span></span>

### <span data-ttu-id="f62df-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f62df-121">-DefaultProfile</span></span>
<span data-ttu-id="f62df-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f62df-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f62df-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="f62df-123">-DetailedOutput</span></span>
<span data-ttu-id="f62df-124">顯示輸出中的完整詳細資料。</span><span class="sxs-lookup"><span data-stu-id="f62df-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="f62df-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="f62df-125">-Name</span></span>
<span data-ttu-id="f62df-126">指定要取得之警示規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="f62df-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f62df-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f62df-127">-ResourceGroupName</span></span>
<span data-ttu-id="f62df-128">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f62df-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f62df-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f62df-129">-TargetResourceId</span></span>
<span data-ttu-id="f62df-130">指定目標資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f62df-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f62df-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f62df-131">CommonParameters</span></span>
<span data-ttu-id="f62df-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f62df-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f62df-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f62df-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f62df-134">輸入</span><span class="sxs-lookup"><span data-stu-id="f62df-134">INPUTS</span></span>

### <span data-ttu-id="f62df-135">System.object</span><span class="sxs-lookup"><span data-stu-id="f62df-135">System.String</span></span>

### <span data-ttu-id="f62df-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="f62df-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f62df-137">輸出</span><span class="sxs-lookup"><span data-stu-id="f62df-137">OUTPUTS</span></span>

### <span data-ttu-id="f62df-138">PSAlertRule 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="f62df-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="f62df-139">筆記</span><span class="sxs-lookup"><span data-stu-id="f62df-139">NOTES</span></span>

## <span data-ttu-id="f62df-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="f62df-140">RELATED LINKS</span></span>

[<span data-ttu-id="f62df-141">附加 AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="f62df-141">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="f62df-142">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="f62df-142">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="f62df-143">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="f62df-143">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="f62df-144">AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="f62df-144">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="f62df-145">移除-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="f62df-145">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


