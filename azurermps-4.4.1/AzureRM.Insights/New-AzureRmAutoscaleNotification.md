---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: f6791d2cc962f0bb0db038ad8c5391425c09bfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455807"
---
# <span data-ttu-id="1b2ce-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="1b2ce-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="1b2ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1b2ce-102">SYNOPSIS</span></span>
<span data-ttu-id="1b2ce-103">建立自動縮放電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="1b2ce-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b2ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="1b2ce-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhooks] <WebhookNotification[]>] [[-CustomEmails] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b2ce-105">說明</span><span class="sxs-lookup"><span data-stu-id="1b2ce-105">DESCRIPTION</span></span>
<span data-ttu-id="1b2ce-106">**新的-AzureRmAutoscaleNotification** Cmdlet 會建立自動縮放的電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="1b2ce-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="1b2ce-107">示例</span><span class="sxs-lookup"><span data-stu-id="1b2ce-107">EXAMPLES</span></span>

### <span data-ttu-id="1b2ce-108">範例1：建立自動縮放電子郵件通知</span><span class="sxs-lookup"><span data-stu-id="1b2ce-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="1b2ce-109">這個命令會建立兩個指定位址的 Autosacale 電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="1b2ce-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="1b2ce-110">範例2：為訂閱管理員建立自動縮放電子郵件通知</span><span class="sxs-lookup"><span data-stu-id="1b2ce-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="1b2ce-111">這個命令會建立訂閱系統管理員的 Autosacale 電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="1b2ce-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="1b2ce-112">參數</span><span class="sxs-lookup"><span data-stu-id="1b2ce-112">PARAMETERS</span></span>

### <span data-ttu-id="1b2ce-113">-CustomEmails</span><span class="sxs-lookup"><span data-stu-id="1b2ce-113">-CustomEmails</span></span>
<span data-ttu-id="1b2ce-114">指定以逗號分隔的電子郵件地址清單。</span><span class="sxs-lookup"><span data-stu-id="1b2ce-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2ce-115">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="1b2ce-115">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="1b2ce-116">表示此操作會傳送電子郵件通知給訂閱管理員。</span><span class="sxs-lookup"><span data-stu-id="1b2ce-116">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="1b2ce-117">-SendEmailToSubscriptionCoAdministrators</span><span class="sxs-lookup"><span data-stu-id="1b2ce-117">-SendEmailToSubscriptionCoAdministrators</span></span>
<span data-ttu-id="1b2ce-118">表示此操作會傳送電子郵件通知給訂閱共同管理員。</span><span class="sxs-lookup"><span data-stu-id="1b2ce-118">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="1b2ce-119">-Webhooks</span><span class="sxs-lookup"><span data-stu-id="1b2ce-119">-Webhooks</span></span>
<span data-ttu-id="1b2ce-120">指定以逗號分隔的自動縮放 webhooks 清單。</span><span class="sxs-lookup"><span data-stu-id="1b2ce-120">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b2ce-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b2ce-121">-DefaultProfile</span></span>
<span data-ttu-id="1b2ce-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="1b2ce-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b2ce-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b2ce-123">CommonParameters</span></span>
<span data-ttu-id="1b2ce-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1b2ce-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b2ce-125">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1b2ce-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b2ce-126">輸入</span><span class="sxs-lookup"><span data-stu-id="1b2ce-126">INPUTS</span></span>

## <span data-ttu-id="1b2ce-127">輸出</span><span class="sxs-lookup"><span data-stu-id="1b2ce-127">OUTPUTS</span></span>

### <span data-ttu-id="1b2ce-128">AutoscaleNotification 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="1b2ce-128">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="1b2ce-129">筆記</span><span class="sxs-lookup"><span data-stu-id="1b2ce-129">NOTES</span></span>

## <span data-ttu-id="1b2ce-130">相關連結</span><span class="sxs-lookup"><span data-stu-id="1b2ce-130">RELATED LINKS</span></span>

[<span data-ttu-id="1b2ce-131">新-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="1b2ce-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


