---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 315a44b986317157a0ada22955c04ea01726327a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100139882"
---
# <span data-ttu-id="bbc5f-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="bbc5f-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="bbc5f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="bbc5f-102">SYNOPSIS</span></span>
<span data-ttu-id="bbc5f-103">建立資料連線器。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-103">Create a Data Connector.</span></span>

## <span data-ttu-id="bbc5f-104">句法</span><span class="sxs-lookup"><span data-stu-id="bbc5f-104">SYNTAX</span></span>

### <span data-ttu-id="bbc5f-105">AzureActiveDirectory (預設) </span><span class="sxs-lookup"><span data-stu-id="bbc5f-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbc5f-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="bbc5f-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc5f-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="bbc5f-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc5f-108">AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="bbc5f-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc5f-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="bbc5f-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc5f-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="bbc5f-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc5f-111">Office365</span><span class="sxs-lookup"><span data-stu-id="bbc5f-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbc5f-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="bbc5f-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bbc5f-113">說明</span><span class="sxs-lookup"><span data-stu-id="bbc5f-113">DESCRIPTION</span></span>
<span data-ttu-id="bbc5f-114">**新的-AzSentinelAlertRule** Cmdlet 會在指定的工作區中建立) 的分析 (警示規則。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="bbc5f-115">您必須指定其中一個參數（例如，AzureActiveDirectory），以指定要建立的警示規則類型。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="bbc5f-116">每個類型都有不同的必要 paramaters。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="bbc5f-117">您可以使用 *Confirm* 參數和 $ConfirmPreference 的 Windows PowerShell 變數來控制 Cmdlet 是否提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="bbc5f-118">注意：並非入口網站中所有可用的資料連線器都是透過 API avaialble。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="bbc5f-119">示例</span><span class="sxs-lookup"><span data-stu-id="bbc5f-119">EXAMPLES</span></span>

### <span data-ttu-id="bbc5f-120">範例1</span><span class="sxs-lookup"><span data-stu-id="bbc5f-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="bbc5f-121">這個範例會在指定的工作區中建立 Azure 安全中心的 **DataConnector** ，然後將其儲存在 $DataConnector 變數中。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="bbc5f-122">範例2</span><span class="sxs-lookup"><span data-stu-id="bbc5f-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="bbc5f-123">這個範例會在指定的工作區中建立 Microsoft Cloud App Security 的 **DataConnector** ，然後將其儲存在 $DataConnector 變數中。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="bbc5f-124">參數</span><span class="sxs-lookup"><span data-stu-id="bbc5f-124">PARAMETERS</span></span>

### <span data-ttu-id="bbc5f-125">-提醒</span><span class="sxs-lookup"><span data-stu-id="bbc5f-125">-Alerts</span></span>
<span data-ttu-id="bbc5f-126">資料連線器通知</span><span class="sxs-lookup"><span data-stu-id="bbc5f-126">Data Connector Alerts</span></span>

```yaml
Type: System.String
Parameter Sets: AzureActiveDirectory, AzureAdvancedThreatProtection, AzureSecurityCenter, MicrosoftCloudAppSecurity, MicrosoftDefenderAdvancedThreatProtection
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-127">-AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="bbc5f-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="bbc5f-128">資料連線器 Amazon Web 服務雲端追蹤</span><span class="sxs-lookup"><span data-stu-id="bbc5f-128">Data Connector Amazon Web Services Cloud Trail</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="bbc5f-129">-AwsRoleArn</span></span>
<span data-ttu-id="bbc5f-130">資料連線器 AWS 角色 Arn</span><span class="sxs-lookup"><span data-stu-id="bbc5f-130">Data Connector AWS Role Arn</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-131">-AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="bbc5f-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="bbc5f-132">資料連線器 Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="bbc5f-132">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureActiveDirectory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="bbc5f-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="bbc5f-134">資料連線器 Azure 高級威脅防護</span><span class="sxs-lookup"><span data-stu-id="bbc5f-134">Data Connector Azure Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-135">-AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="bbc5f-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="bbc5f-136">資料連線器 Azure 安全中心</span><span class="sxs-lookup"><span data-stu-id="bbc5f-136">Data Connector Azure Security Center</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="bbc5f-137">-DataConnectorId</span></span>
<span data-ttu-id="bbc5f-138">資料連線器 Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="bbc5f-138">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbc5f-139">-DefaultProfile</span></span>
<span data-ttu-id="bbc5f-140">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbc5f-141">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="bbc5f-141">-DiscoveryLogs</span></span>
<span data-ttu-id="bbc5f-142">資料連線器探索記錄</span><span class="sxs-lookup"><span data-stu-id="bbc5f-142">Data Connector Discovery Logs</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-143">-Exchange</span><span class="sxs-lookup"><span data-stu-id="bbc5f-143">-Exchange</span></span>
<span data-ttu-id="bbc5f-144">資料連線器交換</span><span class="sxs-lookup"><span data-stu-id="bbc5f-144">Data Connector Exchange</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-145">-指標</span><span class="sxs-lookup"><span data-stu-id="bbc5f-145">-Indicators</span></span>
<span data-ttu-id="bbc5f-146">資料連線器標記</span><span class="sxs-lookup"><span data-stu-id="bbc5f-146">Data Connector Indicators</span></span>

```yaml
Type: System.String
Parameter Sets: ThreatIntelligence
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-147">-記錄</span><span class="sxs-lookup"><span data-stu-id="bbc5f-147">-Logs</span></span>
<span data-ttu-id="bbc5f-148">資料連線器記錄</span><span class="sxs-lookup"><span data-stu-id="bbc5f-148">Data Connector Logs</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="bbc5f-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="bbc5f-150">資料連線器 Microsoft 雲端 App 安全性</span><span class="sxs-lookup"><span data-stu-id="bbc5f-150">Data Connector Microsoft Cloud App Security</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="bbc5f-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="bbc5f-152">資料連線器 Microsoft Defender 高級威脅防護</span><span class="sxs-lookup"><span data-stu-id="bbc5f-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftDefenderAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-153">-Office365</span><span class="sxs-lookup"><span data-stu-id="bbc5f-153">-Office365</span></span>
<span data-ttu-id="bbc5f-154">資料連線器 Office 365</span><span class="sxs-lookup"><span data-stu-id="bbc5f-154">Data Connector Office 365</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Office365
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbc5f-155">-ResourceGroupName</span></span>
<span data-ttu-id="bbc5f-156">資料連線器 Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="bbc5f-156">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-157">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="bbc5f-157">-SharePoint</span></span>
<span data-ttu-id="bbc5f-158">資料連線器 SharePoint</span><span class="sxs-lookup"><span data-stu-id="bbc5f-158">Data Connector SharePoint</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bbc5f-159">-SubscriptionId</span></span>
<span data-ttu-id="bbc5f-160">資料連線器訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="bbc5f-160">Data connector Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="bbc5f-161">-ThreatIntelligence</span></span>
<span data-ttu-id="bbc5f-162">資料連線器威脅情報</span><span class="sxs-lookup"><span data-stu-id="bbc5f-162">Data Connector Threat Intelligence</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ThreatIntelligence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-163">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bbc5f-163">-WorkspaceName</span></span>
<span data-ttu-id="bbc5f-164">資料連線器 Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="bbc5f-164">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-165">-確認</span><span class="sxs-lookup"><span data-stu-id="bbc5f-165">-Confirm</span></span>
<span data-ttu-id="bbc5f-166">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbc5f-167">-WhatIf</span></span>
<span data-ttu-id="bbc5f-168">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bbc5f-169">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbc5f-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbc5f-170">CommonParameters</span></span>
<span data-ttu-id="bbc5f-171">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbc5f-172">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="bbc5f-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbc5f-173">輸入</span><span class="sxs-lookup"><span data-stu-id="bbc5f-173">INPUTS</span></span>

### <span data-ttu-id="bbc5f-174">所有</span><span class="sxs-lookup"><span data-stu-id="bbc5f-174">None</span></span>
## <span data-ttu-id="bbc5f-175">輸出</span><span class="sxs-lookup"><span data-stu-id="bbc5f-175">OUTPUTS</span></span>

### <span data-ttu-id="bbc5f-176">SecurityInsights DataConnectors. PSSentinelDataConnector （）</span><span class="sxs-lookup"><span data-stu-id="bbc5f-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="bbc5f-177">筆記</span><span class="sxs-lookup"><span data-stu-id="bbc5f-177">NOTES</span></span>

## <span data-ttu-id="bbc5f-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="bbc5f-178">RELATED LINKS</span></span>
