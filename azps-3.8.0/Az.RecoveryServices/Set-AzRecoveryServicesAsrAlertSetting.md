---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: bd470a027285f66f15c831950639edaeb750c302
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93959474"
---
# <span data-ttu-id="273d4-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="273d4-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="273d4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="273d4-102">SYNOPSIS</span></span>
<span data-ttu-id="273d4-103">針對保存庫 (電子郵件通知) 設定 Azure 網站復原通知設定。</span><span class="sxs-lookup"><span data-stu-id="273d4-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="273d4-104">句法</span><span class="sxs-lookup"><span data-stu-id="273d4-104">SYNTAX</span></span>

### <span data-ttu-id="273d4-105">設定 (預設) </span><span class="sxs-lookup"><span data-stu-id="273d4-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="273d4-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="273d4-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="273d4-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="273d4-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="273d4-108">禁止</span><span class="sxs-lookup"><span data-stu-id="273d4-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="273d4-109">說明</span><span class="sxs-lookup"><span data-stu-id="273d4-109">DESCRIPTION</span></span>
<span data-ttu-id="273d4-110">AzRecoveryServicesAsrNotificationSetting Cmdlet 會針對保存庫 (電子郵件通知) 來 **設定** Azure 網站復原通知設定。</span><span class="sxs-lookup"><span data-stu-id="273d4-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="273d4-111">示例</span><span class="sxs-lookup"><span data-stu-id="273d4-111">EXAMPLES</span></span>

### <span data-ttu-id="273d4-112">範例1</span><span class="sxs-lookup"><span data-stu-id="273d4-112">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="273d4-113">停用通知。</span><span class="sxs-lookup"><span data-stu-id="273d4-113">Disable notification.</span></span>

### <span data-ttu-id="273d4-114">範例2</span><span class="sxs-lookup"><span data-stu-id="273d4-114">Example 2</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="273d4-115">針對自訂電子郵件地址 (s) 及訂閱擁有者設定通知。</span><span class="sxs-lookup"><span data-stu-id="273d4-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="273d4-116">參數</span><span class="sxs-lookup"><span data-stu-id="273d4-116">PARAMETERS</span></span>

### <span data-ttu-id="273d4-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="273d4-117">-CustomEmailAddress</span></span>
<span data-ttu-id="273d4-118">傳送給電子郵件的通知/通知。</span><span class="sxs-lookup"><span data-stu-id="273d4-118">Alert / Notification sent to emails.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="273d4-119">-DefaultProfile</span></span>
<span data-ttu-id="273d4-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="273d4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="273d4-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="273d4-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="273d4-122">切換參數指定 [啟用訂閱擁有者的通知]。</span><span class="sxs-lookup"><span data-stu-id="273d4-122">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273d4-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="273d4-123">-DisableNotification</span></span>
<span data-ttu-id="273d4-124">[標記] 可停用所有通知。</span><span class="sxs-lookup"><span data-stu-id="273d4-124">Flag to disable all notification.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273d4-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="273d4-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="273d4-126">切換參數指定 [啟用訂閱擁有者的通知]。</span><span class="sxs-lookup"><span data-stu-id="273d4-126">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273d4-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="273d4-127">-LocaleID</span></span>
<span data-ttu-id="273d4-128">從 microsoft)  (支援的區域性代碼，以電子郵件傳送通知/notification 給使用者的語言。</span><span class="sxs-lookup"><span data-stu-id="273d4-128">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: System.String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="273d4-129">-確認</span><span class="sxs-lookup"><span data-stu-id="273d4-129">-Confirm</span></span>
<span data-ttu-id="273d4-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="273d4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="273d4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="273d4-131">-WhatIf</span></span>
<span data-ttu-id="273d4-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="273d4-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="273d4-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="273d4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="273d4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="273d4-134">CommonParameters</span></span>
<span data-ttu-id="273d4-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="273d4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="273d4-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="273d4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="273d4-137">輸入</span><span class="sxs-lookup"><span data-stu-id="273d4-137">INPUTS</span></span>

### <span data-ttu-id="273d4-138">所有</span><span class="sxs-lookup"><span data-stu-id="273d4-138">None</span></span>

## <span data-ttu-id="273d4-139">輸出</span><span class="sxs-lookup"><span data-stu-id="273d4-139">OUTPUTS</span></span>

### <span data-ttu-id="273d4-140">RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="273d4-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="273d4-141">筆記</span><span class="sxs-lookup"><span data-stu-id="273d4-141">NOTES</span></span>

## <span data-ttu-id="273d4-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="273d4-142">RELATED LINKS</span></span>
