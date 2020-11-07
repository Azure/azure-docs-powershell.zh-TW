---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 43eda2eb27003a079dae0442d7ab8e9f636cbef4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93789846"
---
# <span data-ttu-id="5a086-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="5a086-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5a086-102">SYNOPSIS</span></span>
<span data-ttu-id="5a086-103">建立新的 [動作群組收件者]。</span><span class="sxs-lookup"><span data-stu-id="5a086-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="5a086-104">句法</span><span class="sxs-lookup"><span data-stu-id="5a086-104">SYNTAX</span></span>

### <span data-ttu-id="5a086-105">NewEmailReceiver (預設) </span><span class="sxs-lookup"><span data-stu-id="5a086-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a086-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a086-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a086-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a086-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a086-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a086-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a086-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a086-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a086-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a086-115">說明</span><span class="sxs-lookup"><span data-stu-id="5a086-115">DESCRIPTION</span></span>
<span data-ttu-id="5a086-116">**新的-AzActionGroupReceiver** Cmdlet 會在記憶體中建立新的動作群組接收器。</span><span class="sxs-lookup"><span data-stu-id="5a086-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="5a086-117">示例</span><span class="sxs-lookup"><span data-stu-id="5a086-117">EXAMPLES</span></span>

### <span data-ttu-id="5a086-118">範例1：在記憶體中建立新的電子郵件收件者。</span><span class="sxs-lookup"><span data-stu-id="5a086-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="5a086-119">這個命令會在記憶體中建立新的電子郵件收件者。</span><span class="sxs-lookup"><span data-stu-id="5a086-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="5a086-120">範例2：在記憶體中建立新的 SMS 接收器。</span><span class="sxs-lookup"><span data-stu-id="5a086-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="5a086-121">這個命令會在記憶體中建立新的 SMS 接收器。</span><span class="sxs-lookup"><span data-stu-id="5a086-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="5a086-122">範例3：在記憶體中建立新的 webhook 接收器。</span><span class="sxs-lookup"><span data-stu-id="5a086-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="5a086-123">這個命令會在記憶體中建立新的 webhook 接收器。</span><span class="sxs-lookup"><span data-stu-id="5a086-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="5a086-124">參數</span><span class="sxs-lookup"><span data-stu-id="5a086-124">PARAMETERS</span></span>

### <span data-ttu-id="5a086-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="5a086-126">建立 ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-126">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="5a086-127">-AutomationAccountId</span></span>
<span data-ttu-id="5a086-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="5a086-128">the AutomationAccountId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="5a086-130">建立 AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-130">Create a AutomationRunbookReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="5a086-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="5a086-132">應傳送 webhooks 的 URI</span><span class="sxs-lookup"><span data-stu-id="5a086-132">the URI where webhooks should be sent</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="5a086-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="5a086-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="5a086-134">the AzureAppPushEmailAddress</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="5a086-136">建立 AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-136">Create a AzureAppPushReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureAppPushReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="5a086-138">建立 ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-138">Create a ArmRoleReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-139">-CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="5a086-139">-CallbackUrl</span></span>
<span data-ttu-id="5a086-140">CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="5a086-140">the CallbackUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="5a086-141">-ConnectionId</span></span>
<span data-ttu-id="5a086-142">此接收器的 itsm 連線 id</span><span class="sxs-lookup"><span data-stu-id="5a086-142">the itsm connection id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="5a086-143">-CountryCode</span></span>
<span data-ttu-id="5a086-144">指定 SMS 接收器的國家/地區碼。</span><span class="sxs-lookup"><span data-stu-id="5a086-144">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a086-145">-DefaultProfile</span></span>
<span data-ttu-id="5a086-146">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5a086-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a086-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="5a086-147">-EmailAddress</span></span>
<span data-ttu-id="5a086-148">指定電子郵件收件者的位址。</span><span class="sxs-lookup"><span data-stu-id="5a086-148">Specifies the address for the Email receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewEmailReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-149">-EmailReceiver</span></span>
<span data-ttu-id="5a086-150">指定建立電子郵件收件者</span><span class="sxs-lookup"><span data-stu-id="5a086-150">Specifies to create an Email receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="5a086-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="5a086-152">函數 app resourceId</span><span class="sxs-lookup"><span data-stu-id="5a086-152">the function app resourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="5a086-153">-FunctionName</span></span>
<span data-ttu-id="5a086-154">functionName</span><span class="sxs-lookup"><span data-stu-id="5a086-154">the functionName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-155">-HttpTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="5a086-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="5a086-156">HTTPTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="5a086-156">the httpTriggerUrl</span></span>

