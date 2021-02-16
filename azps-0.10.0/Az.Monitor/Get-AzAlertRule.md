---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: c48a3fcf2441c7818d087e42b1271939963936ce
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399051"
---
# <span data-ttu-id="25e22-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="25e22-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="25e22-102">簡介</span><span class="sxs-lookup"><span data-stu-id="25e22-102">SYNOPSIS</span></span>
<span data-ttu-id="25e22-103">獲得警示規則。</span><span class="sxs-lookup"><span data-stu-id="25e22-103">Gets alert rules.</span></span>

## <span data-ttu-id="25e22-104">語法</span><span class="sxs-lookup"><span data-stu-id="25e22-104">SYNTAX</span></span>

### <span data-ttu-id="25e22-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="25e22-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="25e22-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="25e22-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="25e22-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="25e22-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25e22-108">描述</span><span class="sxs-lookup"><span data-stu-id="25e22-108">DESCRIPTION</span></span>
<span data-ttu-id="25e22-109">**Get-AzAlertRule** Cmdlet 會依名稱或 URI 或指定資源群組的所有警示規則，取得警示規則。</span><span class="sxs-lookup"><span data-stu-id="25e22-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="25e22-110">例子</span><span class="sxs-lookup"><span data-stu-id="25e22-110">EXAMPLES</span></span>

### <span data-ttu-id="25e22-111">範例 1：取得資源群組的警示規則</span><span class="sxs-lookup"><span data-stu-id="25e22-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="25e22-112">此命令會針對名為 Default-Web-CentralUS 的資源群組，獲得所有警示規則。</span><span class="sxs-lookup"><span data-stu-id="25e22-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="25e22-113">輸出不會包含規則的詳細資料，因為 *未指定 DetailedOutput* 參數。</span><span class="sxs-lookup"><span data-stu-id="25e22-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="25e22-114">範例 2：依名稱取得提醒規則</span><span class="sxs-lookup"><span data-stu-id="25e22-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="25e22-115">此命令會獲得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。</span><span class="sxs-lookup"><span data-stu-id="25e22-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="25e22-116">由於 *未指定 DetailedOutput* 參數，因此輸出只會包含警示規則的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="25e22-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="25e22-117">範例 3：依名稱取得具有詳細輸出的警示規則</span><span class="sxs-lookup"><span data-stu-id="25e22-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="25e22-118">此命令會獲得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。</span><span class="sxs-lookup"><span data-stu-id="25e22-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="25e22-119">*指定 DetailedOutput* 參數，因此輸出會詳述。</span><span class="sxs-lookup"><span data-stu-id="25e22-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="25e22-120">參數</span><span class="sxs-lookup"><span data-stu-id="25e22-120">PARAMETERS</span></span>

### <span data-ttu-id="25e22-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e22-121">-DefaultProfile</span></span>
<span data-ttu-id="25e22-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="25e22-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25e22-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="25e22-123">-DetailedOutput</span></span>
<span data-ttu-id="25e22-124">在輸出中顯示完整詳細資料。</span><span class="sxs-lookup"><span data-stu-id="25e22-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="25e22-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="25e22-125">-Name</span></span>
<span data-ttu-id="25e22-126">指定要取得之警示規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="25e22-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="25e22-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e22-127">-ResourceGroupName</span></span>
<span data-ttu-id="25e22-128">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="25e22-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="25e22-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="25e22-129">-TargetResourceId</span></span>
<span data-ttu-id="25e22-130">指定目標資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="25e22-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="25e22-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e22-131">CommonParameters</span></span>
<span data-ttu-id="25e22-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="25e22-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e22-133">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25e22-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e22-134">輸入</span><span class="sxs-lookup"><span data-stu-id="25e22-134">INPUTS</span></span>

### <span data-ttu-id="25e22-135">System.String</span><span class="sxs-lookup"><span data-stu-id="25e22-135">System.String</span></span>

### <span data-ttu-id="25e22-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="25e22-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="25e22-137">輸出</span><span class="sxs-lookup"><span data-stu-id="25e22-137">OUTPUTS</span></span>

### <span data-ttu-id="25e22-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="25e22-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="25e22-139">筆記</span><span class="sxs-lookup"><span data-stu-id="25e22-139">NOTES</span></span>

## <span data-ttu-id="25e22-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="25e22-140">RELATED LINKS</span></span>


[<span data-ttu-id="25e22-141">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="25e22-141">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="25e22-142">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="25e22-142">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="25e22-143">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="25e22-143">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="25e22-144">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="25e22-144">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


