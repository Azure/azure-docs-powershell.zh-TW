---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 11A521DF-E77C-4D6F-A2D9-1C2CF8972F57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
ms.openlocfilehash: 38644018ac9ae19d1c413123ca071f564d336fa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456612"
---
# <span data-ttu-id="b65f1-101">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="b65f1-101">Add-AzureRmLogAlertRule</span></span>

## <span data-ttu-id="b65f1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="b65f1-102">SYNOPSIS</span></span>
<span data-ttu-id="b65f1-103">新增或取代記錄提醒規則。</span><span class="sxs-lookup"><span data-stu-id="b65f1-103">Adds or replaces a log alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b65f1-104">句法</span><span class="sxs-lookup"><span data-stu-id="b65f1-104">SYNTAX</span></span>

```
Add-AzureRmLogAlertRule [-TargetResourceGroup <String>] [-TargetResourceId <String>] [-Level <String>]
 -OperationName <String> [-TargetResourceProvider <String>] [-Status <String>] [-SubStatus <String>]
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b65f1-105">說明</span><span class="sxs-lookup"><span data-stu-id="b65f1-105">DESCRIPTION</span></span>
<span data-ttu-id="b65f1-106">**AzureRmLogAlertRule** Cmdlet 會新增或取代事件警報規則。</span><span class="sxs-lookup"><span data-stu-id="b65f1-106">The **Add-AzureRmLogAlertRule** cmdlet adds or replaces an event alert rule.</span></span>
<span data-ttu-id="b65f1-107">新增的規則與資源群組相關聯，且具有名稱。</span><span class="sxs-lookup"><span data-stu-id="b65f1-107">The added rule is associated with a resource group and has a name.</span></span>

<span data-ttu-id="b65f1-108">如先前版本所宣告：在 **未來版本中，將會棄用 AzureRMLogAlertRule Cmdlet。**</span><span class="sxs-lookup"><span data-stu-id="b65f1-108">As announced in previous releases: **Add-AzureRMLogAlertRule cmdlet will be deprecated in a future release.**</span></span> <span data-ttu-id="b65f1-109">2017年10月1日之後，使用此 Cmdlet 將不會有任何作用，因為此功能正在轉換為活動記錄通知。</span><span class="sxs-lookup"><span data-stu-id="b65f1-109">After October 1st 2017 using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="b65f1-110">如需 **_https://aka.ms/migratemealerts_** 詳細資訊，請參閱。</span><span class="sxs-lookup"><span data-stu-id="b65f1-110">Please see **_https://aka.ms/migratemealerts_** for more information.</span></span>

## <span data-ttu-id="b65f1-111">示例</span><span class="sxs-lookup"><span data-stu-id="b65f1-111">EXAMPLES</span></span>

### <span data-ttu-id="b65f1-112">範例1：新增記錄提醒規則</span><span class="sxs-lookup"><span data-stu-id="b65f1-112">Example 1: Add a log alert rule</span></span>
```
PS C:\>Add-AzureRmLogAlertRule -Name "logRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -OperationName "Create" -TargetResourceId "/subscriptions/abbfb07c-6c93-40be-bc9b-4f0deba32f4c/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/misitiooeltuyo" -Description "My log rule"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="b65f1-113">這個命令會新增或更新以事件為基礎的警示規則。</span><span class="sxs-lookup"><span data-stu-id="b65f1-113">This command adds or updates an event-based alert rule.</span></span>

## <span data-ttu-id="b65f1-114">參數</span><span class="sxs-lookup"><span data-stu-id="b65f1-114">PARAMETERS</span></span>

