---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: c537908d2249ca5ec8a33adffa4e655b0a9ec6e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909589"
---
# <span data-ttu-id="e7c91-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="e7c91-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="e7c91-102">簡介</span><span class="sxs-lookup"><span data-stu-id="e7c91-102">SYNOPSIS</span></span>
<span data-ttu-id="e7c91-103">建立自動縮放電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="e7c91-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="e7c91-104">語法</span><span class="sxs-lookup"><span data-stu-id="e7c91-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7c91-105">描述</span><span class="sxs-lookup"><span data-stu-id="e7c91-105">DESCRIPTION</span></span>
<span data-ttu-id="e7c91-106">**New-AzAutoscaleNotification** Cmdlet 會針對自動縮放建立電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="e7c91-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="e7c91-107">例子</span><span class="sxs-lookup"><span data-stu-id="e7c91-107">EXAMPLES</span></span>

### <span data-ttu-id="e7c91-108">範例 1：建立自動縮放電子郵件通知</span><span class="sxs-lookup"><span data-stu-id="e7c91-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="e7c91-109">此命令會針對兩個指定的位址建立自動設置電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="e7c91-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="e7c91-110">範例 2：為訂閱系統管理員建立自動縮放電子郵件通知</span><span class="sxs-lookup"><span data-stu-id="e7c91-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="e7c91-111">此命令會為訂閱系統管理員建立自動訂閱電子郵件通知。</span><span class="sxs-lookup"><span data-stu-id="e7c91-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="e7c91-112">參數</span><span class="sxs-lookup"><span data-stu-id="e7c91-112">PARAMETERS</span></span>

### <span data-ttu-id="e7c91-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="e7c91-113">-CustomEmail</span></span>
<span data-ttu-id="e7c91-114">指定電子郵件地址的逗號分隔清單。</span><span class="sxs-lookup"><span data-stu-id="e7c91-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="e7c91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7c91-115">-DefaultProfile</span></span>
<span data-ttu-id="e7c91-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="e7c91-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7c91-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="e7c91-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="e7c91-118">表示此作業會傳送電子郵件通知給訂閱系統管理員。</span><span class="sxs-lookup"><span data-stu-id="e7c91-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="e7c91-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="e7c91-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="e7c91-120">表示此作業會傳送電子郵件通知給訂閱共同管理員。</span><span class="sxs-lookup"><span data-stu-id="e7c91-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="e7c91-121">-Web上</span><span class="sxs-lookup"><span data-stu-id="e7c91-121">-Webhook</span></span>
<span data-ttu-id="e7c91-122">指定自動縮放網頁元件以逗號分隔的清單。</span><span class="sxs-lookup"><span data-stu-id="e7c91-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="e7c91-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7c91-123">CommonParameters</span></span>
<span data-ttu-id="e7c91-124">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="e7c91-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7c91-125">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7c91-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7c91-126">輸入</span><span class="sxs-lookup"><span data-stu-id="e7c91-126">INPUTS</span></span>

### <span data-ttu-id="e7c91-127">Microsoft.Azure.management.Monitor.management.models.WebificationNotification[]</span><span class="sxs-lookup"><span data-stu-id="e7c91-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="e7c91-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e7c91-128">System.String[]</span></span>

### <span data-ttu-id="e7c91-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e7c91-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e7c91-130">輸出</span><span class="sxs-lookup"><span data-stu-id="e7c91-130">OUTPUTS</span></span>

### <span data-ttu-id="e7c91-131">Microsoft.Azure.management.Monitor.management.models.AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="e7c91-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="e7c91-132">筆記</span><span class="sxs-lookup"><span data-stu-id="e7c91-132">NOTES</span></span>

## <span data-ttu-id="e7c91-133">相關連結</span><span class="sxs-lookup"><span data-stu-id="e7c91-133">RELATED LINKS</span></span>

[<span data-ttu-id="e7c91-134">New-AzAutoscaleWeb用</span><span class="sxs-lookup"><span data-stu-id="e7c91-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


