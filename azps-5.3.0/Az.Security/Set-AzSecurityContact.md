---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 504f07092a0a8e246e778421748f1cd807b04a77
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98448619"
---
# <span data-ttu-id="8048c-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="8048c-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="8048c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8048c-102">SYNOPSIS</span></span>
<span data-ttu-id="8048c-103">更新訂閱的安全連絡人。</span><span class="sxs-lookup"><span data-stu-id="8048c-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="8048c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8048c-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8048c-105">說明</span><span class="sxs-lookup"><span data-stu-id="8048c-105">DESCRIPTION</span></span>
<span data-ttu-id="8048c-106">更新訂閱的安全連絡人。</span><span class="sxs-lookup"><span data-stu-id="8048c-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="8048c-107">示例</span><span class="sxs-lookup"><span data-stu-id="8048c-107">EXAMPLES</span></span>

### <span data-ttu-id="8048c-108">範例1</span><span class="sxs-lookup"><span data-stu-id="8048c-108">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityContact -Name "default1" -Email "john@contoso.com" -Phone "214275-4038" -AlertAdmin -NotifyOnAlert

Id                 : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/securityContacts/
                     default1
Name               : default1
Email              : john@contoso.com
Phone              : 214275-4038
AlertNotifications : On
AlertsToAdmins     : On
```

<span data-ttu-id="8048c-109">更新訂閱的安全連絡人。</span><span class="sxs-lookup"><span data-stu-id="8048c-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="8048c-110">參數</span><span class="sxs-lookup"><span data-stu-id="8048c-110">PARAMETERS</span></span>

### <span data-ttu-id="8048c-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="8048c-111">-AlertAdmin</span></span>
<span data-ttu-id="8048c-112">給管理員的警示。</span><span class="sxs-lookup"><span data-stu-id="8048c-112">Alerts To Administrators.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8048c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8048c-113">-DefaultProfile</span></span>
<span data-ttu-id="8048c-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="8048c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8048c-115">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="8048c-115">-Email</span></span>
<span data-ttu-id="8048c-116">形式.</span><span class="sxs-lookup"><span data-stu-id="8048c-116">E-Mail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8048c-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="8048c-117">-Name</span></span>
<span data-ttu-id="8048c-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="8048c-118">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8048c-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="8048c-119">-NotifyOnAlert</span></span>
<span data-ttu-id="8048c-120">警示通知。</span><span class="sxs-lookup"><span data-stu-id="8048c-120">Alert Notifications.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8048c-121">-電話</span><span class="sxs-lookup"><span data-stu-id="8048c-121">-Phone</span></span>
<span data-ttu-id="8048c-122">電話.</span><span class="sxs-lookup"><span data-stu-id="8048c-122">Phone.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8048c-123">-確認</span><span class="sxs-lookup"><span data-stu-id="8048c-123">-Confirm</span></span>
<span data-ttu-id="8048c-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="8048c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8048c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8048c-125">-WhatIf</span></span>
<span data-ttu-id="8048c-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8048c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8048c-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8048c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8048c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8048c-128">CommonParameters</span></span>
<span data-ttu-id="8048c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8048c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8048c-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="8048c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8048c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="8048c-131">INPUTS</span></span>

### <span data-ttu-id="8048c-132">所有</span><span class="sxs-lookup"><span data-stu-id="8048c-132">None</span></span>

## <span data-ttu-id="8048c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="8048c-133">OUTPUTS</span></span>

### <span data-ttu-id="8048c-134">PSSecurityContact 中的 SecurityContacts （Security..。</span><span class="sxs-lookup"><span data-stu-id="8048c-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="8048c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="8048c-135">NOTES</span></span>

## <span data-ttu-id="8048c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="8048c-136">RELATED LINKS</span></span>
