---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 917f6287c40d4c26123217cccbf1dfc11866a488
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908898"
---
# <span data-ttu-id="66c06-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="66c06-102">簡介</span><span class="sxs-lookup"><span data-stu-id="66c06-102">SYNOPSIS</span></span>
<span data-ttu-id="66c06-103">建立新動作群組接收者。</span><span class="sxs-lookup"><span data-stu-id="66c06-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="66c06-104">語法</span><span class="sxs-lookup"><span data-stu-id="66c06-104">SYNTAX</span></span>

### <span data-ttu-id="66c06-105">NewEmailReceiver (預設) </span><span class="sxs-lookup"><span data-stu-id="66c06-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c06-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-SmsReceiver] [-CountryCode <String>]
 -PhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c06-107">NewWeb有Receiver</span><span class="sxs-lookup"><span data-stu-id="66c06-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-WebhookReceiver] -ServiceUri <String>
 [-UseAadAuth] [-ObjectId <String>] [-IdentifierUri <String>] [-TenantId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c06-108">NewItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-108">NewItsmReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ItsmReceiver] -WorkspaceId <String>
 -ConnectionId <String> -TicketConfiguration <String> -Region <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c06-109">NewVoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-109">NewVoiceReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-VoiceReceiver] [-VoiceCountryCode <String>]
 -VoicePhoneNumber <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c06-110">NewArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-110">NewArmRoleReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-ArmRoleReceiver] -RoleId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c06-111">NewAzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-111">NewAzureFunctionReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureFunctionReceiver]
 -FunctionAppResourceId <String> -HttpTriggerUrl <String> -FunctionName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c06-112">NewLogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-112">NewLogicAppReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-LogicAppReceiver] -ResourceId <String>
 -CallbackUrl <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c06-113">NewAutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-113">NewAutomationRunbookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AutomationRunbookReceiver]
 -AutomationAccountId <String> -RunbookName <String> [-IsGlobalRunbook] -AutomationRunbookServiceUri <String>
 -WebhookResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="66c06-114">NewAzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-114">NewAzureAppPushReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-UseCommonAlertSchema] [-AzureAppPushReceiver]
 -AzureAppPushEmailAddress <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66c06-115">描述</span><span class="sxs-lookup"><span data-stu-id="66c06-115">DESCRIPTION</span></span>
<span data-ttu-id="66c06-116">**New-AzActionGroupReceiver** Cmdlet 在記憶體中建立新的動作群組聽筒。</span><span class="sxs-lookup"><span data-stu-id="66c06-116">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="66c06-117">例子</span><span class="sxs-lookup"><span data-stu-id="66c06-117">EXAMPLES</span></span>

### <span data-ttu-id="66c06-118">範例 1：在記憶體中建立一個新的電子郵件接收者。</span><span class="sxs-lookup"><span data-stu-id="66c06-118">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="66c06-119">此命令在記憶體中建立一個新的電子郵件接收者。</span><span class="sxs-lookup"><span data-stu-id="66c06-119">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="66c06-120">範例 2：在記憶體中建立新的 SMS 聽筒。</span><span class="sxs-lookup"><span data-stu-id="66c06-120">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="66c06-121">此命令在記憶體中建立一個新的 SMS 聽筒。</span><span class="sxs-lookup"><span data-stu-id="66c06-121">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="66c06-122">範例 3：在記憶體中建立一個新的 web一體聽筒。</span><span class="sxs-lookup"><span data-stu-id="66c06-122">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="66c06-123">此命令在記憶體中建立一個新的 web一體聽筒。</span><span class="sxs-lookup"><span data-stu-id="66c06-123">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="66c06-124">參數</span><span class="sxs-lookup"><span data-stu-id="66c06-124">PARAMETERS</span></span>

### <span data-ttu-id="66c06-125">-ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-125">-ArmRoleReceiver</span></span>
<span data-ttu-id="66c06-126">建立 ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-126">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="66c06-127">-AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="66c06-127">-AutomationAccountId</span></span>
<span data-ttu-id="66c06-128">AutomationAccountId</span><span class="sxs-lookup"><span data-stu-id="66c06-128">the AutomationAccountId</span></span>

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

