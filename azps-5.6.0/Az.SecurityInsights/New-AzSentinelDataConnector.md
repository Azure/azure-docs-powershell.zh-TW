---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 7eb4675e44a252feec913b531a30f9062f6b791b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908009"
---
# <span data-ttu-id="5cfa7-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="5cfa7-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="5cfa7-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5cfa7-102">SYNOPSIS</span></span>
<span data-ttu-id="5cfa7-103">建立資料連線器。</span><span class="sxs-lookup"><span data-stu-id="5cfa7-103">Create a Data Connector.</span></span>

## <span data-ttu-id="5cfa7-104">語法</span><span class="sxs-lookup"><span data-stu-id="5cfa7-104">SYNTAX</span></span>

### <span data-ttu-id="5cfa7-105">AzureActiveDirectory (預設) </span><span class="sxs-lookup"><span data-stu-id="5cfa7-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cfa7-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5cfa7-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cfa7-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="5cfa7-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cfa7-108">AmazonWebServicesCloudTcloud</span><span class="sxs-lookup"><span data-stu-id="5cfa7-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cfa7-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="5cfa7-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cfa7-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5cfa7-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cfa7-111">Office365</span><span class="sxs-lookup"><span data-stu-id="5cfa7-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5cfa7-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="5cfa7-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5cfa7-113">描述</span><span class="sxs-lookup"><span data-stu-id="5cfa7-113">DESCRIPTION</span></span>
<span data-ttu-id="5cfa7-114">**New-AzSentinelAlertRule** Cmdlet 會建立 (工作區) 警示規則。</span><span class="sxs-lookup"><span data-stu-id="5cfa7-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="5cfa7-115">您必須指定其中一個參數 ，例如 -AzureActiveDirectory，以指定要建立的警示規則類型。</span><span class="sxs-lookup"><span data-stu-id="5cfa7-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="5cfa7-116">每種類型都有不同的所需參數。</span><span class="sxs-lookup"><span data-stu-id="5cfa7-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="5cfa7-117">您可以使用確認 *參數$ConfirmPreference* Windows PowerShell 變數來控制 Cmdlet 是否提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5cfa7-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="5cfa7-118">注意：並非入口網站中所有可用的資料連線器都可透過 API 進行連接。</span><span class="sxs-lookup"><span data-stu-id="5cfa7-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="5cfa7-119">例子</span><span class="sxs-lookup"><span data-stu-id="5cfa7-119">EXAMPLES</span></span>

### <span data-ttu-id="5cfa7-120">範例 1</span><span class="sxs-lookup"><span data-stu-id="5cfa7-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="5cfa7-121">此範例會針對指定的工作區建立 Azure 資訊安全中心的 **DataConnector，** 然後將它儲存在 $DataConnector 變數中。</span><span class="sxs-lookup"><span data-stu-id="5cfa7-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="5cfa7-122">範例 2</span><span class="sxs-lookup"><span data-stu-id="5cfa7-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="5cfa7-123">此範例會為 Microsoft Cloud App Security 在指定的工作區中建立 **DataConnector，** 然後將它儲存在$DataConnector變數。</span><span class="sxs-lookup"><span data-stu-id="5cfa7-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="5cfa7-124">參數</span><span class="sxs-lookup"><span data-stu-id="5cfa7-124">PARAMETERS</span></span>

### <span data-ttu-id="5cfa7-125">-通知</span><span class="sxs-lookup"><span data-stu-id="5cfa7-125">-Alerts</span></span>
<span data-ttu-id="5cfa7-126">資料連線器通知</span><span class="sxs-lookup"><span data-stu-id="5cfa7-126">Data Connector Alerts</span></span>

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

### <span data-ttu-id="5cfa7-127">-AmazonWebServicesCloudTcloud</span><span class="sxs-lookup"><span data-stu-id="5cfa7-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="5cfa7-128">Data Connector Amazon Web Services Cloud Trail</span><span class="sxs-lookup"><span data-stu-id="5cfa7-128">Data Connector Amazon Web Services Cloud Trail</span></span>

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

### <span data-ttu-id="5cfa7-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="5cfa7-129">-AwsRoleArn</span></span>
<span data-ttu-id="5cfa7-130">Data Connector AWS 角色 Arn</span><span class="sxs-lookup"><span data-stu-id="5cfa7-130">Data Connector AWS Role Arn</span></span>

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

### <span data-ttu-id="5cfa7-131">-AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="5cfa7-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="5cfa7-132">資料連線器 Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5cfa7-132">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="5cfa7-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5cfa7-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="5cfa7-134">Data Connector Azure 進位威脅防護</span><span class="sxs-lookup"><span data-stu-id="5cfa7-134">Data Connector Azure Advanced Threat Protection</span></span>

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

### <span data-ttu-id="5cfa7-135">-AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="5cfa7-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="5cfa7-136">資料連線器 Azure 資訊安全中心</span><span class="sxs-lookup"><span data-stu-id="5cfa7-136">Data Connector Azure Security Center</span></span>

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

