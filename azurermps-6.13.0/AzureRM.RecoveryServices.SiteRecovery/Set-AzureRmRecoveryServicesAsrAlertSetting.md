---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 70816649b33cd91c7d378b3588b443e4dd5b8fe9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448955"
---
# <span data-ttu-id="ca407-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="ca407-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="ca407-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ca407-102">SYNOPSIS</span></span>
<span data-ttu-id="ca407-103">針對保存庫 (電子郵件通知) 設定 Azure 網站復原通知設定。</span><span class="sxs-lookup"><span data-stu-id="ca407-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca407-104">句法</span><span class="sxs-lookup"><span data-stu-id="ca407-104">SYNTAX</span></span>

### <span data-ttu-id="ca407-105">設定 (預設) </span><span class="sxs-lookup"><span data-stu-id="ca407-105">Set (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca407-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ca407-106">EmailToSubscriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca407-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ca407-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca407-108">禁止</span><span class="sxs-lookup"><span data-stu-id="ca407-108">Disable</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca407-109">說明</span><span class="sxs-lookup"><span data-stu-id="ca407-109">DESCRIPTION</span></span>
<span data-ttu-id="ca407-110">AzureRmRecoveryServicesAsrNotificationSetting Cmdlet 會針對保存庫 (電子郵件通知) 來 **設定** Azure 網站復原通知設定。</span><span class="sxs-lookup"><span data-stu-id="ca407-110">The **Set-AzureRmRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="ca407-111">示例</span><span class="sxs-lookup"><span data-stu-id="ca407-111">EXAMPLES</span></span>

### <span data-ttu-id="ca407-112">範例1</span><span class="sxs-lookup"><span data-stu-id="ca407-112">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="ca407-113">停用通知。</span><span class="sxs-lookup"><span data-stu-id="ca407-113">Disable notification.</span></span>

### <span data-ttu-id="ca407-114">範例2</span><span class="sxs-lookup"><span data-stu-id="ca407-114">Example 2</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="ca407-115">針對自訂電子郵件地址 (s) 及訂閱擁有者設定通知。</span><span class="sxs-lookup"><span data-stu-id="ca407-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="ca407-116">參數</span><span class="sxs-lookup"><span data-stu-id="ca407-116">PARAMETERS</span></span>

### <span data-ttu-id="ca407-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="ca407-117">-CustomEmailAddress</span></span>
<span data-ttu-id="ca407-118">傳送給電子郵件的通知/通知。</span><span class="sxs-lookup"><span data-stu-id="ca407-118">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="ca407-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca407-119">-DefaultProfile</span></span>
<span data-ttu-id="ca407-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ca407-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca407-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ca407-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="ca407-122">切換參數指定 [啟用訂閱擁有者的通知]。</span><span class="sxs-lookup"><span data-stu-id="ca407-122">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="ca407-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="ca407-123">-DisableNotification</span></span>
<span data-ttu-id="ca407-124">[標記] 可停用所有通知。</span><span class="sxs-lookup"><span data-stu-id="ca407-124">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="ca407-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="ca407-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="ca407-126">切換參數指定 [啟用訂閱擁有者的通知]。</span><span class="sxs-lookup"><span data-stu-id="ca407-126">Switch paramter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="ca407-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="ca407-127">-LocaleID</span></span>
<span data-ttu-id="ca407-128">從 microsoft)  (支援的區域性代碼，以電子郵件傳送通知/notifcation 給使用者的語言。</span><span class="sxs-lookup"><span data-stu-id="ca407-128">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="ca407-129">-確認</span><span class="sxs-lookup"><span data-stu-id="ca407-129">-Confirm</span></span>
<span data-ttu-id="ca407-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ca407-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca407-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca407-131">-WhatIf</span></span>
<span data-ttu-id="ca407-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ca407-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca407-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ca407-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca407-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca407-134">CommonParameters</span></span>
<span data-ttu-id="ca407-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ca407-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca407-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ca407-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca407-137">輸入</span><span class="sxs-lookup"><span data-stu-id="ca407-137">INPUTS</span></span>

### <span data-ttu-id="ca407-138">所有</span><span class="sxs-lookup"><span data-stu-id="ca407-138">None</span></span>

## <span data-ttu-id="ca407-139">輸出</span><span class="sxs-lookup"><span data-stu-id="ca407-139">OUTPUTS</span></span>

### <span data-ttu-id="ca407-140">System.object. IEnumerable "1 [ASRAlertSetting，RecoveryServices. SiteRecovery，Version = 0.1.1.0，Culture = 中性，PublicKeyToken = null]]。））。））。）</span><span class="sxs-lookup"><span data-stu-id="ca407-140">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ca407-141">筆記</span><span class="sxs-lookup"><span data-stu-id="ca407-141">NOTES</span></span>

## <span data-ttu-id="ca407-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="ca407-142">RELATED LINKS</span></span>