### <span data-ttu-id="66c06-129">-AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-129">-AutomationRunbookReceiver</span></span>
<span data-ttu-id="66c06-130">建立 AutomationRunbookReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-130">Create a AutomationRunbookReceiver</span></span>

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

### <span data-ttu-id="66c06-131">-AutomationRunbookServiceUri</span><span class="sxs-lookup"><span data-stu-id="66c06-131">-AutomationRunbookServiceUri</span></span>
<span data-ttu-id="66c06-132">應該要送出 Web下拉子的 URI</span><span class="sxs-lookup"><span data-stu-id="66c06-132">the URI where webhooks should be sent</span></span>

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

### <span data-ttu-id="66c06-133">-AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="66c06-133">-AzureAppPushEmailAddress</span></span>
<span data-ttu-id="66c06-134">AzureAppPushEmailAddress</span><span class="sxs-lookup"><span data-stu-id="66c06-134">the AzureAppPushEmailAddress</span></span>

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

### <span data-ttu-id="66c06-135">-AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-135">-AzureAppPushReceiver</span></span>
<span data-ttu-id="66c06-136">建立 AzureAppPushReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-136">Create a AzureAppPushReceiver</span></span>

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

### <span data-ttu-id="66c06-137">-AzureFunctionReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-137">-AzureFunctionReceiver</span></span>
<span data-ttu-id="66c06-138">建立 ArmRoleReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-138">Create a ArmRoleReceiver</span></span>

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

### <span data-ttu-id="66c06-139">-Url</span><span class="sxs-lookup"><span data-stu-id="66c06-139">-CallbackUrl</span></span>
<span data-ttu-id="66c06-140">的Url</span><span class="sxs-lookup"><span data-stu-id="66c06-140">the CallbackUrl</span></span>

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

### <span data-ttu-id="66c06-141">-ConnectionId</span><span class="sxs-lookup"><span data-stu-id="66c06-141">-ConnectionId</span></span>
<span data-ttu-id="66c06-142">此聽筒的M 連接識別碼</span><span class="sxs-lookup"><span data-stu-id="66c06-142">the itsm connection id of this receiver</span></span>

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

### <span data-ttu-id="66c06-143">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="66c06-143">-CountryCode</span></span>
<span data-ttu-id="66c06-144">指定簡訊接收者的國家/地區代碼。</span><span class="sxs-lookup"><span data-stu-id="66c06-144">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="66c06-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66c06-145">-DefaultProfile</span></span>
<span data-ttu-id="66c06-146">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="66c06-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="66c06-147">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="66c06-147">-EmailAddress</span></span>
<span data-ttu-id="66c06-148">指定電子郵件接收者的位址。</span><span class="sxs-lookup"><span data-stu-id="66c06-148">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="66c06-149">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-149">-EmailReceiver</span></span>
<span data-ttu-id="66c06-150">指定建立電子郵件接收者</span><span class="sxs-lookup"><span data-stu-id="66c06-150">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="66c06-151">-FunctionAppResourceId</span><span class="sxs-lookup"><span data-stu-id="66c06-151">-FunctionAppResourceId</span></span>
<span data-ttu-id="66c06-152">函數應用程式 resourceId</span><span class="sxs-lookup"><span data-stu-id="66c06-152">the function app resourceId</span></span>

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

### <span data-ttu-id="66c06-153">-FunctionName</span><span class="sxs-lookup"><span data-stu-id="66c06-153">-FunctionName</span></span>
<span data-ttu-id="66c06-154">functionName</span><span class="sxs-lookup"><span data-stu-id="66c06-154">the functionName</span></span>

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

### <span data-ttu-id="66c06-155">-HTTPTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="66c06-155">-HttpTriggerUrl</span></span>
<span data-ttu-id="66c06-156">HTTPTriggerUrl</span><span class="sxs-lookup"><span data-stu-id="66c06-156">the httpTriggerUrl</span></span>

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

### <span data-ttu-id="66c06-157">-IdentifierUri</span><span class="sxs-lookup"><span data-stu-id="66c06-157">-IdentifierUri</span></span>
<span data-ttu-id="66c06-158">aad 驗證的識別碼 uri</span><span class="sxs-lookup"><span data-stu-id="66c06-158">the Identifier uri for aad auth</span></span>

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

