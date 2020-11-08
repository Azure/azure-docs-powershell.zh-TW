---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: f515d7db58e75cc916478e07edb4e34233201a4d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140050"
---
# <span data-ttu-id="9ba9b-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="9ba9b-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="9ba9b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9ba9b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba9b-103">取得警示規則。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-103">Gets alert rules.</span></span>

## <span data-ttu-id="9ba9b-104">句法</span><span class="sxs-lookup"><span data-stu-id="9ba9b-104">SYNTAX</span></span>

### <span data-ttu-id="9ba9b-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9ba9b-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ba9b-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="9ba9b-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ba9b-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="9ba9b-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9ba9b-108">說明</span><span class="sxs-lookup"><span data-stu-id="9ba9b-108">DESCRIPTION</span></span>
<span data-ttu-id="9ba9b-109">AzAlertRule Cmdlet 會根據其名稱或 URI，或從指定的資源群組取得所有警示規則，來 **取得** 警示規則。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="9ba9b-110">示例</span><span class="sxs-lookup"><span data-stu-id="9ba9b-110">EXAMPLES</span></span>

### <span data-ttu-id="9ba9b-111">範例1：取得資源群組的警示規則</span><span class="sxs-lookup"><span data-stu-id="9ba9b-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="9ba9b-112">這個命令會取得名為 [預設-Web CentralUS] 的資源群組的所有通知規則。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="9ba9b-113">輸出不會包含有關規則的詳細資料，因為未指定 *DetailedOutput* 參數。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="9ba9b-114">範例2：依名稱取得警示規則</span><span class="sxs-lookup"><span data-stu-id="9ba9b-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="9ba9b-115">這個命令會取得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="9ba9b-116">因為未指定 *DetailedOutput* 參數，所以輸出只包含有關警示規則的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="9ba9b-117">範例3：透過名稱取得警示規則及詳細的輸出</span><span class="sxs-lookup"><span data-stu-id="9ba9b-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="9ba9b-118">這個命令會取得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="9ba9b-119">已指定 *DetailedOutput* 參數，因此會詳細說明輸出。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="9ba9b-120">參數</span><span class="sxs-lookup"><span data-stu-id="9ba9b-120">PARAMETERS</span></span>

### <span data-ttu-id="9ba9b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba9b-121">-DefaultProfile</span></span>
<span data-ttu-id="9ba9b-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="9ba9b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9ba9b-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="9ba9b-123">-DetailedOutput</span></span>
<span data-ttu-id="9ba9b-124">顯示輸出中的完整詳細資料。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="9ba9b-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="9ba9b-125">-Name</span></span>
<span data-ttu-id="9ba9b-126">指定要取得之警示規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="9ba9b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba9b-127">-ResourceGroupName</span></span>
<span data-ttu-id="9ba9b-128">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="9ba9b-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9ba9b-129">-TargetResourceId</span></span>
<span data-ttu-id="9ba9b-130">指定目標資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="9ba9b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba9b-131">CommonParameters</span></span>
<span data-ttu-id="9ba9b-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba9b-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba9b-134">輸入</span><span class="sxs-lookup"><span data-stu-id="9ba9b-134">INPUTS</span></span>

### <span data-ttu-id="9ba9b-135">System.object</span><span class="sxs-lookup"><span data-stu-id="9ba9b-135">System.String</span></span>

### <span data-ttu-id="9ba9b-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="9ba9b-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9ba9b-137">輸出</span><span class="sxs-lookup"><span data-stu-id="9ba9b-137">OUTPUTS</span></span>

### <span data-ttu-id="9ba9b-138">PSAlertRule 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="9ba9b-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="9ba9b-139">筆記</span><span class="sxs-lookup"><span data-stu-id="9ba9b-139">NOTES</span></span>

## <span data-ttu-id="9ba9b-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="9ba9b-140">RELATED LINKS</span></span>

[<span data-ttu-id="9ba9b-141">附加 AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="9ba9b-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="9ba9b-142">附加 AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="9ba9b-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="9ba9b-143">附加 AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="9ba9b-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="9ba9b-144">AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="9ba9b-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="9ba9b-145">移除-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="9ba9b-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


