---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Set-AzSecurityContact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityContact.md
ms.openlocfilehash: 8cd5adee5e8b992cf709b76996a70760f3fd90a5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910626"
---
# <span data-ttu-id="fd42a-101">Set-AzSecurityContact</span><span class="sxs-lookup"><span data-stu-id="fd42a-101">Set-AzSecurityContact</span></span>

## <span data-ttu-id="fd42a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="fd42a-102">SYNOPSIS</span></span>
<span data-ttu-id="fd42a-103">更新訂閱的安全性連絡人。</span><span class="sxs-lookup"><span data-stu-id="fd42a-103">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="fd42a-104">語法</span><span class="sxs-lookup"><span data-stu-id="fd42a-104">SYNTAX</span></span>

```
Set-AzSecurityContact -Name <String> -Email <String> [-Phone <String>] [-AlertAdmin] [-NotifyOnAlert]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd42a-105">描述</span><span class="sxs-lookup"><span data-stu-id="fd42a-105">DESCRIPTION</span></span>
<span data-ttu-id="fd42a-106">更新訂閱的安全性連絡人。</span><span class="sxs-lookup"><span data-stu-id="fd42a-106">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="fd42a-107">例子</span><span class="sxs-lookup"><span data-stu-id="fd42a-107">EXAMPLES</span></span>

### <span data-ttu-id="fd42a-108">範例 1</span><span class="sxs-lookup"><span data-stu-id="fd42a-108">Example 1</span></span>
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

<span data-ttu-id="fd42a-109">更新訂閱的安全性連絡人。</span><span class="sxs-lookup"><span data-stu-id="fd42a-109">Updates a security contact for a subscription.</span></span>

## <span data-ttu-id="fd42a-110">參數</span><span class="sxs-lookup"><span data-stu-id="fd42a-110">PARAMETERS</span></span>

### <span data-ttu-id="fd42a-111">-AlertAdmin</span><span class="sxs-lookup"><span data-stu-id="fd42a-111">-AlertAdmin</span></span>
<span data-ttu-id="fd42a-112">通知系統管理員。</span><span class="sxs-lookup"><span data-stu-id="fd42a-112">Alerts To Administrators.</span></span>

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

### <span data-ttu-id="fd42a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd42a-113">-DefaultProfile</span></span>
<span data-ttu-id="fd42a-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="fd42a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd42a-115">-電子郵件</span><span class="sxs-lookup"><span data-stu-id="fd42a-115">-Email</span></span>
<span data-ttu-id="fd42a-116">電子郵件。</span><span class="sxs-lookup"><span data-stu-id="fd42a-116">E-Mail.</span></span>

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

### <span data-ttu-id="fd42a-117">-名稱</span><span class="sxs-lookup"><span data-stu-id="fd42a-117">-Name</span></span>
<span data-ttu-id="fd42a-118">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="fd42a-118">Resource name.</span></span>

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

### <span data-ttu-id="fd42a-119">-NotifyOnAlert</span><span class="sxs-lookup"><span data-stu-id="fd42a-119">-NotifyOnAlert</span></span>
<span data-ttu-id="fd42a-120">警示通知。</span><span class="sxs-lookup"><span data-stu-id="fd42a-120">Alert Notifications.</span></span>

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

### <span data-ttu-id="fd42a-121">-電話</span><span class="sxs-lookup"><span data-stu-id="fd42a-121">-Phone</span></span>
<span data-ttu-id="fd42a-122">電話。</span><span class="sxs-lookup"><span data-stu-id="fd42a-122">Phone.</span></span>

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

### <span data-ttu-id="fd42a-123">-確認</span><span class="sxs-lookup"><span data-stu-id="fd42a-123">-Confirm</span></span>
<span data-ttu-id="fd42a-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="fd42a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd42a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd42a-125">-WhatIf</span></span>
<span data-ttu-id="fd42a-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="fd42a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd42a-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="fd42a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd42a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd42a-128">CommonParameters</span></span>
<span data-ttu-id="fd42a-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="fd42a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd42a-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd42a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd42a-131">輸入</span><span class="sxs-lookup"><span data-stu-id="fd42a-131">INPUTS</span></span>

### <span data-ttu-id="fd42a-132">沒有</span><span class="sxs-lookup"><span data-stu-id="fd42a-132">None</span></span>

## <span data-ttu-id="fd42a-133">輸出</span><span class="sxs-lookup"><span data-stu-id="fd42a-133">OUTPUTS</span></span>

### <span data-ttu-id="fd42a-134">Microsoft.Azure.Commands.Security.models.SecurityContacts.PSSecurityContact</span><span class="sxs-lookup"><span data-stu-id="fd42a-134">Microsoft.Azure.Commands.Security.Models.SecurityContacts.PSSecurityContact</span></span>

## <span data-ttu-id="fd42a-135">筆記</span><span class="sxs-lookup"><span data-stu-id="fd42a-135">NOTES</span></span>

## <span data-ttu-id="fd42a-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="fd42a-136">RELATED LINKS</span></span>