### <span data-ttu-id="66c06-159">-IsGlobalRunbook</span><span class="sxs-lookup"><span data-stu-id="66c06-159">-IsGlobalRunbook</span></span>
<span data-ttu-id="66c06-160">指出此實例是否為全域 runbook</span><span class="sxs-lookup"><span data-stu-id="66c06-160">indicating whether this instance is global runbook</span></span>

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

### <span data-ttu-id="66c06-161">-ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-161">-ItsmReceiver</span></span>
<span data-ttu-id="66c06-162">建立 ItsmReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-162">Create a ItsmReceiver</span></span>

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

### <span data-ttu-id="66c06-163">-LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-163">-LogicAppReceiver</span></span>
<span data-ttu-id="66c06-164">建立 LogicAppReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-164">Create a LogicAppReceiver</span></span>

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

### <span data-ttu-id="66c06-165">-名稱</span><span class="sxs-lookup"><span data-stu-id="66c06-165">-Name</span></span>
<span data-ttu-id="66c06-166">指定收受者的名稱。</span><span class="sxs-lookup"><span data-stu-id="66c06-166">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="66c06-167">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="66c06-167">-ObjectId</span></span>
<span data-ttu-id="66c06-168">適用于 aad 驗證的 web上 App 物件識別碼</span><span class="sxs-lookup"><span data-stu-id="66c06-168">the webhook app object Id for aad auth</span></span>

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

### <span data-ttu-id="66c06-169">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="66c06-169">-PhoneNumber</span></span>
<span data-ttu-id="66c06-170">指定簡訊接收者的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="66c06-170">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="66c06-171">-區域</span><span class="sxs-lookup"><span data-stu-id="66c06-171">-Region</span></span>
<span data-ttu-id="66c06-172">此聽筒的其 m 區域</span><span class="sxs-lookup"><span data-stu-id="66c06-172">the itsm Region of this receiver</span></span>

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

### <span data-ttu-id="66c06-173">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="66c06-173">-ResourceId</span></span>
<span data-ttu-id="66c06-174">ResourceId</span><span class="sxs-lookup"><span data-stu-id="66c06-174">the ResourceId</span></span>

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

### <span data-ttu-id="66c06-175">-RoleId</span><span class="sxs-lookup"><span data-stu-id="66c06-175">-RoleId</span></span>
<span data-ttu-id="66c06-176">收受者之 arm 角色識別碼</span><span class="sxs-lookup"><span data-stu-id="66c06-176">The arm role id of the receiver</span></span>

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

### <span data-ttu-id="66c06-177">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="66c06-177">-RunbookName</span></span>
<span data-ttu-id="66c06-178">RunbookName</span><span class="sxs-lookup"><span data-stu-id="66c06-178">the RunbookName</span></span>

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

### <span data-ttu-id="66c06-179">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="66c06-179">-ServiceUri</span></span>
<span data-ttu-id="66c06-180">指定 web一聽筒的 URI。</span><span class="sxs-lookup"><span data-stu-id="66c06-180">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="66c06-181">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-181">-SmsReceiver</span></span>
<span data-ttu-id="66c06-182">指定建立簡訊接收者</span><span class="sxs-lookup"><span data-stu-id="66c06-182">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="66c06-183">-TenantId</span><span class="sxs-lookup"><span data-stu-id="66c06-183">-TenantId</span></span>
<span data-ttu-id="66c06-184">aad 驗證的租使用者識別碼</span><span class="sxs-lookup"><span data-stu-id="66c06-184">the tenant id for aad auth</span></span>

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

### <span data-ttu-id="66c06-185">-TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="66c06-185">-TicketConfiguration</span></span>
<span data-ttu-id="66c06-186">此聽筒的其m TicketConfiguration</span><span class="sxs-lookup"><span data-stu-id="66c06-186">the itsm TicketConfiguration of this receiver</span></span>

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