### <span data-ttu-id="5cfa7-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="5cfa7-137">-DataConnectorId</span></span>
<span data-ttu-id="5cfa7-138">資料連線器 Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5cfa7-138">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="5cfa7-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cfa7-139">-DefaultProfile</span></span>
<span data-ttu-id="5cfa7-140">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="5cfa7-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cfa7-141">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="5cfa7-141">-DiscoveryLogs</span></span>
<span data-ttu-id="5cfa7-142">資料連線器探索記錄</span><span class="sxs-lookup"><span data-stu-id="5cfa7-142">Data Connector Discovery Logs</span></span>

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

### <span data-ttu-id="5cfa7-143">-Exchange</span><span class="sxs-lookup"><span data-stu-id="5cfa7-143">-Exchange</span></span>
<span data-ttu-id="5cfa7-144">資料連線器 Exchange</span><span class="sxs-lookup"><span data-stu-id="5cfa7-144">Data Connector Exchange</span></span>

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

### <span data-ttu-id="5cfa7-145">-標記</span><span class="sxs-lookup"><span data-stu-id="5cfa7-145">-Indicators</span></span>
<span data-ttu-id="5cfa7-146">資料連線器指示器</span><span class="sxs-lookup"><span data-stu-id="5cfa7-146">Data Connector Indicators</span></span>

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

### <span data-ttu-id="5cfa7-147">-記錄</span><span class="sxs-lookup"><span data-stu-id="5cfa7-147">-Logs</span></span>
<span data-ttu-id="5cfa7-148">資料連線器記錄</span><span class="sxs-lookup"><span data-stu-id="5cfa7-148">Data Connector Logs</span></span>

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

### <span data-ttu-id="5cfa7-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="5cfa7-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="5cfa7-150">Data Connector Microsoft Cloud App 安全性</span><span class="sxs-lookup"><span data-stu-id="5cfa7-150">Data Connector Microsoft Cloud App Security</span></span>

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

### <span data-ttu-id="5cfa7-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="5cfa7-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="5cfa7-152">Data Connector Microsoft Defender 進位威脅防護</span><span class="sxs-lookup"><span data-stu-id="5cfa7-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

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

### <span data-ttu-id="5cfa7-153">-Office365</span><span class="sxs-lookup"><span data-stu-id="5cfa7-153">-Office365</span></span>
<span data-ttu-id="5cfa7-154">資料連線器 Office 365</span><span class="sxs-lookup"><span data-stu-id="5cfa7-154">Data Connector Office 365</span></span>

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

### <span data-ttu-id="5cfa7-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cfa7-155">-ResourceGroupName</span></span>
<span data-ttu-id="5cfa7-156">資料連線器 Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5cfa7-156">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="5cfa7-157">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="5cfa7-157">-SharePoint</span></span>
<span data-ttu-id="5cfa7-158">資料連線器 SharePoint</span><span class="sxs-lookup"><span data-stu-id="5cfa7-158">Data Connector SharePoint</span></span>

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

### <span data-ttu-id="5cfa7-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5cfa7-159">-SubscriptionId</span></span>
<span data-ttu-id="5cfa7-160">資料連線器訂閱識別碼</span><span class="sxs-lookup"><span data-stu-id="5cfa7-160">Data connector Subscription Id</span></span>

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

### <span data-ttu-id="5cfa7-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="5cfa7-161">-ThreatIntelligence</span></span>
<span data-ttu-id="5cfa7-162">資料連線器威脅情報</span><span class="sxs-lookup"><span data-stu-id="5cfa7-162">Data Connector Threat Intelligence</span></span>

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

### <span data-ttu-id="5cfa7-163">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5cfa7-163">-WorkspaceName</span></span>
<span data-ttu-id="5cfa7-164">資料連線器 Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="5cfa7-164">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="5cfa7-165">-確認</span><span class="sxs-lookup"><span data-stu-id="5cfa7-165">-Confirm</span></span>
<span data-ttu-id="5cfa7-166">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5cfa7-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cfa7-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cfa7-167">-WhatIf</span></span>
<span data-ttu-id="5cfa7-168">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5cfa7-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5cfa7-169">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5cfa7-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5cfa7-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cfa7-170">CommonParameters</span></span>
<span data-ttu-id="5cfa7-171">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5cfa7-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cfa7-172">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cfa7-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cfa7-173">輸入</span><span class="sxs-lookup"><span data-stu-id="5cfa7-173">INPUTS</span></span>

### <span data-ttu-id="5cfa7-174">沒有</span><span class="sxs-lookup"><span data-stu-id="5cfa7-174">None</span></span>
## <span data-ttu-id="5cfa7-175">輸出</span><span class="sxs-lookup"><span data-stu-id="5cfa7-175">OUTPUTS</span></span>

### <span data-ttu-id="5cfa7-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="5cfa7-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="5cfa7-177">筆記</span><span class="sxs-lookup"><span data-stu-id="5cfa7-177">NOTES</span></span>

## <span data-ttu-id="5cfa7-178">相關連結</span><span class="sxs-lookup"><span data-stu-id="5cfa7-178">RELATED LINKS</span></span>