```yaml
Type: System.String
Parameter Sets: NewAzureFunctionReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="5a086-157">-IdentifierUri</span></span>
<span data-ttu-id="5a086-158">aad 驗證的識別碼 uri</span><span class="sxs-lookup"><span data-stu-id="5a086-158">the Identifier uri for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="5a086-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="5a086-160">指出此實例是否為全域 runbook</span><span class="sxs-lookup"><span data-stu-id="5a086-160">indicating whether this instance is global runbook</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-161">-ItsmReceiver</span></span>
<span data-ttu-id="5a086-162">建立 ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-162">Create a ItsmReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewItsmReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-163">-LogicAppReceiver</span></span>
<span data-ttu-id="5a086-164">建立 LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-164">Create a LogicAppReceiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-165">-名稱</span><span class="sxs-lookup"><span data-stu-id="5a086-165">-Name</span></span>
<span data-ttu-id="5a086-166">指定收件者的名稱。</span><span class="sxs-lookup"><span data-stu-id="5a086-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="5a086-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5a086-167">-ObjectId</span></span>
<span data-ttu-id="5a086-168">aad 驗證的 webhook app 物件識別碼</span><span class="sxs-lookup"><span data-stu-id="5a086-168">the webhook app object Id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="5a086-169">-PhoneNumber</span></span>
<span data-ttu-id="5a086-170">指定 SMS 接收器的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="5a086-170">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewSmsReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-171">-Region</span><span class="sxs-lookup"><span data-stu-id="5a086-171">-Region</span></span>
<span data-ttu-id="5a086-172">此接收器的 itsm 區域</span><span class="sxs-lookup"><span data-stu-id="5a086-172">the itsm Region of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a086-173">-ResourceId</span></span>
<span data-ttu-id="5a086-174">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a086-174">the ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewLogicAppReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="5a086-175">-RoleId</span></span>
<span data-ttu-id="5a086-176">接收器的 arm 角色識別碼</span><span class="sxs-lookup"><span data-stu-id="5a086-176">The arm role id of the receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewArmRoleReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="5a086-177">-RunbookName</span></span>
<span data-ttu-id="5a086-178">RunbookName</span><span class="sxs-lookup"><span data-stu-id="5a086-178">the RunbookName</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="5a086-179">-ServiceUri</span></span>
<span data-ttu-id="5a086-180">指定 webhook 接收器的 URI。</span><span class="sxs-lookup"><span data-stu-id="5a086-180">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-181">-SmsReceiver</span></span>
<span data-ttu-id="5a086-182">指定建立 SMS 接收器</span><span class="sxs-lookup"><span data-stu-id="5a086-182">Specifies to create a SMS receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="5a086-183">-TenantId</span></span>
<span data-ttu-id="5a086-184">aad 驗證的租使用者識別碼</span><span class="sxs-lookup"><span data-stu-id="5a086-184">the tenant id for aad auth</span></span>

```yaml
Type: System.String
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a086-185">-TicketConfiguration</span></span>
<span data-ttu-id="5a086-186">此接收器的 itsm TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="5a086-186">the itsm TicketConfiguration of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="5a086-187">-UseAadAuth</span></span>
<span data-ttu-id="5a086-188">使用 [新增驗證] 的標誌</span><span class="sxs-lookup"><span data-stu-id="5a086-188">the flag to use add auth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="5a086-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="5a086-190">標誌是否要使用常見的通知架構。</span><span class="sxs-lookup"><span data-stu-id="5a086-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="5a086-191">此值將會 neglectedfor SMS、Azure App push、ITSM 和語音 recievers。</span><span class="sxs-lookup"><span data-stu-id="5a086-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="5a086-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="5a086-192">-VoiceCountryCode</span></span>
<span data-ttu-id="5a086-193">語音收件者的國家/地區代碼</span><span class="sxs-lookup"><span data-stu-id="5a086-193">The country code of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="5a086-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="5a086-195">語音接收器的電話號碼</span><span class="sxs-lookup"><span data-stu-id="5a086-195">The phone number of the voice receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewVoiceReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-196">-VoiceReceiver</span></span>
<span data-ttu-id="5a086-197">建立語音接收器</span><span class="sxs-lookup"><span data-stu-id="5a086-197">Create a voice receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewVoiceReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-198">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="5a086-198">-WebhookReceiver</span></span>
<span data-ttu-id="5a086-199">指定建立 webhook 接收器</span><span class="sxs-lookup"><span data-stu-id="5a086-199">Specifies to create a webhook receiver</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-200">-WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="5a086-200">-WebhookResourceId</span></span>
<span data-ttu-id="5a086-201">WebhookResourceId</span><span class="sxs-lookup"><span data-stu-id="5a086-201">the WebhookResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: NewAutomationRunbookReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="5a086-202">-WorkspaceId</span></span>
<span data-ttu-id="5a086-203">此接收器的 itsm 工作區識別碼</span><span class="sxs-lookup"><span data-stu-id="5a086-203">the itsm workspace id of this receiver</span></span>

```yaml
Type: System.String
Parameter Sets: NewItsmReceiver
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a086-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a086-204">CommonParameters</span></span>
<span data-ttu-id="5a086-205">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5a086-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a086-206">如需詳細資訊，請參閱 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="5a086-206">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a086-207">輸入</span><span class="sxs-lookup"><span data-stu-id="5a086-207">INPUTS</span></span>

### <span data-ttu-id="5a086-208">System.object</span><span class="sxs-lookup"><span data-stu-id="5a086-208">System.String</span></span>

### <span data-ttu-id="5a086-209">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="5a086-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5a086-210">輸出</span><span class="sxs-lookup"><span data-stu-id="5a086-210">OUTPUTS</span></span>

### <span data-ttu-id="5a086-211">PSActionGroupReceiverBase 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="5a086-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="5a086-212">筆記</span><span class="sxs-lookup"><span data-stu-id="5a086-212">NOTES</span></span>

## <span data-ttu-id="5a086-213">相關連結</span><span class="sxs-lookup"><span data-stu-id="5a086-213">RELATED LINKS</span></span>

<span data-ttu-id="5a086-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
[AzActionGroup](./Get-AzActionGroup.md) 
[移除-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="5a086-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