### <span data-ttu-id="66c06-187">-UseAadAuth</span><span class="sxs-lookup"><span data-stu-id="66c06-187">-UseAadAuth</span></span>
<span data-ttu-id="66c06-188">使用 Add auth 的標號</span><span class="sxs-lookup"><span data-stu-id="66c06-188">the flag to use add auth</span></span>

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

### <span data-ttu-id="66c06-189">-UseCommonAlertSchema</span><span class="sxs-lookup"><span data-stu-id="66c06-189">-UseCommonAlertSchema</span></span>
<span data-ttu-id="66c06-190">是否要使用一般警示架構的標標。</span><span class="sxs-lookup"><span data-stu-id="66c06-190">The flag whether to use common alert schema .</span></span> <span data-ttu-id="66c06-191">此值會用於簡訊、Azure App 推入、ITSM 和 Voice 訂閱。</span><span class="sxs-lookup"><span data-stu-id="66c06-191">This value will be neglectedfor SMS, Azure App push , ITSM and Voice recievers.</span></span>

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

### <span data-ttu-id="66c06-192">-VoiceCountryCode</span><span class="sxs-lookup"><span data-stu-id="66c06-192">-VoiceCountryCode</span></span>
<span data-ttu-id="66c06-193">語音聽筒的國家/地區代碼</span><span class="sxs-lookup"><span data-stu-id="66c06-193">The country code of the voice receiver</span></span>

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

### <span data-ttu-id="66c06-194">-VoicePhoneNumber</span><span class="sxs-lookup"><span data-stu-id="66c06-194">-VoicePhoneNumber</span></span>
<span data-ttu-id="66c06-195">語音聽筒的電話號碼</span><span class="sxs-lookup"><span data-stu-id="66c06-195">The phone number of the voice receiver</span></span>

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

### <span data-ttu-id="66c06-196">-VoiceReceiver</span><span class="sxs-lookup"><span data-stu-id="66c06-196">-VoiceReceiver</span></span>
<span data-ttu-id="66c06-197">建立語音聽筒</span><span class="sxs-lookup"><span data-stu-id="66c06-197">Create a voice receiver</span></span>

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

### <span data-ttu-id="66c06-198">-Web上Receiver</span><span class="sxs-lookup"><span data-stu-id="66c06-198">-WebhookReceiver</span></span>
<span data-ttu-id="66c06-199">指定建立 web一台接收器</span><span class="sxs-lookup"><span data-stu-id="66c06-199">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="66c06-200">-WebsourceResourceId</span><span class="sxs-lookup"><span data-stu-id="66c06-200">-WebhookResourceId</span></span>
<span data-ttu-id="66c06-201">WebsourceResourceId</span><span class="sxs-lookup"><span data-stu-id="66c06-201">the WebhookResourceId</span></span>

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

### <span data-ttu-id="66c06-202">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="66c06-202">-WorkspaceId</span></span>
<span data-ttu-id="66c06-203">此收受者其 m 工作區識別碼</span><span class="sxs-lookup"><span data-stu-id="66c06-203">the itsm workspace id of this receiver</span></span>

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

### <span data-ttu-id="66c06-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66c06-204">CommonParameters</span></span>
<span data-ttu-id="66c06-205">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="66c06-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66c06-206">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66c06-206">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66c06-207">輸入</span><span class="sxs-lookup"><span data-stu-id="66c06-207">INPUTS</span></span>

### <span data-ttu-id="66c06-208">System.String</span><span class="sxs-lookup"><span data-stu-id="66c06-208">System.String</span></span>

### <span data-ttu-id="66c06-209">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="66c06-209">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="66c06-210">輸出</span><span class="sxs-lookup"><span data-stu-id="66c06-210">OUTPUTS</span></span>

### <span data-ttu-id="66c06-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span><span class="sxs-lookup"><span data-stu-id="66c06-211">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="66c06-212">筆記</span><span class="sxs-lookup"><span data-stu-id="66c06-212">NOTES</span></span>

## <span data-ttu-id="66c06-213">相關連結</span><span class="sxs-lookup"><span data-stu-id="66c06-213">RELATED LINKS</span></span>

<span data-ttu-id="66c06-214">[Set-AzActionGroup](./Set-AzActionGroup.md) 
[Get-AzActionGroup](./Get-AzActionGroup.md) 
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="66c06-214">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
