---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
ms.openlocfilehash: fe763bcf6ff4aeeeedb3ff0dcb0c2ebd5c4b45cc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/15/2020
ms.locfileid: "93802482"
---
# <span data-ttu-id="cec1c-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="cec1c-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="cec1c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cec1c-102">SYNOPSIS</span></span>
<span data-ttu-id="cec1c-103">取得警示規則。</span><span class="sxs-lookup"><span data-stu-id="cec1c-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cec1c-104">句法</span><span class="sxs-lookup"><span data-stu-id="cec1c-104">SYNTAX</span></span>

### <span data-ttu-id="cec1c-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cec1c-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cec1c-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="cec1c-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cec1c-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="cec1c-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cec1c-108">說明</span><span class="sxs-lookup"><span data-stu-id="cec1c-108">DESCRIPTION</span></span>
<span data-ttu-id="cec1c-109">AzureRmAlertRule Cmdlet 會根據其名稱或 URI，或從指定的資源群組取得所有警示規則，來 **取得** 警示規則。</span><span class="sxs-lookup"><span data-stu-id="cec1c-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="cec1c-110">示例</span><span class="sxs-lookup"><span data-stu-id="cec1c-110">EXAMPLES</span></span>

### <span data-ttu-id="cec1c-111">範例1：取得資源群組的警示規則</span><span class="sxs-lookup"><span data-stu-id="cec1c-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="cec1c-112">這個命令會取得名為 [預設-Web CentralUS] 的資源群組的所有通知規則。</span><span class="sxs-lookup"><span data-stu-id="cec1c-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="cec1c-113">輸出不會包含有關規則的詳細資料，因為未指定 *DetailedOutput* 參數。</span><span class="sxs-lookup"><span data-stu-id="cec1c-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="cec1c-114">範例2：依名稱取得警示規則</span><span class="sxs-lookup"><span data-stu-id="cec1c-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="cec1c-115">這個命令會取得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。</span><span class="sxs-lookup"><span data-stu-id="cec1c-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="cec1c-116">因為未指定 *DetailedOutput* 參數，所以輸出只包含有關警示規則的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="cec1c-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="cec1c-117">範例3：透過名稱取得警示規則及詳細的輸出</span><span class="sxs-lookup"><span data-stu-id="cec1c-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="cec1c-118">這個命令會取得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。</span><span class="sxs-lookup"><span data-stu-id="cec1c-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="cec1c-119">已指定 *DetailedOutput* 參數，因此會詳細說明輸出。</span><span class="sxs-lookup"><span data-stu-id="cec1c-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="cec1c-120">參數</span><span class="sxs-lookup"><span data-stu-id="cec1c-120">PARAMETERS</span></span>

### <span data-ttu-id="cec1c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cec1c-121">-DefaultProfile</span></span>
<span data-ttu-id="cec1c-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cec1c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cec1c-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="cec1c-123">-DetailedOutput</span></span>
<span data-ttu-id="cec1c-124">顯示輸出中的完整詳細資料。</span><span class="sxs-lookup"><span data-stu-id="cec1c-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="cec1c-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="cec1c-125">-Name</span></span>
<span data-ttu-id="cec1c-126">指定要取得之警示規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="cec1c-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="cec1c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cec1c-127">-ResourceGroupName</span></span>
<span data-ttu-id="cec1c-128">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cec1c-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="cec1c-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="cec1c-129">-TargetResourceId</span></span>
<span data-ttu-id="cec1c-130">指定目標資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="cec1c-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="cec1c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec1c-131">CommonParameters</span></span>
<span data-ttu-id="cec1c-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cec1c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cec1c-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cec1c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec1c-134">輸入</span><span class="sxs-lookup"><span data-stu-id="cec1c-134">INPUTS</span></span>

### <span data-ttu-id="cec1c-135">System.object</span><span class="sxs-lookup"><span data-stu-id="cec1c-135">System.String</span></span>

### <span data-ttu-id="cec1c-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="cec1c-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cec1c-137">輸出</span><span class="sxs-lookup"><span data-stu-id="cec1c-137">OUTPUTS</span></span>

### <span data-ttu-id="cec1c-138">PSAlertRule 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="cec1c-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="cec1c-139">筆記</span><span class="sxs-lookup"><span data-stu-id="cec1c-139">NOTES</span></span>

## <span data-ttu-id="cec1c-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="cec1c-140">RELATED LINKS</span></span>



[<span data-ttu-id="cec1c-141">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="cec1c-141">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="cec1c-142">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="cec1c-142">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="cec1c-143">AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="cec1c-143">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="cec1c-144">移除-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="cec1c-144">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


