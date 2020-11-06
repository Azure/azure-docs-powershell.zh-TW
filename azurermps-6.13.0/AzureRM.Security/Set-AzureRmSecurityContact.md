---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Set-AzureRmSecurityContact.md
ms.openlocfilehash: 30586dcbbc08c31bf9b9fe65886fd2f487398618
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448909"
---
# <span data-ttu-id="872fd-101">Set-AzureRmSecurityContact</span><span class="sxs-lookup"><span data-stu-id="872fd-101">Set-AzureRmSecurityContact</span></span>

## <span data-ttu-id="872fd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="872fd-102">SYNOPSIS</span></span>
<span data-ttu-id="872fd-103">更新訂閱的安全連絡人。</span><span class="sxs-lookup"><span data-stu-id="872fd-103">Updates a security contact for a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="872fd-104">句法</span><span class="sxs-lookup"><span data-stu-id="872fd-104">SYNTAX</span></span>

```
Set-AzureRmSecurityContact -Name <String> -Email <String> -Phone <String> [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="872fd-105">說明</span><span class="sxs-lookup"><span data-stu-id="872fd-105">DESCRIPTION</span></span>
<span data-ttu-id="872fd-106">更新訂閱的安全連絡人。</span><span class="sxs-lookup"><span data-stu-id="872fd-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="872fd-107">示例</span><span class="sxs-lookup"><span data-stu-id="872fd-107">EXAMPLES</span></span>

### <span data-ttu-id="872fd-108">範例1</span><span class="sxs-lookup"><span data-stu-id="872fd-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="872fd-109">更新訂閱的安全連絡人。</span><span class="sxs-lookup"><span data-stu-id="872fd-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="872fd-110">參數</span><span class="sxs-lookup"><span data-stu-id="872fd-110">PARAMETERS</span></span>

### <span data-ttu-id="872fd-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="872fd-111">-AlertAdmin</span></span>
<span data-ttu-id="872fd-112">給管理員的警示。</span><span class="sxs-lookup"><span data-stu-id="872fd-112">Alerts To Administrators.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872fd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="872fd-113">-DefaultProfile</span></span>
<span data-ttu-id="872fd-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="872fd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="872fd-115">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="872fd-115">-Email</span></span>
<span data-ttu-id="872fd-116">形式.</span><span class="sxs-lookup"><span data-stu-id="872fd-116">E-Mail.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872fd-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="872fd-117">-Name</span></span>
<span data-ttu-id="872fd-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="872fd-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872fd-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="872fd-119">-NotifyOnAlert</span></span>
<span data-ttu-id="872fd-120">警示通知。</span><span class="sxs-lookup"><span data-stu-id="872fd-120">Alert Notifications.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872fd-121">-電話</span><span class="sxs-lookup"><span data-stu-id="872fd-121">-Phone</span></span>
<span data-ttu-id="872fd-122">電話.</span><span class="sxs-lookup"><span data-stu-id="872fd-122">Phone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872fd-123">-確認</span><span class="sxs-lookup"><span data-stu-id="872fd-123">-Confirm</span></span>
<span data-ttu-id="872fd-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="872fd-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872fd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="872fd-125">-WhatIf</span></span>
<span data-ttu-id="872fd-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="872fd-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="872fd-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="872fd-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="872fd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="872fd-128">CommonParameters</span></span>
<span data-ttu-id="872fd-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="872fd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="872fd-130">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="872fd-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="872fd-131">輸入</span><span class="sxs-lookup"><span data-stu-id="872fd-131">INPUTS</span></span>

### <span data-ttu-id="872fd-132">System.object</span><span class="sxs-lookup"><span data-stu-id="872fd-132">System.String</span></span>

## <span data-ttu-id="872fd-133">輸出</span><span class="sxs-lookup"><span data-stu-id="872fd-133">OUTPUTS</span></span>

### <span data-ttu-id="872fd-134">PSSecurityContact 中的 SecurityContacts （Security..。</span><span class="sxs-lookup"><span data-stu-id="872fd-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="872fd-135">筆記</span><span class="sxs-lookup"><span data-stu-id="872fd-135">NOTES</span></span>

## <span data-ttu-id="872fd-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="872fd-136">RELATED LINKS</span></span>
