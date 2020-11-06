---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: ee95455b5081105ec4e28a4811e46ca92bfbc240
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449353"
---
# <span data-ttu-id="a870b-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="a870b-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="a870b-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a870b-102">SYNOPSIS</span></span>
<span data-ttu-id="a870b-103">建立自動縮放電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="a870b-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a870b-104">句法</span><span class="sxs-lookup"><span data-stu-id="a870b-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator] 
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a870b-105">說明</span><span class="sxs-lookup"><span data-stu-id="a870b-105">DESCRIPTION</span></span>
<span data-ttu-id="a870b-106">**新的-AzureRmAutoscaleNotification** Cmdlet 會建立自動縮放的電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="a870b-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="a870b-107">示例</span><span class="sxs-lookup"><span data-stu-id="a870b-107">EXAMPLES</span></span>

### <span data-ttu-id="a870b-108">範例1：建立自動縮放電子郵件通知</span><span class="sxs-lookup"><span data-stu-id="a870b-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="a870b-109">這個命令會建立兩個指定位址的 Autosacale 電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="a870b-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="a870b-110">範例2：為訂閱管理員建立自動縮放電子郵件通知</span><span class="sxs-lookup"><span data-stu-id="a870b-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="a870b-111">這個命令會建立訂閱系統管理員的 Autosacale 電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="a870b-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="a870b-112">參數</span><span class="sxs-lookup"><span data-stu-id="a870b-112">PARAMETERS</span></span>

### <span data-ttu-id="a870b-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="a870b-113">-CustomEmail</span></span>
<span data-ttu-id="a870b-114">指定以逗號分隔的電子郵件地址清單。</span><span class="sxs-lookup"><span data-stu-id="a870b-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CustomEmails

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a870b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a870b-115">-DefaultProfile</span></span>
<span data-ttu-id="a870b-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="a870b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a870b-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="a870b-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="a870b-118">表示此操作會傳送電子郵件通知給訂閱管理員。</span><span class="sxs-lookup"><span data-stu-id="a870b-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a870b-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="a870b-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="a870b-120">表示此操作會傳送電子郵件通知給訂閱共同管理員。</span><span class="sxs-lookup"><span data-stu-id="a870b-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: SendEmailToSubscriptionCoAdministrators

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a870b-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="a870b-121">-Webhook</span></span>
<span data-ttu-id="a870b-122">指定以逗號分隔的自動縮放 webhooks 清單。</span><span class="sxs-lookup"><span data-stu-id="a870b-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: WebhookNotification[]
Parameter Sets: (All)
Aliases: Webhooks

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a870b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a870b-123">CommonParameters</span></span>
<span data-ttu-id="a870b-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a870b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a870b-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a870b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a870b-126">輸入</span><span class="sxs-lookup"><span data-stu-id="a870b-126">INPUTS</span></span>

### <span data-ttu-id="a870b-127">所有</span><span class="sxs-lookup"><span data-stu-id="a870b-127">None</span></span>
<span data-ttu-id="a870b-128">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="a870b-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a870b-129">輸出</span><span class="sxs-lookup"><span data-stu-id="a870b-129">OUTPUTS</span></span>

### <span data-ttu-id="a870b-130">AutoscaleNotification 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="a870b-130">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="a870b-131">筆記</span><span class="sxs-lookup"><span data-stu-id="a870b-131">NOTES</span></span>

## <span data-ttu-id="a870b-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="a870b-132">RELATED LINKS</span></span>

[<span data-ttu-id="a870b-133">新-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="a870b-133">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


