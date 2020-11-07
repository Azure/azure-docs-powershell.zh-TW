---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 01774d80ce422c1ac0a48df61d44328b6b5b0105
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794629"
---
# <span data-ttu-id="4e107-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="4e107-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="4e107-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4e107-102">SYNOPSIS</span></span>
<span data-ttu-id="4e107-103">取得警示規則。</span><span class="sxs-lookup"><span data-stu-id="4e107-103">Gets alert rules.</span></span>

## <span data-ttu-id="4e107-104">句法</span><span class="sxs-lookup"><span data-stu-id="4e107-104">SYNTAX</span></span>

### <span data-ttu-id="4e107-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4e107-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4e107-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="4e107-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e107-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="4e107-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e107-108">說明</span><span class="sxs-lookup"><span data-stu-id="4e107-108">DESCRIPTION</span></span>
<span data-ttu-id="4e107-109">AzAlertRule Cmdlet 會根據其名稱或 URI，或從指定的資源群組取得所有警示規則，來 **取得** 警示規則。</span><span class="sxs-lookup"><span data-stu-id="4e107-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="4e107-110">示例</span><span class="sxs-lookup"><span data-stu-id="4e107-110">EXAMPLES</span></span>

### <span data-ttu-id="4e107-111">範例1：取得資源群組的警示規則</span><span class="sxs-lookup"><span data-stu-id="4e107-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="4e107-112">這個命令會取得名為 [預設-Web CentralUS] 的資源群組的所有通知規則。</span><span class="sxs-lookup"><span data-stu-id="4e107-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="4e107-113">輸出不會包含有關規則的詳細資料，因為未指定 *DetailedOutput* 參數。</span><span class="sxs-lookup"><span data-stu-id="4e107-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="4e107-114">範例2：依名稱取得警示規則</span><span class="sxs-lookup"><span data-stu-id="4e107-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="4e107-115">這個命令會取得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。</span><span class="sxs-lookup"><span data-stu-id="4e107-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="4e107-116">因為未指定 *DetailedOutput* 參數，所以輸出只包含有關警示規則的基本資訊。</span><span class="sxs-lookup"><span data-stu-id="4e107-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="4e107-117">範例3：透過名稱取得警示規則及詳細的輸出</span><span class="sxs-lookup"><span data-stu-id="4e107-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="4e107-118">這個命令會取得名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。</span><span class="sxs-lookup"><span data-stu-id="4e107-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="4e107-119">已指定 *DetailedOutput* 參數，因此會詳細說明輸出。</span><span class="sxs-lookup"><span data-stu-id="4e107-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="4e107-120">參數</span><span class="sxs-lookup"><span data-stu-id="4e107-120">PARAMETERS</span></span>

### <span data-ttu-id="4e107-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e107-121">-DefaultProfile</span></span>
<span data-ttu-id="4e107-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4e107-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4e107-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="4e107-123">-DetailedOutput</span></span>
<span data-ttu-id="4e107-124">顯示輸出中的完整詳細資料。</span><span class="sxs-lookup"><span data-stu-id="4e107-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="4e107-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="4e107-125">-Name</span></span>
<span data-ttu-id="4e107-126">指定要取得之警示規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e107-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="4e107-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e107-127">-ResourceGroupName</span></span>
<span data-ttu-id="4e107-128">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4e107-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="4e107-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="4e107-129">-TargetResourceId</span></span>
<span data-ttu-id="4e107-130">指定目標資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="4e107-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="4e107-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e107-131">CommonParameters</span></span>
<span data-ttu-id="4e107-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4e107-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e107-133">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="4e107-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e107-134">輸入</span><span class="sxs-lookup"><span data-stu-id="4e107-134">INPUTS</span></span>

### <span data-ttu-id="4e107-135">System.object</span><span class="sxs-lookup"><span data-stu-id="4e107-135">System.String</span></span>

### <span data-ttu-id="4e107-136">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="4e107-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4e107-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4e107-137">OUTPUTS</span></span>

### <span data-ttu-id="4e107-138">PSAlertRule 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="4e107-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="4e107-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4e107-139">NOTES</span></span>

## <span data-ttu-id="4e107-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4e107-140">RELATED LINKS</span></span>

[<span data-ttu-id="4e107-141">附加 AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="4e107-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="4e107-142">附加 AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="4e107-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="4e107-143">附加 AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="4e107-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="4e107-144">AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="4e107-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="4e107-145">移除-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="4e107-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


