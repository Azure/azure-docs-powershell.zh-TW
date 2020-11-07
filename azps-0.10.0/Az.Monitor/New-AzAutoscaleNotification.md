---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: da3c2e26b5b83f43802734d95d17b8bbcaa4194c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/16/2020
ms.locfileid: "93794602"
---
# <span data-ttu-id="ea5a5-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="ea5a5-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="ea5a5-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ea5a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5a5-103">建立自動縮放電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="ea5a5-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="ea5a5-104">句法</span><span class="sxs-lookup"><span data-stu-id="ea5a5-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea5a5-105">說明</span><span class="sxs-lookup"><span data-stu-id="ea5a5-105">DESCRIPTION</span></span>
<span data-ttu-id="ea5a5-106">**新的-AzAutoscaleNotification** Cmdlet 會建立自動縮放的電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="ea5a5-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="ea5a5-107">示例</span><span class="sxs-lookup"><span data-stu-id="ea5a5-107">EXAMPLES</span></span>

### <span data-ttu-id="ea5a5-108">範例1：建立自動縮放電子郵件通知</span><span class="sxs-lookup"><span data-stu-id="ea5a5-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="ea5a5-109">這個命令會建立兩個指定位址的 Autosacale 電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="ea5a5-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="ea5a5-110">範例2：為訂閱管理員建立自動縮放電子郵件通知</span><span class="sxs-lookup"><span data-stu-id="ea5a5-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="ea5a5-111">這個命令會建立訂閱系統管理員的 Autosacale 電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="ea5a5-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="ea5a5-112">參數</span><span class="sxs-lookup"><span data-stu-id="ea5a5-112">PARAMETERS</span></span>

### <span data-ttu-id="ea5a5-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="ea5a5-113">-CustomEmail</span></span>
<span data-ttu-id="ea5a5-114">指定以逗號分隔的電子郵件地址清單。</span><span class="sxs-lookup"><span data-stu-id="ea5a5-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="ea5a5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea5a5-115">-DefaultProfile</span></span>
<span data-ttu-id="ea5a5-116">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ea5a5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ea5a5-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="ea5a5-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="ea5a5-118">表示此操作會傳送電子郵件通知給訂閱管理員。</span><span class="sxs-lookup"><span data-stu-id="ea5a5-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="ea5a5-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="ea5a5-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="ea5a5-120">表示此操作會傳送電子郵件通知給訂閱共同管理員。</span><span class="sxs-lookup"><span data-stu-id="ea5a5-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="ea5a5-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="ea5a5-121">-Webhook</span></span>
<span data-ttu-id="ea5a5-122">指定以逗號分隔的自動縮放 webhooks 清單。</span><span class="sxs-lookup"><span data-stu-id="ea5a5-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="ea5a5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5a5-123">CommonParameters</span></span>
<span data-ttu-id="ea5a5-124">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ea5a5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5a5-125">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ea5a5-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5a5-126">輸入</span><span class="sxs-lookup"><span data-stu-id="ea5a5-126">INPUTS</span></span>

### <span data-ttu-id="ea5a5-127">WebhookNotification [] 中的 [管理模型]</span><span class="sxs-lookup"><span data-stu-id="ea5a5-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="ea5a5-128">System.object []</span><span class="sxs-lookup"><span data-stu-id="ea5a5-128">System.String[]</span></span>

### <span data-ttu-id="ea5a5-129">SwitchParameter 的系統管理功能</span><span class="sxs-lookup"><span data-stu-id="ea5a5-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ea5a5-130">輸出</span><span class="sxs-lookup"><span data-stu-id="ea5a5-130">OUTPUTS</span></span>

### <span data-ttu-id="ea5a5-131">AutoscaleNotification 中的 [管理模型]。</span><span class="sxs-lookup"><span data-stu-id="ea5a5-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="ea5a5-132">筆記</span><span class="sxs-lookup"><span data-stu-id="ea5a5-132">NOTES</span></span>

## <span data-ttu-id="ea5a5-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="ea5a5-133">RELATED LINKS</span></span>

[<span data-ttu-id="ea5a5-134">新-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="ea5a5-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


