---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActionGroupReceiver.md
ms.openlocfilehash: 35f540d26464b7cdc4b08916f1397b71ee7cca18
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93786717"
---
# <span data-ttu-id="5bd3b-101">New-AzActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="5bd3b-101">New-AzActionGroupReceiver</span></span>

## <span data-ttu-id="5bd3b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5bd3b-102">SYNOPSIS</span></span>
<span data-ttu-id="5bd3b-103">建立新的 [動作群組收件者]。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-103">Creates an new action group receiver.</span></span>

## <span data-ttu-id="5bd3b-104">句法</span><span class="sxs-lookup"><span data-stu-id="5bd3b-104">SYNTAX</span></span>

### <span data-ttu-id="5bd3b-105">NewEmailReceiver (預設) </span><span class="sxs-lookup"><span data-stu-id="5bd3b-105">NewEmailReceiver (Default)</span></span>
```
New-AzActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bd3b-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="5bd3b-106">NewSmsReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5bd3b-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="5bd3b-107">NewWebhookReceiver</span></span>
```
New-AzActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5bd3b-108">說明</span><span class="sxs-lookup"><span data-stu-id="5bd3b-108">DESCRIPTION</span></span>
<span data-ttu-id="5bd3b-109">**新的-AzActionGroupReceiver** Cmdlet 會在記憶體中建立新的動作群組接收器。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-109">The **New-AzActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="5bd3b-110">示例</span><span class="sxs-lookup"><span data-stu-id="5bd3b-110">EXAMPLES</span></span>

### <span data-ttu-id="5bd3b-111">範例1：在記憶體中建立新的電子郵件收件者。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="5bd3b-112">這個命令會在記憶體中建立新的電子郵件收件者。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="5bd3b-113">範例2：在記憶體中建立新的 SMS 接收器。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="5bd3b-114">這個命令會在記憶體中建立新的 SMS 接收器。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="5bd3b-115">範例3：在記憶體中建立新的 webhook 接收器。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzActionGroupReceiver -Name 'webhookReceiver1' -WebhookReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="5bd3b-116">這個命令會在記憶體中建立新的 webhook 接收器。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="5bd3b-117">參數</span><span class="sxs-lookup"><span data-stu-id="5bd3b-117">PARAMETERS</span></span>

### <span data-ttu-id="5bd3b-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="5bd3b-118">-CountryCode</span></span>
<span data-ttu-id="5bd3b-119">指定 SMS 接收器的國家/地區碼。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-119">Specifies the country code for the SMS receiver.</span></span>

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

### <span data-ttu-id="5bd3b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bd3b-120">-DefaultProfile</span></span>
<span data-ttu-id="5bd3b-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="5bd3b-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5bd3b-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="5bd3b-122">-EmailAddress</span></span>
<span data-ttu-id="5bd3b-123">指定電子郵件收件者的位址。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-123">Specifies the address for the Email receiver.</span></span>

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

### <span data-ttu-id="5bd3b-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="5bd3b-124">-EmailReceiver</span></span>
<span data-ttu-id="5bd3b-125">指定建立電子郵件收件者</span><span class="sxs-lookup"><span data-stu-id="5bd3b-125">Specifies to create an Email receiver</span></span>

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

### <span data-ttu-id="5bd3b-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="5bd3b-126">-Name</span></span>
<span data-ttu-id="5bd3b-127">指定收件者的名稱。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-127">Specifies the name for the receiver.</span></span>

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

### <span data-ttu-id="5bd3b-128">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="5bd3b-128">-PhoneNumber</span></span>
<span data-ttu-id="5bd3b-129">指定 SMS 接收器的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-129">Specifies the phone number for the SMS receiver.</span></span>

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

### <span data-ttu-id="5bd3b-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="5bd3b-130">-ServiceUri</span></span>
<span data-ttu-id="5bd3b-131">指定 webhook 接收器的 URI。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-131">Specifies the URI for the webhook receiver.</span></span>

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

### <span data-ttu-id="5bd3b-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="5bd3b-132">-SmsReceiver</span></span>
<span data-ttu-id="5bd3b-133">指定建立 SMS 接收器</span><span class="sxs-lookup"><span data-stu-id="5bd3b-133">Specifies to create a SMS receiver</span></span>

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

### <span data-ttu-id="5bd3b-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="5bd3b-134">-WebhookReceiver</span></span>
<span data-ttu-id="5bd3b-135">指定建立 webhook 接收器</span><span class="sxs-lookup"><span data-stu-id="5bd3b-135">Specifies to create a webhook receiver</span></span>

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

### <span data-ttu-id="5bd3b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bd3b-136">CommonParameters</span></span>
<span data-ttu-id="5bd3b-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bd3b-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bd3b-139">輸入</span><span class="sxs-lookup"><span data-stu-id="5bd3b-139">INPUTS</span></span>

### <span data-ttu-id="5bd3b-140">System.object</span><span class="sxs-lookup"><span data-stu-id="5bd3b-140">System.String</span></span>

### <span data-ttu-id="5bd3b-141">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="5bd3b-141">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5bd3b-142">輸出</span><span class="sxs-lookup"><span data-stu-id="5bd3b-142">OUTPUTS</span></span>

### <span data-ttu-id="5bd3b-143">PSActionGroupReceiverBase 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="5bd3b-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="5bd3b-144">筆記</span><span class="sxs-lookup"><span data-stu-id="5bd3b-144">NOTES</span></span>

## <span data-ttu-id="5bd3b-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="5bd3b-145">RELATED LINKS</span></span>

<span data-ttu-id="5bd3b-146">[Set-AzActionGroup](./Set-AzActionGroup.md) 
[AzActionGroup](./Get-AzActionGroup.md) 
[移除-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="5bd3b-146">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>
