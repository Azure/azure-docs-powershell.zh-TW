---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 9830CD16-D797-47EB-BEF5-6CFE3454BCAA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroupreceiver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroupReceiver.md
ms.openlocfilehash: 1c35572191ccf66bd7fd4e88e0996a8efdd1b82b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449360"
---
# <span data-ttu-id="e4328-101">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="e4328-101">New-AzureRmActionGroupReceiver</span></span>

## <span data-ttu-id="e4328-102">摘要</span><span class="sxs-lookup"><span data-stu-id="e4328-102">SYNOPSIS</span></span>
<span data-ttu-id="e4328-103">建立新的 [動作群組收件者]。</span><span class="sxs-lookup"><span data-stu-id="e4328-103">Creates an new action group receiver.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e4328-104">句法</span><span class="sxs-lookup"><span data-stu-id="e4328-104">SYNTAX</span></span>

### <span data-ttu-id="e4328-105">NewEmailReceiver (預設) </span><span class="sxs-lookup"><span data-stu-id="e4328-105">NewEmailReceiver (Default)</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-EmailReceiver] -EmailAddress <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4328-106">NewSmsReceiver</span><span class="sxs-lookup"><span data-stu-id="e4328-106">NewSmsReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-SmsReceiver] [-CountryCode <String>] -PhoneNumber <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4328-107">NewWebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="e4328-107">NewWebhookReceiver</span></span>
```
New-AzureRmActionGroupReceiver -Name <String> [-WebhookReceiver] -ServiceUri <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4328-108">說明</span><span class="sxs-lookup"><span data-stu-id="e4328-108">DESCRIPTION</span></span>
<span data-ttu-id="e4328-109">**新的-AzureRmActionGroupReceiver** Cmdlet 會在記憶體中建立新的動作群組接收器。</span><span class="sxs-lookup"><span data-stu-id="e4328-109">The **New-AzureRmActionGroupReceiver** cmdlet creates new action group receiver in memory.</span></span>

## <span data-ttu-id="e4328-110">示例</span><span class="sxs-lookup"><span data-stu-id="e4328-110">EXAMPLES</span></span>

### <span data-ttu-id="e4328-111">範例1：在記憶體中建立新的電子郵件收件者。</span><span class="sxs-lookup"><span data-stu-id="e4328-111">Example 1: Create a new Email receiver in memory.</span></span>
```
PS C:\>$emailReceiver = New-AzureRmActionGroupReceiver -Name 'emailReceiver1' -EmailReceiver -EmailAddress 'user1@example.com'
```

<span data-ttu-id="e4328-112">這個命令會在記憶體中建立新的電子郵件收件者。</span><span class="sxs-lookup"><span data-stu-id="e4328-112">This command creates a new Email receiver in memory.</span></span>

### <span data-ttu-id="e4328-113">範例2：在記憶體中建立新的 SMS 接收器。</span><span class="sxs-lookup"><span data-stu-id="e4328-113">Example 2: Create a new SMS receiver in memory.</span></span>
```
PS C:\>$smsReceiver = New-AzureRmActionGroupReceiver -Name 'smsReceiver1' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
```

<span data-ttu-id="e4328-114">這個命令會在記憶體中建立新的 SMS 接收器。</span><span class="sxs-lookup"><span data-stu-id="e4328-114">This command creates a new SMS receiver in memory.</span></span>

### <span data-ttu-id="e4328-115">範例3：在記憶體中建立新的 webhook 接收器。</span><span class="sxs-lookup"><span data-stu-id="e4328-115">Example 3: Create a new webhook receiver in memory.</span></span>
```
PS C:\>$webhookReceiver = New-AzureRmActionGroupReceiver -Name 'webhookReceiver1' -SMSReceiver -ServiceUri 'http://test.com'
```

<span data-ttu-id="e4328-116">這個命令會在記憶體中建立新的 webhook 接收器。</span><span class="sxs-lookup"><span data-stu-id="e4328-116">This command creates a new webhook receiver in memory.</span></span>

## <span data-ttu-id="e4328-117">參數</span><span class="sxs-lookup"><span data-stu-id="e4328-117">PARAMETERS</span></span>

### <span data-ttu-id="e4328-118">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="e4328-118">-CountryCode</span></span>
<span data-ttu-id="e4328-119">指定 SMS 接收器的國家/地區碼。</span><span class="sxs-lookup"><span data-stu-id="e4328-119">Specifies the country code for the SMS receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewSmsReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4328-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4328-120">-DefaultProfile</span></span>
<span data-ttu-id="e4328-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="e4328-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4328-122">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e4328-122">-EmailAddress</span></span>
<span data-ttu-id="e4328-123">指定電子郵件收件者的位址。</span><span class="sxs-lookup"><span data-stu-id="e4328-123">Specifies the address for the Email receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewEmailReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4328-124">-EmailReceiver</span><span class="sxs-lookup"><span data-stu-id="e4328-124">-EmailReceiver</span></span>
<span data-ttu-id="e4328-125">指定建立電子郵件收件者</span><span class="sxs-lookup"><span data-stu-id="e4328-125">Specifies to create an Email receiver</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NewEmailReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4328-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="e4328-126">-Name</span></span>
<span data-ttu-id="e4328-127">指定收件者的名稱。</span><span class="sxs-lookup"><span data-stu-id="e4328-127">Specifies the name for the receiver.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4328-128">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="e4328-128">-PhoneNumber</span></span>
<span data-ttu-id="e4328-129">指定 SMS 接收器的電話號碼。</span><span class="sxs-lookup"><span data-stu-id="e4328-129">Specifies the phone number for the SMS receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewSmsReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4328-130">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="e4328-130">-ServiceUri</span></span>
<span data-ttu-id="e4328-131">指定 webhook 接收器的 URI。</span><span class="sxs-lookup"><span data-stu-id="e4328-131">Specifies the URI for the webhook receiver.</span></span>

```yaml
Type: String
Parameter Sets: NewWebhookReceiver
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4328-132">-SmsReceiver</span><span class="sxs-lookup"><span data-stu-id="e4328-132">-SmsReceiver</span></span>
<span data-ttu-id="e4328-133">指定建立 SMS 接收器</span><span class="sxs-lookup"><span data-stu-id="e4328-133">Specifies to create a SMS receiver</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NewSmsReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4328-134">-WebhookReceiver</span><span class="sxs-lookup"><span data-stu-id="e4328-134">-WebhookReceiver</span></span>
<span data-ttu-id="e4328-135">指定建立 webhook 接收器</span><span class="sxs-lookup"><span data-stu-id="e4328-135">Specifies to create a webhook receiver</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: NewWebhookReceiver
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4328-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4328-136">CommonParameters</span></span>
<span data-ttu-id="e4328-137">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="e4328-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4328-138">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="e4328-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4328-139">輸入</span><span class="sxs-lookup"><span data-stu-id="e4328-139">INPUTS</span></span>

### <span data-ttu-id="e4328-140">所有</span><span class="sxs-lookup"><span data-stu-id="e4328-140">None</span></span>
<span data-ttu-id="e4328-141">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="e4328-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e4328-142">輸出</span><span class="sxs-lookup"><span data-stu-id="e4328-142">OUTPUTS</span></span>

### <span data-ttu-id="e4328-143">PSActionGroupReceiverBase 中的 OutputClasses。</span><span class="sxs-lookup"><span data-stu-id="e4328-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase</span></span>

## <span data-ttu-id="e4328-144">筆記</span><span class="sxs-lookup"><span data-stu-id="e4328-144">NOTES</span></span>

## <span data-ttu-id="e4328-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="e4328-145">RELATED LINKS</span></span>

<span data-ttu-id="e4328-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
[AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
[移除-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="e4328-146">[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md)
[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)</span></span>