### <span data-ttu-id="b65f1-115">-動作</span><span class="sxs-lookup"><span data-stu-id="b65f1-115">-Actions</span></span>
<span data-ttu-id="b65f1-116">指定以逗號分隔的動作清單。</span><span class="sxs-lookup"><span data-stu-id="b65f1-116">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65f1-117">-描述</span><span class="sxs-lookup"><span data-stu-id="b65f1-117">-Description</span></span>
<span data-ttu-id="b65f1-118">指定規則的描述。</span><span class="sxs-lookup"><span data-stu-id="b65f1-118">Specifies a description of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65f1-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="b65f1-119">-DisableRule</span></span>
<span data-ttu-id="b65f1-120">停用規則。</span><span class="sxs-lookup"><span data-stu-id="b65f1-120">Disables a rule.</span></span>
<span data-ttu-id="b65f1-121">如果您沒有指定此參數，則會啟用規則。</span><span class="sxs-lookup"><span data-stu-id="b65f1-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="b65f1-122">層級</span><span class="sxs-lookup"><span data-stu-id="b65f1-122">-Level</span></span>
<span data-ttu-id="b65f1-123">指定規則監視的事件層級。</span><span class="sxs-lookup"><span data-stu-id="b65f1-123">Specifies the level of the event the rule is monitoring.</span></span>
<span data-ttu-id="b65f1-124">僅針對事件規則指定此參數。</span><span class="sxs-lookup"><span data-stu-id="b65f1-124">Specify this parameter only for event-based rules.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65f1-125">-位置</span><span class="sxs-lookup"><span data-stu-id="b65f1-125">-Location</span></span>
<span data-ttu-id="b65f1-126">指定規則的位置。</span><span class="sxs-lookup"><span data-stu-id="b65f1-126">Specifies the location for the rule.</span></span>

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

### <span data-ttu-id="b65f1-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="b65f1-127">-Name</span></span>
<span data-ttu-id="b65f1-128">指定規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="b65f1-128">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="b65f1-129">-OperationName</span><span class="sxs-lookup"><span data-stu-id="b65f1-129">-OperationName</span></span>
<span data-ttu-id="b65f1-130">指定作業的名稱。</span><span class="sxs-lookup"><span data-stu-id="b65f1-130">Specifies the name of the operation.</span></span>

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

### <span data-ttu-id="b65f1-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b65f1-131">-ResourceGroup</span></span>
<span data-ttu-id="b65f1-132">指定規則之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b65f1-132">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="b65f1-133">-狀態</span><span class="sxs-lookup"><span data-stu-id="b65f1-133">-Status</span></span>
<span data-ttu-id="b65f1-134">指定狀態。</span><span class="sxs-lookup"><span data-stu-id="b65f1-134">Specifies the status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65f1-135">-子狀態</span><span class="sxs-lookup"><span data-stu-id="b65f1-135">-SubStatus</span></span>
<span data-ttu-id="b65f1-136">指定子狀態。</span><span class="sxs-lookup"><span data-stu-id="b65f1-136">Specifies the substatus.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65f1-137">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="b65f1-137">-TargetResourceGroup</span></span>
<span data-ttu-id="b65f1-138">指定規則所監視之資源的資源群組。</span><span class="sxs-lookup"><span data-stu-id="b65f1-138">Specifies the resource group of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65f1-139">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b65f1-139">-TargetResourceId</span></span>
<span data-ttu-id="b65f1-140">指定規則所監視之資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b65f1-140">Specifies the ID of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65f1-141">-TargetResourceProvider</span><span class="sxs-lookup"><span data-stu-id="b65f1-141">-TargetResourceProvider</span></span>
<span data-ttu-id="b65f1-142">指定規則所監視之資源的資源提供者。</span><span class="sxs-lookup"><span data-stu-id="b65f1-142">Specifies the resource provider of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65f1-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b65f1-143">-DefaultProfile</span></span>
<span data-ttu-id="b65f1-144">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="b65f1-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b65f1-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65f1-145">CommonParameters</span></span>
<span data-ttu-id="b65f1-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="b65f1-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65f1-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="b65f1-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65f1-148">輸入</span><span class="sxs-lookup"><span data-stu-id="b65f1-148">INPUTS</span></span>

## <span data-ttu-id="b65f1-149">輸出</span><span class="sxs-lookup"><span data-stu-id="b65f1-149">OUTPUTS</span></span>

### <span data-ttu-id="b65f1-150">PSAddAlertRuleOperationResponse 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="b65f1-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="b65f1-151">筆記</span><span class="sxs-lookup"><span data-stu-id="b65f1-151">NOTES</span></span>

## <span data-ttu-id="b65f1-152">相關連結</span><span class="sxs-lookup"><span data-stu-id="b65f1-152">RELATED LINKS</span></span>

[<span data-ttu-id="b65f1-153">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b65f1-153">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="b65f1-154">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b65f1-154">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="b65f1-155">AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="b65f1-155">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="b65f1-156">新-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="b65f1-156">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="b65f1-157">新-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="b65f1-157">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


